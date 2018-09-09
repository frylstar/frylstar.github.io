---
title: Way_back_home
date: 2018-09-09 17:10:56
tags: 随笔
---

[TOC]

换电脑之后，接下来就在这儿记些东西放这儿吧~

### 一、安装必要软件

安装Git 以及 node JS

### 二、在 Github 网站上添加新电脑产生的秘钥（待补充...）

### 三、源文件拷贝

将你原来电脑上个人博客目录下的必要文件拷到你的新电脑上（比如G:/hexo_blog 目录下），注意无需全部拷贝，只拷如下几个目录：

```html
scaffolds
source
themes
_config.yml
package.json
```

### 四、安装 Hexo

在 cmd 下输入下面指令安装 hexo：

```html
npm install hexo-cli -g
```

### 五、进入 G:/hexo_blog 目录 （拷贝到的目录），输入下面指令安装相关模块

```
npm install
npm install hexo-deployer-git --save       // 文章部署到git的模块
//（下面为选择安装）
npm install hexo-generator-feed --save     // 建立RSS订阅
npm install hexo-generator-sitemap --save  // 建立站点地图
```

### 六、测试

`$ hexo server` 

启动服务器。默认情况下，访问网址为：http://localhost:4000/

| 选项          | 描述                           |
| ------------- | ------------------------------ |
| -p , --port   | 重设端口                       |
| -s , --static | 只使用静态文件                 |
| -l , --log    | 启动日记记录，使用覆盖记录格式 |

### 附录：Hexo 命令

### init

`$ hexo init [folder]`

新建一个网站。如果没有设置 folder , Hexo 默认在目前的文件夹建立网站

### new

`$ hexo new [layout] <title>`

新建一篇文章。如果没有设置 layout 的话，默认使用 _config.yml 中的 default_flayout 参数代替。如果标题包含空格的话，请使用引号括起来。

### generate

`$ hexo generate`

生成静态文件。该命令可简写为 `$ hexo g`

| 选项          | 描述                   |
| ------------- | ---------------------- |
| -d , --deploy | 文件生成后立即部署网站 |
| -w , --watch  | 监视文件变动           |

### publish

`$ hexo publish [layout] <filename>`

发表草稿

### deploy

`$ hexo deploy`

部署网站。该命令可以简写为：`$ hexo d`

| 参数            | 描述                     |
| --------------- | ------------------------ |
| -g , --generate | 部署之前预先生成静态文件 |

### render

`$ hexo render <file1> [file2] ...`

渲染文件。

| 参数          | 描述         |
| ------------- | ------------ |
| -o , --output | 设置输出路径 |

### migrate

`$ hexo migrate <type>`

从其他博客<u>迁移内容</u>

### clean

`$ hexo clean`

清除缓存文件( db.json )和已经生成的静态文件( public )。

在某些情况（尤其是更换主题后），如果发现您对站点的更改无论如何也不生效，您可能需要运行该命令。

### list

`$ hexo list <type>`

列出网站资料。

### version

`$ hexo version`

显示 Hexo 版本。

#### 其余参考 https://hexo.io/zh-cn/docs/commands