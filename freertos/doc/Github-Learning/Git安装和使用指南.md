> Git是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理

#### 1.Git安装
Git客户端官网下载链接：[Git下载](https://git-scm.com/downloads)（选择适合自己本机的版本下载，可以到战队仓库里面下载）

	下载后一直next，选择命令行工具，一般选择:User Git from Git Bash only，点击Next(可以更改安装目录为其他盘，注意安装目录不要有中文和空格)

#### 2. Git配置
安装完成后，按下WIN+R 打开命令行，输入`git --version`，如果出现版本号，则表示安装成功

	右键桌面或者找到git bash打开
	使用以下命令来配置你的用户名和邮箱：
	>git config --global user.name "github上的注册的用户名"
	>git config --global user.email "github上的注册的邮箱"

	你可以使用以下命令来检查配置是否成功：
	>git config --global --list

（没有github账户就开VPN去注册一个）

#### 3. 添加SSH密钥(需要向管理者获取密钥)
	SSH添加后，可以直接使用SSH进行克隆
桌面右键鼠标 点击GIt Bash Here，打开终端窗口，ssh-keygen -t rsa -C "xxxxx@xxxxx.com"，按照提示完成三次回车，即可生成ssh key
![[image-10.png]]
可用cat ~/.ssh/id_rsa.pub 查看生成的钥匙信息
![[image-11.png]]
拷贝上面的钥匙信息，在你的Git（Gitee）账号里面添加 SSH 公钥管理（这里以 Gitee 为例）
![[image-12.png]]
回到终端 ssh -T git@gitee.com ，若返回 `Hi XXX! You've successfully authenticated, but Gitee.com does not provide shell access.` 内容，则证明添加成功。

#### 4. Git基本命令
![[image-4.png]]

#### 5.上传仓库步骤
	1.使当前目录成为可管理的本地仓库
	>git init
	2.添加文件到仓库
	>git add . # 添加所有文件
	>git add ./<文件名> # 添加指定文件的文件路径（例如：git add ./abc.text）
	3.添加提交记录信息
	>git commit -m "说明文字"
	4.上传至仓库
	>git push -u origin <分支名> # 初次上传
	>git push origin <分支名> # 后续上传

#### 6.删除文件步骤（前三步非必要，若无克隆到本地则需克隆）

	1.到需要克隆的github页面，点击Code->SSH复制地址
	2.克隆远程仓库
	>git clone <地址>
	3.拉取远程仓库
	>git pull origin <分支名>
	4.查看仓库已有文件
	>dir
	5.选择想要删除的文件夹/文件进行删除
	>git rm -r --cached <文件/文件名>
	6.提交删除说明
	>git commit -m '说明文字'
	7.更新GitHub远程仓库（远程仓库中无内容，必须要在 push 后加上 -u，后续不需要）
	>git push -u origin <分支名>	


[使用vscode配合git实现代码仓库回滚_vscode代码回滚-CSDN博客](https://blog.csdn.net/qq_44741577/article/details/149195023?ops_request_misc=&request_id=&biz_id=102&utm_term=vscode%E7%9A%84git%E5%9B%9E%E9%80%80&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-149195023.142^v102^pc_search_result_base1&spm=1018.2226.3001.4187)



