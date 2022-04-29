1. 查看软件版本

```ssh
dnf install modules mysql-server
```

<img width="743" alt="image" src="https://user-images.githubusercontent.com/68862242/165985591-1050460b-8966-4c16-a92d-5c35f0bc5db0.png">

2. 安装软件

```ssh
dnf install mysql-server
```

<img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165985847-279aac02-f43a-4b24-98c0-09073bc5adee.png">

输入"y"确认安装

<img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165986100-4f19b488-4f05-4c81-b291-a263a500d252.png">

安装完成

3. 设置开机启动

```ssh
systemctl enable mysqld
```

<img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165986437-3de40756-0f1c-49a2-8757-4827199f7fe6.png">

4. 启动 MySQL

```ssh
systemctl start mysqld
```

<img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165986966-c65f7f9c-1b13-45c5-bfa4-5bd26aa669c9.png">

  查看是否启动成功
  
```ssh
systemctl status mysqld
```

<img width="745" alt="image" src="https://user-images.githubusercontent.com/68862242/165987277-dc28591b-a7eb-4c82-ba64-910057a93015.png">

出现"active(running)"字样表示启动成功

5. 修改默认密码
  - 进入MySQL
  ```ssh
  mysql -u root -p
  ```
  <img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165989475-f08ba9dc-8400-40da-9fd6-ba53ae847ff4.png">

   提示输入密码，首次登陆密码为空，直接回车进入。
   
   <img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165989683-d5f920e8-d3e6-46a4-a888-169b7611ad3d.png">

  - 更改密码
   
   ```ssh
   ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'yourpassword';
   ```
   
   <img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165990157-f109317f-cd1c-4033-b0a0-ac7c16becd04.png">

   <img width="744" alt="image" src="https://user-images.githubusercontent.com/68862242/165990299-b2c08cf7-d1ac-45b2-9f4b-8eedbeb08ff1.png">
