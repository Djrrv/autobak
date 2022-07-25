# autobak
autobak，自动备份加密文件，保护文件安全\
## 简介
DiskDriveAutoBackups，缩写DDAB，简称autobak（以下简称为“本软件”或“本程序”或“此软件”或“此程序”）\
亮点：全自动备份，隐藏窗口执行，中美国防部文件加密标准AES-256，极长密钥，设备序列号、管理员授权INF文件双重验证，随机文件名\
自动寻找可移动存储设备（不包括移动硬盘），将指定文件或关键词文件或所有文件加密存储到指定目录，并将加密后的文件移动到管理员的可移动存储设备（包括移动硬盘）中的指定目录，然后随机重命名，删除前面的备份。\
## 协议
此软件受到该软件受国际版权法和国际公约，《中华人民共和国著作权法》《中华人民共和国计算机软件保护条例》《美利坚合众国版权法》保护，作者拥有对任何用户的许可权力，任何人使用、试用都应得到作者的许可并且颁发许可证，任何人使用或试用都应当遵守当地相关规定，任何侵权行为将承受最严厉的民事和刑事处罚，对已知的违法者将给予法律范围内的全面制裁\
### 规避审查
为了规避审查，本软件许可任何人对程序的文件名称、文件版权信息进行任何修改，但是不得进行其他未许可的逆向\
例如：DriveShadow,DiskCopy,Copy Right GFW LLC.\
## 源码相关
autobak.exe ： autobak主程序，不包括进程保护，可以单独放到任意目录直接运行\
autobak.bat ： 主程序源码\
Rar.exe ： winrar的命令行版本，autobak使用它用于加密和拷贝\
recopy.exe ： autobak使用它，是将加密后文件随机重命名并且更改存放目录的程序\
recopy.bat ： recopy.exe的源码\
编译autobak.bat，并且保证由autobak.bat编译出的autobak.exe在运行时会自动释放出Rar.exe和recopy.exe到运行目录下\
在源码autobak.bat中，用户需要填入自己的可移动存储设备序列号；设置加密密码，以及用来二次识别管理员的可移动存储设备的key（密钥）\
管理员在自己的可移动存储设备根目录下创建文件“admin.inf”，格式如下：\
[admin]\
username: FangBinxing\
key: Great_Firewall\
===========\
[admin]和username后面的随便写，key后面的就是二次识别使用的密钥，冒号后面有空格\
## 安装

## 历代更新
### 1.x版本
#### 1.0
第一个测试版本，bug很多，只能备份 根目录下文件
#### 1.1
增加进程保护
### 2.x版本
#### 2.0
增加关键词
### 3.x版本
#### 3.0
增加关键词，启动项防护，注册表防护，进程ID重置
#### 3.1
增加文件强制隐藏
### 4.x版本
#### 4.0
增加管理员序列号检测、授权文件检测、句柄占用、文件夹fake隐藏、使用中美国防部基于AES-256的加密算法
#### 4.1
加长密码长度
