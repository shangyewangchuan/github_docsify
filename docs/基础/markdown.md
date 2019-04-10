# MarkDown

?> Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档，然后转换成格式丰富的HTML页面。

> ## MarkDown基本语法

- [Cmd Markdown 语法手册](https://www.zybuluo.com/mdeditor?url=https://www.zybuluo.com/static/editor/md-help.markdown)

> ## MarkDown扩展语法

- [docsify扩展语法](https://docsify.js.org/#/zh-cn/helpers)

> ## MarkDown Html语法

- 换行

```html
  <br></br>
```

- 文字居中

```html
  <center>居中文字</center>
```

- 图片居中+图片注释

```html
  <center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="这里输入图片地址">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">这里输入题注</div>
 </center>
```

> ## MarkDown缺点

!> MarkDown编写文档最大的缺点——`引入图片`

### MarkDown引入图片的三种方法

- 插入本地图片  
`![avatar](/home/picture/1.png)`
  - 不容易丢失图片
  - 插入截图困难
  - 网络共享困难
- 插入网络图片  
`![avatar]([/home/picture/1.png](http://baidu.com/pic/doge.png))`
  - 依赖图床提供图片服务
  - 上传繁琐，依赖插件
- 插入转码图片  
`![avatar](data:image/png;base64,iVBORw0......)`
  - 不依赖本地图片和网络图片
  - 插入截图困难
  - 图片base64转码后文本过长，图片大小约增加30%

### 图床网站

- 新浪图床
  - 免费畅用
  - 容易封图
- 七牛云图床
  - 限制收费
  - 国内主流
- Github
  - 免费畅用
  - 几无限制

!> 本文采用Github图床，配合PicGo图片上传助手。

!> 目前没有自动删除文章同时删除对应的图床图片的方案。
