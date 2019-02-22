<p align="center"><img src="https://redis.io/images/redis-white.png"></p>

## Window 下安装Redis

[安装文档](http://www.runoob.com/redis/redis-install.html)

## PHP扩展安装

- 下载 php_redis.dll扩展包，[下载地址](https://windows.php.net/downloads/pecl/releases/redis/)
-  用phpinfo 查看到时TS vc9。那么下载的版本就对应好

<p><img src="https://github.com/amoswdh/Redis-Help/blob/redis-windows-install/example/12123134-109e384e6e4c48419bf7d9354b301400.png"></p>

- 修改php.ini文件。加入extension 扩展

``` shell
extension=php_redis.dll
```

- 重启服务器(apache/nginx) ，查看phpinfo 界面。如下则表示安装成功

<p><img src="https://github.com/amoswdh/Redis-Help/blob/redis-windows-install/example/12124001-7113248b3c474c7fbfbff299f40e5b6e.png"></p>

- 开始使用你的Redis

``` shell
<?php
     $redis = new Redis();                   //redis对象
     $redis->connect("192.168.60.6","6379"); //连接redis服务器
     $redis->set("test","Hello World");      //set字符串值
     echo $redis->get("test");               //获取值
?>
```