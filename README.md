# snlp_story_understanding

## 生成shh key

在terminal输入

```bash
$ ssh-keygen -t rsa -C "youremail@xxx.com" -f ~/.ssh/id_rsa_snlp_github
```

摁两次回车（或者也可以自己设置密码）

检查是否生成 id_rsa_snlp_github.pub

```bash
$ cd ~/.ssh
$ ls
```

然后输入

```bash
$ pbcopy < ~/.ssh/id_rsa_snlp_github.pub
```

公钥已经复制到了剪贴板，粘贴后发送给我（@圆圆哥哥）

我会把公钥添加到repository里，我回复之后，在terminal输入

```bash
$ ssh-add -K ~/.ssh/id_rsa_snlp_github
```

查看添加结果

```bash
$ ssh-add -l
```

创建本地配置文件

```bash
$ touch config
```

打开配置文件(Finder -> Go to Folder -> 输入~/.shh), 输入如下内容

```bash
Host snlp.github.com
		HostName github.com
		User git
		PreferredAuthentications publickey
		IdentityFile ~/.ssh/id_rsa_snlp_github
```

保存后在terminal输入

```bash
$ ssh -T git@snlp.github.com
```

如果出现 Hi XXXXXXX 这样的内容就代表成功了



## Clone 文件

在 stat-nlp-book/assignments/2017/ 建立文件夹 assignment3

在terminal 中用 ``cd`` 命令到达该目录下，输入

```bash
$ git clone git@snlp.github.com:TheSuguser/snlp_story_understanding.git
```



## Git 操作

### 建立自己的分支

从个



qxy edit