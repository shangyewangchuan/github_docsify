# docsify

?> docsify 是一个动态生成文档网站的工具。不同于 GitBook、Hexo 的地方是它不会生成将 `.md` 转成 `.html` 文件，所有转换工作都是在运行时进行。  ——[docsify中文文档](https://docsify.js.org/#/zh-cn/)

> ## 使用`docsify`

#### 1.安装 `docsify-cli` 工具

`$ npm i docsify-cli -g`

!> 安装过程很慢，建议开启代理加速

#### 2.Git 仓库初始化

```bash
$ mkdir base
$ cd base
$ git init docsify
```
- `.git` Git仓库核心文件
#### 3.初始化`docsify`项目

```bash
$ cd docsify
$ docsify init docs
```

- `index.html` 入口文件
- `README.md` 会做为主页内容渲染
- `.nojekyll` 用于阻止 GitHub Pages 会忽略掉下划线开头的文件

#### 4.本地预览

运行一个本地服务器通过 docsify serve 可以方便的预览效果，而且提供 LiveReload 功能，可以实时预览。默认访问 http://localhost:3000 。
<br></br>
`$ docsify serve docs &`

> ## `docsify设置`

### index.html设置

?> [具体设置参考官方文档](https://docsify.js.org/#/zh-cn/configuration)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <!-- docsify默认样式 -->
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/vue.css">
  <!-- Theme: Simple (latest v0.x.x) -->
  <!-- <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-defaults.css"> -->

</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      // 侧边栏标题
      name: 'Github+docsify',
      // 仓库地址
      repo: 'https://github.com/shangyewangchuan/github_docsify',
      // 主页设置
      homepage: '概览.md',
      // 启用侧边栏
      loadSidebar: true,
      // 侧边栏目录等级
      subMaxLevel: 3,
      // 启用封面
      coverpage: true,
      // 启用搜索
      search: 'auto',
      
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  <!-- 搜索 -->
  <script src="//unpkg.com/docsify/lib/plugins/search.min.js"></script>
  <!-- 图片放大 -->
  <script src="//unpkg.com/docsify/lib/plugins/zoom-image.js"></script>
  <!-- 复制代码 -->
  <script src="//unpkg.com/docsify-copy-code"></script>
  <!-- bash 代码高亮 -->
  <script src="//unpkg.com/prismjs/components/prism-bash.js"></script>
  <!-- git 代码高亮 -->
  <script src="//unpkg.com/prismjs/components/prism-git.js"></script>
  <!-- markdown 代码高亮 -->
  <script src="//unpkg.com/prismjs/components/prism-markdown.js"></script>"></script>
  <!-- docsify-themeable (latest v0.x.x) -->
  <!-- <script src="https://cdn.jsdelivr.net/npm/docsify-themeable@0"></script> -->
</body>
</html>
```

### _coverpage.md封面设置

```markdown
![logo](https://docsify.js.org/_media/icon.svg)

# docsify

> A magical documentation site generator.

* Simple and lightweight (~12kb gzipped)
* Multiple themes
* Not build static html files

[GitHub](https://github.com/docsifyjs/docsify/)
[Get Started](#quick-start)
```

### _sidebar.md侧边栏设置

```markdown
<!-- docs/_sidebar.md -->

* [概览](/)
* 基础
    * [Git](/基础/git.md)
    * [Markdown](/基础/markdown.md)
* 快速开始
    * [环境搭建](/快速开始/环境搭建.md)
    * [docsify](/快速开始/docsify.md)
```

### .nojekyll设置

!> 阻止 GitHub Pages 忽略下划线开头的文件

`_*.md`