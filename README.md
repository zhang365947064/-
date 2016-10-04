# server218
2016.09.30-2016.10.04：重装8服务器系统，并配置环境

以下是过程中遇到的问题，以及解决方法。

问题1：Ubuntum系统引导盘失败
解决1：换了另外一个软件制作引导盘

问题2：Ubuntum系统分区的问题
解决2：/boot    1G    ext4(选ext2格式会卡主)    主要是给引导单独分一个区，安全些
      /根目录   100G  ext4
      /tem      50G   ext4                     不单独分这个区的话，可能安装不了软件
      /home     other ext4
      /swap     内存的1~2倍，相当于虚拟内存
      
问题3：网络配置问题，插错网孔了，插进一个没有网卡的网孔
解决3：插进能用网孔，并配置IP-172.18.32.218 子网掩码-255.255.0.0 网关-172.18.32.254 DNS-192.168.153.3

问题4：更新软件源，选择最优的软件源，并进行更新和升级

问题5：驱动安装之后，重启进入登录界面后，输入密码一直循环
解决5：在BISO中，关掉secure boot(未验证？)

问题6：使用opencv显示图像一直提示Window system doesn't support OpenGL，困扰了1-2天！！！
解决6：OpenCV没有装好！！！！用215服务器上的opencv安装包的方式，成功安装opencv，并能使用！

问题7：matlab安装好后，打开就崩溃死掉，困扰了1天左右！！！！
解决7：安装网上找到的教程http://blog.csdn.net/he_mm/article/details/51920936成功解决

问题8：VNC一直没有界面
解决8：装vnc4server后，再装一个tightvncserver,两种界面都可以使用了，具体看教程
