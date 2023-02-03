## 下载
去GitHub下载对应你系统版本的ffmpeg，下载地址：https://github.com/BtbN/FFmpeg-Builds/releases  
这里我是windows 64位，就选择**ffmpeg-master-latest-win64-gpl.zip**  
解压到你想要存放的目录  
进入解压后的文件夹，单击bin文件夹，右键，复制文件地址

## 添加环境变量
Windows打开搜索，输入**编辑系统环境变量**，然后打开  
点击**环境变量**，在系统变量中找到**Path**，双击，然后点**新建**  
将刚刚复制的bin文件夹地址粘贴，**注意去掉地址的双引号**

## 运行
打开命令行（Windows搜索中输入cmd即可）  
首先确认环境变量是否添加成功，输入
```
ffmpeg
```
末尾出现*Use -h to get full help or, even better, run 'man ffmpeg'*，并且看不到报错即为正常  
如果提示“ffmpeg不是内部或外部命令，也不是可运行的程序”之类的，就是环境变量没有添加好  

运行命令
```
ffmpeg -i video.mp4 -i audio.mp4 -c:v copy -c:a aac -strict experimental output.mp4
```
其中`video.mp4`替换为你下载的vedio文件的位置，`audio.mp4`替换为你下载的audio文件的位置，`output.mp4`替换为你要输出的目录

## 检查
到你设置的输出目录检查一下生成的文件是否有问题
