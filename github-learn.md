## 关于github的使用

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
git commit -a -m "Add more"
git push
```
---
gihub内的菜单：

1. Fork:复制别人的仓库
2. Clone or download:通过命令复制仓库并下载到你的电脑文件夹内