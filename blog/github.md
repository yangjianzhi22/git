# git远程仓库(github)

## 添加远程库

#### 获取ssh key

由于本地Git仓库和GitHub仓库之间的传输是通过SSH加密的，所以我们需要配置验证信息:

使用以下命令生成**ssh key**:

`
// 默认一路回车就行.
ssh-keygen -t rsa -C "youremail@example.com"
`

成功后会在 ~/ 下生成 .ssh 文件夹，进去，打开 id_rsa.pub，复制里面的 key

#### github添加ssh key

回到 github 上，进入 Account => Settings（账户配置）=> SSH and GPG keys

title 设置标题，可以随便填，粘贴在你电脑上生成的 key

#### 验证

输入以下命令：

`
$ ssh -T git@github.com

The authenticity of host 'github.com (52.74.223.119)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes                   # 输入 yes
Warning: Permanently added 'github.com,52.74.223.119' (RSA) to the list of known hosts.
Hi tianqixin! You've successfully authenticated, but GitHub does not provide shell access. # 成功信息
`