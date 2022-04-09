## WebSSH

How  add to record video ?
use https://github.com/asciinema/asciinema-player/releases

asciinema


使用全局变量来做到这一需要 在安装目录webssh/main文件中修改

打开tornado.web代码

配置类中全局变量

RequestHandler类

添加全局三个类变量：hostname , username , now_time

给变量赋值（此时每次进入的uri都是只匹配一个url 包含 hostname的，而且全局变量在另外用户进入时不会重新创建不会影响到之前的用户）

在webnssh/work文件提取

__ini__() 方法定义初始变量

每次返回就实时写入

