# Dataset_website
> This is a website sharing the Quark links of the datasets.
### ***How to update the links***
> 先联系我给你添加权限
1. 确保你的电脑上安装了git（没装的话上网找一下教程），可以了解一下git的一些知识，大致就是我们共享的是一个远程仓库，你自己电脑上有个本地仓库。
2. 创建一个新的directory（name it website_datasets)
3. 在website_datasets这个directory新建一个终端。
```
> git init // 初始化本地仓库
> git remote add origin https://github.com/ICS-Datasets/website_datasets.git // 添加远程仓库
> git pull origin main // 拉取远程仓库的文件
// 终端一直开着，不用关了
```
4. 更新链接:在本地打开website_datasets/docs/dataset.md
> 因为本质上我们的这个网站就是一个个markdown文件组成的， 如何修改或者一些markdown语法可以上网查一下，这里就不赘述了。  

> 你可以看到```[babababab](*******)```这样的例子[]中放这个链接的名字（）放网站地址，你可以按照这个格式添加你的链接。

> 修改完记得保存
5. 把本地的修改提交到远程仓库
```
> git add . // 把所有修改的文件添加到暂存区
> git commit -m "update" // 提交到本地仓库，引号内写上你这次提交的说明
> git push origin main --force // 强制push到远程仓库
//不加force总会出现莫名其妙的不同步错误
//所以请确保每一次都只去修改相关的md文件，不要动其他的，也不要随意的push和pull
```
6. 等待一段时间，刷新一下网页，就可以看到你的链接了。
```
网页用了mkdocs框架，其实网页的更新过程都被省略了，我在.github/workflows/main.yml文件中已经写好了，只要push到远程仓库，就会自动更新网页。
```
之后你每次要更新时就在你创建的这个文件新建终端，然后请务必***pull***(不然的话push相当于直接把很大一部分旧的内容覆盖了现在的内容), 不需要再去初始化和远程连接了，只要修改相关的内容然后第4，5步就行了。
