# github报错 ERROR: You're using an RSA key with SHA-1, which is no longer allowed. Please use a newer client or a different key type.

webstorm无法使用git，下载发布github项目

RSA不能用，需要升级

`
ERROR: You're using an RSA key with SHA-1, which is no longer allowed. Please use a newer client or a different key type.
Please see https://github.blog/2021-09-01-improving-git-protocol-security-github/ for more information.
`

**原因：**

git(2.9)版本太低

**解决方法：**

将git卸载重装高版本，安装git 2.36之后，webstrom正常使用git