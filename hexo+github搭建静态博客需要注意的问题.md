# hexo+github搭建静态博客需要注意的问题
[TOC]
#####遇到的问题
1. 创建了与用户名相同的repository，配置好了_config.yml中的deploy，但是username.github.io进不去网站。
2. 好不容易进去了username.github.io，页面上什么东西都没有。
3. localhost:4000访问不了。

##### 解决办法
> 当你在你的github上创建repository时，需要编写一个readme.md文件来初始化。然后将这个项目git clone到你本地之后，再进行npm install hexo等操作。（创建本地与远程的关系）
在github的repository中创建一个新分支，例如：hexo，将这个新分支作为默认分支。hexo放网站的原始文件。master放生成的html文件。
这样你就能进入网站username.github.io了。

> hexo deploy没反应。在_config.yml的deploy后面的type:冒号后面有空格，后面几个都是的。这样hexo deploy才会有效。看到的页面才不是什么东西都没有。

> localhost：4000访问不了。是你的hosts文件配置没设置好。把127.0.0.1映射到 localhost就可以了。



