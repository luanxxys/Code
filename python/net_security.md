### 函数

crypt()
> 快速计算 hash

    import crypt
    crypt.crypt("egg", "HX")

实例：UNIX 口令破解

``` python
import crypt
def test_pass(crypt_pass):
    salt = crypt_pass[0:2]
dcit_file = open('dictionary.txt')
for word in dcit_file.readlines():
    word = word.strip('\n')
    crypt_word = crypt.crypt(word)
    if (crypt_word == crypt_pass):
        print("Found password: %s\n" % word)
        return
    print("Password Not Found.\n")
    return
```

实例：ZIP 文件破解

``` python
import zipfile
def extract_file(z_file, password):
    try:
        z_file.extractall(pwd = password)
        return password
    expect:
        return
def main():
    z_file = zipfile.zipfile('evil.txt')
    pass_file = open('dictionary.txt')
    for line in pass_file.readlines():
        password = line.strip('\n')
        guess = extract_file(z_file, password)
        if guess:
            print("Password = " + password +d '\n')
            exit(0)
if __name__ == '__main__':
    main()
```
