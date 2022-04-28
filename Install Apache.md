1. 查看软件源中的版本
```ssh
dnf module list httpd
```
<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165781708-ed4e77b2-2fa8-4bbf-a936-7f355201c055.png">

2. 安装软件
```ssh
dnf install httpd
```
<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165782243-688a7ce9-5eee-4e8c-921c-84b66f08dc64.png">
输入"y“确定
<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165782850-6cd16244-ad22-49a3-8d6f-37a92e296d87.png">
出现"complete!"即安装完成

3. 设置开机启动
```ssh
systemctl enable httpd
```
<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165783679-8fc5558f-8963-4503-b42c-9914fcb7f842.png">
4. 启动

```ssh
systemctl start httpd
```
<img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165784457-d2fb933a-b941-4cd1-9c5b-b663d089c0b3.png">
5. 测试是否安装和启动成功
  打开浏览器，输入ip或域名
  <img width="569" alt="image" src="https://user-images.githubusercontent.com/68862242/165785016-7a746832-1bbc-4bd6-9438-1cde9063a120.png">
  出现类似界面表示成功安装和启动
