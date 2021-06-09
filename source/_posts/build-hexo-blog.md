---
title: 从零开始搭建基于Hexo和Github的个人博客
date: 2021-06-06 05:34:36
tags: [hexo,博客搭建,教程]
---

<!-- toc -->

​                                                                 **最简洁的基于hexo+github搭建个人博客教程**

<!-- more -->



# 1. 环境准备

1.在本地[安装git](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)；在[github](https://github.com/)上新建一个仓库： **[username]** .github.io  //固定名，username必须用你在github上的**账户名**

2.安装nodejs，[安装教程](https://www.runoob.com/nodejs/nodejs-install-setup.html)

3.在node安装目录下使用npm安装hexo，输入:

   ```shell
   npm install -g hexo-cli
   ```

4.在node安装目录下使用npm安装远程部署插件 hexo-deployer-git，输入:

   ```shell
   npm install hexo-deployer-git --save
   ```


# 2. 创建博客

1.在本地选择一个目录作为父目录，如：D:\

2.在该目录打开cmd窗口，执行

   ```shell
   hexo init [blog] #blog为博客工程根目录，可自定义
   cd blog
   npm install
   ```

   

# <span id="jump">3. 运行博客(本地)</span>
1.执行以下生成及部署命令：

   ```shell
   hexo clean #清除缓存文件 (db.json) 和已生成的静态文件 (public)
   hexo g     #生成静态文件
   hexo s     #启动服务器。默认情况下，访问网址为： http://localhost:4000/
   ```

2.访问本地页面 http://localhost:4000/ 即可预览效果

<img src="/images/hexo_helloworld.png" alt="drawing" width="600" height="300"/>

# 4. 编写博客

1.执行新增博客记录命令：

```shell
hexo new myfirstblog   #新建一篇文章,生成source\_posts\myfirstblog.md
```

2.编辑myfirstblog.md并保存，重新[运行博客](#jump)即可预览效果

   *[markdown教程](https://www.runoob.com/markdown/md-tutorial.html)*

# 5. 部署博客(远程)
1.修改博客根目录下的_config.yml文件
![配置git项](/images/set_git_config.png)
*配置项要用自己的仓库地址和分支*
2.执行以下生成及部署命令：

   ```shell
   hexo clean #清除缓存文件 (db.json) 和已生成的静态文件 (public)
   hexo g     #生成静态文件
   hexo d     #上传github并部署到服务器
   ```

3.在浏览器输入网址：[username].github.io即可看到你的个人博客啦

# 6. 后记

看到此处你已经基于hexo搭建起了最基础的个人博客框架，至于更换主题及更多高级用法可自行探索。。。

[hexo官网](https://hexo.io/zh-cn/)

> *可爱的你可以带着收获悄悄地离去，亦或是留下几颗糖果哈哈哈！*


​    



   

