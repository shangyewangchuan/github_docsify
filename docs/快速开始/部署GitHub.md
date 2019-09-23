# 部署GitHub

?> 将`docsify`部署在GitHub上，既不用租用服务器，也不用担心维护的问题。

### 1.创建GitHub仓库

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

### 2.将本地仓库文件push到GitHub仓库

```bash
//切换到工作目录
$ cd [PATH]/docsify
//将工作区缓存提交到暂存区
$ git add .
//将暂存区缓存提交到主分支
$ git commit -m'change'
//添加远程Git仓库
$ git remote add docsify git@github.com:shangyewangchuan/docsify.git
//将本地文件推到远程仓库
$ git push docsify master
```

!> 前提： 已经设置了GitHub SSH秘钥！否则，无法提交。

!> 注意：后续提交需要在`push`操作之前先执行`$ git pull docsify master`，同步远程仓库到本地并合并，以防`push`失败。

### 3.开启GitHub Pages

   <center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/shangyewangchuan/material/master/img/github_3.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">进入仓库设置页面</div>
  </center>

<br>

   <center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="https://raw.githubusercontent.com/shangyewangchuan/material/master/img/github_4.png">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">设置master/docs开启GitHub Pages</div>
  </center>




?> 访问https://shangyewangchuan.github.io/github_docsify/ 即可食用！

!> 需要一段时间后`GitHub Pages`才可以正常解析
