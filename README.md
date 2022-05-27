# AdvIndex
基于 OneIndex 的 OneDrive 网页版，支持自定义域名，查看文件夹大小，配置缓存，上传文件

# 环境要求
|PHP 版本|5.5, 5.6, 7.x|
|---|---|
|PHP 扩展|curl|
|推荐使用|https|

# 安装
- 进入 [Releases](https://github.com/MBRjun/AdvIndex/releases/) 下载最新构建
- 解压到服务器，设置默认文档为 ``index.php``
- 打开网站，开始安装
- 后台默认密码：AdvIndex

# Nginx Rewrite
```php
if (!-f $request_filename){
	    set $rule_0 1$rule_0;
	}
	if (!-d $request_filename){
	    set $rule_0 2$rule_0;
	}
	if ($rule_0 = "21"){
	    rewrite ^/(.*) /?/$1 last;
	}
  ```
