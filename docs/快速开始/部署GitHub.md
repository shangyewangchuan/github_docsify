# 部署GitHub

?> 将`docsify`部署在GitHub上，既不用租用服务器，也不用担心维护的问题。

## 创建GitHub仓库

  <center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/shangyewangchuan/material/master/img/github_1.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">创建仓库</div>
 </center>

 <br>

   <center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/shangyewangchuan/material/master/img/github_2.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">复制Git SSH</div>
 </center>

## 将本地仓库文件push到GitHub仓库

```bash
//切换到工作目录
$ cd [PATH]/docsify
//将工作区缓存提交到暂存区
$ git add .
//将暂存区缓存提交到主分支
$ git commit -m'change'
//添加远程Git仓库
$ git remote add docsofy git@github.com:shangyewangchuan/docsify.git
//将本地文件推到远程仓库
$ git push docsofy master
```

## 开启GitHub Pages

