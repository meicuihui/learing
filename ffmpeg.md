# ffmpeg在windows环境安装
* [下载地址](https://ffmpeg.zeranoe.com/builds/)
* 环境变量配置Path ffmpeg/bin
# 常见命令
### 视频截取
`ffmpeg -i in.mp4 -ss 00:00:10 -t 00:00:06 -acodec aac -vcodec h264 -strict -2 out.mp4`   
//从00:00:10开始，截取的长度为00:00:06
* 参数解释：  
-i  代表输入待处理的文件  
-ss 代表开始的时间   
-t 代表截取的长度  
-acodec 音频编解码器  
-vcodec 音频编解码器  
