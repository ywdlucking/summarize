# 你不得不知道的linux命令
## 归档操作
* 解压tar  
**tar xvf test.tar**
* 查看tar  
**tar tvf test.tar**
* 解压*.gz  
**gzip -d test.txt.gz**
* 解压*.zip  
**unzip test.zip**

## 文件搜索
* 查找指定文件名的文件  
**find -inname "test.java"**
* 在文件中匹配查找字符串  
**grep -i "test" test.file**
* 在文件夹中递归查询包含指定字符串的文件  
**grep -r "test"**
* 显示文件大小（MB,GB...）  
**ls -lh**
* 显示最后修改时间  
**ls -ltr**

## 文本操作
* tail默认显示文件的最后10行文本  
**tail test.txt**
* 显示指定行数  
**tail -n N test,txt**
* 实时查看日志  
**tail -f log-file**

## SSH登录
* 登录到远程主机  
**ssh host.example.com**

## 授权操作
* 给指定文件的属主所有权限  
**chmod ug+rwx file.txt**
* 授权  
**chmod -R 777 file.txt**

## 系统操作
* 显示磁盘情况  
**df -k -h**
* 终止某进程  
**kill -9 12345**
* 查看当前运行的所有进程  
**ps -ef|more**
* 查看某进程  
**ps -ef|grep tomcat**
* 关机  
**shutdown -h now**
* 重启  
**shutdown -r now**

## 其他操作
* 输出跟字符串匹配的环境变量  
**export |grep JAVA_HOEM**
