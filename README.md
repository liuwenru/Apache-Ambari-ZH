# Apache-Ambari-ZH
当前Ambari的汉化版本为2.7.4.0.0,汉化采用对该版本的ambari源码直接修改的方式进行,如有翻译不当之处,请批评指正


使用方法如下：

message.js 因为ambari的前端是一个纯前端的工程，所以如果你要是想使用的话需要重新编译这个包去使用，在ambari-web上brunch build即可，然后把生成public文件夹覆盖到ambari-server的/usr/lib/ambari-server/web目录即可。
或者下载https://github.com/liuwenru/Apache-Ambari-ZH/releases/download/v0.1/public.tar.gz 直接使用
