
 
原GoIndex由于删裤所导致的已搭建GoIndex页面无法打开的解决方法：

登录CF，打开workers，选中项目，修改原代码部分替换成有效的

找到以下代码，我的是在21行

<script src="//cdn.jsdelivr.net/combine/gh/jquery/jquery@3.2/dist/jquery.min.js,gh/donwa/goindex@${authConfig.version}/themes/${authConfig.theme}/app.js"></script>

整行替换成下面（建议fork后替换成自己链接）

<script src="//cdn.jsdelivr.net/combine/gh/jquery/jquery@3.2/dist/jquery.min.js,gh/guxingjinguang/goindex/themes/${authConfig.theme}/app.js"></script>

GoIndex  
==== 
Google云端硬盘目录索引  
Combining the power of [Cloudflare Workers](https://workers.cloudflare.com/) and [Google Drive](https://www.google.com/drive/) will allow you to index you files on the browser on Cloudflare Workers.    

`index.js` is the content of the Workers script.  

## Demo  
material: [https://index.gd.workers.dev/](https://index.gd.workers.dev/)  
classic: [https://indexc.gd.workers.dev/](https://indexc.gd.workers.dev/)  

## Deployment  
1.Install `rclone` software locally  
2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  
3.Execute the command`rclone config file` to find the file `rclone.conf` path  
4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  
5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  
6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## Quick Deployment  
1.Open https://installen.gd.workers.dev/  
2.Auth and get the code  
3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  



## About  
Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  
