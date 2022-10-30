# 恢复出厂设置后的配置过程

1. 修改 **设置向导**，配置ipv4地址，重新联接wifi

2. 修改 路由器登陆密码

3. 修改 挂载点 功能，把自动挂载功能全部打勾✔开启

4. 删除 LED配置 ，目的是关闭LAN和WAN指示灯

5. 打开 软件包 功能，下载luci-app-webdav和luci-app-samba4

6. 配置 阿里云盘webdav相关功能

7. 配置 网络共享smb的相关功能

   ```c++
   smbpasswd -a root    //添加root用户
   smbpasswd root      //修改root用户的密码
   
   
   smbpasswd -n root    //设置root用户的密码为空
   smbpasswd -x root   //删除root用户
   ```

   通过命令添加root用户后，即可正常登陆smb协议，共享文件。

8. 重启路由器
