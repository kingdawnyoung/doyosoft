---
title: 开启航空研发文档之旅
date: 2018/3/20 15:30+
categories: 
- 通用
tags:
- 通用
---

### 启动本地环境

```bash
npm install # 安装依赖
npm run start # 运行起来
```

### 文档书写


文档使用`markdown`语法书写，存放`./source/_posts`目录。文档编译使用的是`hexo`，提供了`Front-matter`等功能。

#### Front-matter

Front-matter 是文件最上方以 --- 分隔的区域，用于指定个别文件的变量，提供了文章标题，创建日期，分类等信息，举例来说：

```bash
---
title: Hello World
date: 2013/7/13 20:46:25
---
```

具体功能如下:

参数 | 描述 | 默认值
---|---|---
layout | 布局 |  &nbsp;
title |	标题 |  &nbsp;	
date |	建立日期 | 文件建立日期
updated | 更新日期 | 文件更新日期
comments | 开启文章的评论功能 | true
tags | 标签（不适用于分页）| &nbsp;
categories | 分类（不适用于分页）|	 &nbsp;
permalink | 覆盖文章网址 | &nbsp;


##### 分类和标签

```ymal
categories:
- 前端
- 基础
tags:
- nodejs
```

#### 资源

资源(Asset)表示除文章以为的内容，诸如图片，CSS，JS等文件。如果你的文章中需要插入图片最简单的方式是将他们放在`source/images`文件夹中，然后在文章中通过类似于`![](/images/image.jpg)`的方式访问它们。


### 构建

文档是通过`markdown`书写，如果要放到服务器需要先编译，生成到`public`文件夹

```bash
npm run build
```

### 部署
将`public`文件夹内所有文件拷贝到ftp

或者放到其他静态文件服务器

