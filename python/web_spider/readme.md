# Python spider

## 主要流程

### 检查 robots.txt

获取方式

    <website/robots.txt>

文档示例

    # 禁止用户代理为 BadCrawler 的爬虫爬取该网站
    # section 1
    User-agent: BadCrawler
    Disallow: /

    # 无论何种代理，应在两次下载请求之间给出 5 秒的抓取延迟
    # section 2
    User-agent: *
    Craw-delay: 5
    # 封禁爬取了不允许链接的恶意爬虫
    Disallow: /trap

    # 定义了一个 Sitemap 文件
    # section 3
    sitemap： <website/sitemap.xml>

### 检查网站地图

网站地图提供了所有网页的链接，即一种爬取网站的有效方式，但该文件经常存在缺失、过期或不完整的问题。

[网站地图标准定义](http://www.sitemaps.org/protocol.html)

### 估算网站大小

简便方法： Google

site 关键词

    # 估算网页数量（网站较小时比较精确）
    site: <website>

域名后面添加 URL 路径，可以对结果过滤

只搜索国家页面

    site: <website>／view

### 识别网站所用的技术： builtwith

    import builtwith
    builtwith.parse('<website>')

### 寻找网站所有者

    import whois
    print whois.whois('<website>')

### 下载网页

``` python
def download(url, user_agent='swap'，num_retries=2):
    print("Downloading", url)

    # 设置用户代理
    headers = {'User_agent': user_agent}
    request = urllib2.Request(url, headers=headers)

    # 捕获异常
    try:
        html = urllib2.urlopen(url).read()
    except urllib2URLError as e:
        print("Download error:", e.reason
        html = None

        # 重试下载
        if num_retries > 0:
            if hasattr(e,'code') and 500 <= e.code <600:
                return download(url, num_retries-1)
    return html
```

### 网站地图爬虫

用一个简单的正则表达式，从 <loc> 标签中提取出 URL，从而解析网站地图。

关键步骤

``` python
#　download the sitemapfile
sitemap = download(url)

# extract the sitemap links
links = re.findall('<loc>(.*?)</loc>loc>', sitemap)

# download each link
for link in links:
    html = download(link)
```

### ID 遍历爬虫

适用于只在结尾处有区别的　URL，且末尾的　ID　连续

``` pyhton
# maximum number of consecutive download errors
max_errors = 5

# current number of consecutive download errors
num_errors = 0

for page in itertools.count(1):

    # ｐｒｏｂｌｅｍ
    url = '<website>／view/-%d' % page
    html = download(url)
    if html is None:

        # received an error trying to download this webpage
        num_errors += 1
        if num_errors == max_errors:
            break
    else:
        num_errors = 0
```

### 链接爬虫

1. 利用正则表达式，爬取特定内容的网页

1. 相对链接　--> 绝对链接

1. 存储已发现的　URL，避免重复下载

    ``` python
    import re
    import urlparse
    def link_crawler(seed_url, link_regex):
        crawl_queue = [seed_url]

        ＃　keep track which URL's have seen before
        seen = set(crawl_queue)
        while crawl_queue:
            url = crawl_queue.pop()
            html = download(url)
            for link in get_links(html):

                # check if link matches expected regex
                if re.match(link_regex, link):

                    # form absolute link
                    link = urlparse.urljoin(seed_url, link)

                    # check if have already seen this link
                    if link not in seen：
                        seen.add(link)
                        crawl_queue.append(link)
    ```

### 高级功能

- 解析　robots.txt --> 避免下载禁止爬取的 URL
- 支持代理（requests 模块更友好）
- 下载限速
- 避免爬虫陷阱 --> 设置深度

## 技巧

- [通过缓存结果避免重复下载](下载缓存.md)
- [网页抓取](数据抓取.md)
