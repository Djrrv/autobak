# autobak
autobak，自动备份加密文件，保护文件安全\
自动寻找可移动存储设备（不包括移动硬盘），将指定文件或关键词文件或所有文件加密存储到指定目录，并将加密后的文件移动到管理员的可移动存储设备（包括移动硬盘）中的指定目录，然后随机重命名，删除前面的备份。\
autobak.exe ： autobak主程序，不包括进程保护，可以单独放到任意目录直接运行\
autobak.bat ： 主程序源码\
Rar.exe ： winrar的命令行版本，autobak使用它用于加密和拷贝\
recopy.exe ： autobak使用它，是将加密后文件随机重命名并且更改存放目录的程序\
recopy.bat ： recopy.exe的源码\
编译autobak.bat，并且保证由autobak.bat编译出的autobak.exe在运行时会自动释放出Rar.exe和recopy.exe到运行目录下\
在源码autobak.bat中，没有填入管理员的可移动存储设备硬件序列号和加密密码，将所有“你的序列号”替换成你的可移动存储设备序列号；将所有“密钥”改成密码，其中“-hp[密钥]”是加密的密码，包含中括号，“ find /n F:\admin.inf "密钥" ” 中的“密钥”是用来二次识别管理员的可移动存储设备的key（密钥）\
管理员在自己的可移动存储设备根目录下创建文件“admin.inf”，格式如下：\
[admin]\
username: FangBinxing\
key: Great_Firewall\
===========\
[admin]和username后面的随便写，key后面的就是二次识别使用的密钥，冒号后面有空格\
