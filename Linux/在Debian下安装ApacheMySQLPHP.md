# 在 Debian 下安装 Apache,MySQL,PHP
安装环境：Debian7 64位

## 首先，对你的源进行更新：

```php
$ sudo apt-get update
```
## 第一步 安装 Apache
Apache 是一个开源软件，它目前运行在全球超过 50% 的服务器上，是 LAMP(Linux,Apache,MySQL,PHP)组成部分之一。
安装 Apache：


    $ sudo apt-get install apache2


 安装完成后可以在浏览器地址栏输入 http://localhost/，安装成功会有一个 It works 页面。
可以通过以下命令找到你的服务器的 IP 地址：


    $ sudo ifconfig eth0 | grep inet | awk '{ print $2 }'


## 第二步：安装php7
apt install php(默认是版本7)
![安装php](https://vnote.oss-cn-beijing.aliyuncs.com/2019519136.png)

## 第三步-安装数据库
    原来在 Debian 9 中，Mysql 已经被替换成了 MariaDB，所以和传统的安装 Mysql 有一些不一样的地方。

## 安装方法
>首先我们还是可以用 sudo apt install mysql-server 这样安装上的
>但是安装上的还是 MariaDB
>所以最好还是采用 sudo apt install mariadb-server。
>安装上之后，发现和传统的不一样，因为没有弹出设置密码的那个蓝色的界面，误以为直接可以空密码登录。直接尝试 mysql -uroot -p，发现 ERROR 1698 (28000): Access denied for user 'root'@'localhost'。难道默认密码不是空。查看 /etc/mysql/debian.cnf 中默认密码确实是空。

>第一反应是执行 mysqld_safe skip-grant-tables，然后 use mysql; ，然后 update user set password=PASSWORD('mysql') where User='root'; 。这样确实可以解决问题，但是重启之后莫名发现又登录不了了。

>懵逼一段时间后发现 MaraiDB 的默认密码确实是空，但是只能用 Root 用户登录注意：这里的用户说的是 linux 系统的 Root 用户，也就是说，你 sudo su 进入 Root 终端后，是可以正常登录的，但是普通用户却无法登录。（为了区别一下，我把 Root 终端的首字母大写，而 mysql 的 root 用户首字母小写）

>大概明白了，所以我们不能图方便一直使用 root 用户了，正确的姿势应该是这样的：
>首先是 `sudo apt install mariadb-server`安装上数据库。
>然后 sudo su 切换至 Root 终端，通过 mariadb -uroot -p 登录到数据库，如果默认密码不是空的话，可以查看 '/etc/mysql/debian.cnf'。
>这时候要做的是创建新用户：create user 'admin'@'localhost' identified by 'mysql'。
>然后给新用户设置权限：grant all on *.* to 'admin'@'localhost'。
>好了，我们又设置了一个方便的 "Root" 用户，只不过改了名字叫做 admin。
PS：我发现在 Root 终端中，不管密码输入什么都能正常连接数据库...晕。

## 总结
>以上就是这篇文章的全部内容，希望本文的内容对大家的学习或者工作具有一定的参考学习价值，如果有疑问大家可以留言交流，谢谢大家对脚本之家的支持。
>以上是互联网用户为您的的内容，在阿里云内部有更多的关于在Debian 9系统上安装Mysql数据库的方法教程_Mysql的内容，欢迎继续使用右上角搜索按钮进行搜索debian9、安装mysql、debian9下安装mysql、debian安装mysql、以便于您获取更多的相关信息。

![安装信息](https://vnote.oss-cn-beijing.aliyuncs.com/2019519130.png)
