1. 查看软件版本

```ssh
dnf module list php
```

<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/166270210-99361eed-0e4a-4819-ad65-2a357ba7cef3.png">

2. 选择安装7.4版本
3. 
```ssh
dnf module install php:7.4
```

<img width="765" alt="image" src="https://user-images.githubusercontent.com/68862242/166270531-5b54b36d-6497-4deb-9061-db65e51a88ae.png">

输入 "y" 确认安装

<img width="800" alt="image" src="https://user-images.githubusercontent.com/68862242/166271313-e8fcf862-cc31-4555-bc06-38b8a68ea87a.png">

安装完成

3. 设置开机启动
```ssh
systemctl enable php-fpm
```

<img width="800" alt="image" src="https://user-images.githubusercontent.com/68862242/166273751-b21755d0-adb2-4be3-9898-526b365d2300.png">

4. 启动软件

```ssh
systemctl start php-fpm
```

<img width="800" alt="image" src="https://user-images.githubusercontent.com/68862242/166276213-f67fdcc6-8f37-435f-b399-626de3ef9305.png">

查看是否启动成功

```ssh
systemctl status php-fpm
```

<img width="800" alt="image" src="https://user-images.githubusercontent.com/68862242/166278534-778a8536-5b23-405a-b484-341e5608d6c1.png">

5. 在Apache中设置支持PHP

```ssh
vim /etc/httpd/conf/httpd.conf
```


找到下面两行代码，并在后面加上AddType application/x-httpd-php .php
```
AddType application/x-compress .Z
AddType application/x-gzip .gz .tgz
```

6. 测试
在网站根目录下新建index.php文件文件内容如下：
```php
<?php
phpinfo()
?>
```
输入域名或IP地址出现php信息页面

<img width="1129" alt="image" src="https://user-images.githubusercontent.com/68862242/166291062-a86e8126-5d81-4cfc-a5fa-3c33e4a06408.png">

