# aliyuan_sync
解决阿里云盘下载不完整问题，依赖aliyunpan-cli 


请先安装 https://github.com/wxy1343/aliyunpan

tag: 阿里云盘 下载 python3.7 php 


aliyunpan download  $path

下载命令也可以下载，但是速度较慢，可以通过以下命令来处理，前提是多数文件大于300字节


find $path -type f -size -1000c | xargs -n 1  -i aliyunpan d "{}"   "$path" 

下载受限制时，下载得到的是xml文件，大小为303字节。
通过查找小于1000字节的文件，提交给aliyunpan 可以实现再次下载。又不用全目录比对。
