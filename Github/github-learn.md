## 关于github的使用

[**github官方说明书**](https://git-scm.com/book/zh/v2)

* **gitbub使用步骤：**

1. 新建仓库
2. 编写文件
3. 编写`"readme.md"`文件
4. 分部使用命令：
```
git init
git add README.md (这里也可以不用文件名，就用:'git add .')
git commit -m "first commit" (这里也可以用:git commit -a -m "Init commit")
git remote add origin https://github.com/hermanxie/刚才新建的仓库名.git
git push -u origin master

修改仓库：
git add .
git commit -a -m "说明"
git push
```

* **gihub内的菜单：**

1. Fork:复制别人的仓库
2. Clone or download:通过命令复制仓库并下载到你的电脑文件夹内

* **gihub新建仓库及版本提交步骤：**
1. 确定本地文件目录；
2. 输入命令`git init`：初始化仓库（创建空的仓库）；
3. 输入命令`git status`：提交到暂存仓库（该命令要不断的使用）；
4. 输入命令`git add`：提交到版本控制管辖范围；
5. 输入命令`git commit`：提交版本（需要编写说明）;
6. 在github新建仓库；
7. 关联本地仓库`git remote add origin https://github.com/hermanxie/刚才新建的仓库名.git`;  
8. 把本地仓库的内容推上github:`git push -u origin master`;

**git其他命令：**

`git restore --staged <你不想提交的文件名>`：把你**不想提交**的文件从暂时的版本控制仓库里拿出来；  
`git log`:查看提交记录；  
`git branch -a`: 查看'branchname'；  
`git --Force`: 查看隐藏文件'.git'文件；  


---
* **解决异常：**

[**GitHub帮助查询**](https://help.github.com/cn/github)

**问题一:**

***当输入`git push`后出现异常：***  
>! [rejected]        master -> master (non-fast-forward)  
error: failed to push some refs to 'ssh://git@*****.git'  
hint: Updates were rejected because the tip of your current branch is behind  
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.  
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

***解决办法：***

修改指令：

`git pull --rebase origin master`
 

查看是否有需要再进一步的commit一下，解决一些冲突。

然后输入指令：

`git push -u origin master -f`

---