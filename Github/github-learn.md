## 关于github的使用

[**github官方说明书**](https://git-scm.com/book/zh/v2)

**一、Gitbub新建仓库及版本提交步骤：**  
* **新建仓库：**
1. 确定本地文件目录；
2. 输入命令`git init`：初始化仓库（创建空的本地仓库）；
3. 输入命令`git status`：提交到本地暂存仓库（该命令要不断的使用）；
4. 输入命令`git add`：提交到版本控制管辖范围；
5. 输入命令`git commit`：提交版本（需要编写说明）;
6. 在github网站上新建仓库；
7. 关联本地仓库`git remote add origin https://github.com/hermanxie/刚才新建的仓库名.git`;  
8. 把本地仓库的内容推上github:`git push -u origin master`;


* **修改仓库：**  
1. `git add .`
2. `git commit -m "说明"`
2. `git push`  
*注：第1和2可以合并命令为：*`git commit -a -m "说明"`

* **建子仓库及上传文件：**  
1. 点击‘Create new file‘按钮，输入 *</文件夹名/文件名（任意一个临时文件名，比如temp）>*,确认;  
2. 进入子仓库，点击’Upload files'按钮，上传文件；

* **Gihub内的菜单：**

1. Fork: 复制别人的仓库到你的github内。
2. Clone or download: 通过命令复制仓库并下载到你的本地电脑文件夹内。

* **git其他常用命令：**  
`git restore --staged <你不想提交的文件名>`：把你**不想提交**的文件从暂时的版本控制仓库里拿出来；  
`git log`:查看提交记录；  
`git branch -a`: 查看'branchname'；  
`git --Force`: 查看隐藏文件'.git'文件；  


---
**二、Github解决异常：**

[**GitHub帮助查询**](https://help.github.com/cn/github)

**1. 问题一:**

***当输入`git push`后出现异常：***  
>! [rejected]        master -> master (non-fast-forward)  
error: failed to push some refs to 'ssh://git@*****.git'  
hint: Updates were rejected because the tip of your current branch is behind  
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.  
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

***解决办法一：***

出现**另外一个远程仓库地址**的情况下，报错：error: failed to push some refs to *'ssh://git@*****.git' * **(此处与想要上传的仓库地址不一样)** ,则采取以下解决方案：

1. 首先直接修改远程仓库地址，运行：`git remote set-url origin [url]`;  
2. 运行：`git fetch origin`,获取对在线存储库的更新;  
3. 运行：`git merge origin/`*YOUR_BRANCH_NAME*(一般名字是'master')  
*注：第2和3步可参照* [Github官方帮助](https://help.github.com/cn/github/using-git/dealing-with-non-fast-forward-errors)

***解决办法二（只能单次有效）：***

1. 修改指令：  
`git pull --rebase origin master`  
 查看是否有需要再进一步的commit一下，解决一些冲突。

2. 然后输入指令：  
`git push -u origin master -f`

***解决办法三：***   
1. 执行： `git pull origin master --allow-unrelated-histories` 把远程仓库和本地的仓库消除差异；  
2. 执行：`git pull origin master`；  
3. 执行：`git push origin master`。

***解决办法四：***

如果运行git status之后，出现：
>On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)
>
>Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   github-learn.md
>
>no changes added to commit (use "git add" and/or "git commit -a")

则运行：  
* `git rebase origin/master`然后：  
* `git pull --rebase`然后：  
* `git push origin master`

---