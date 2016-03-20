---
layout: post
title: windows 10 体验jekyll
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

状况一：
ERROR:  Could not find a valid gem 'jekyll' (>= 0), here is why:
          Unable to download data from https://rubygems.org/ - SSL_connect returned=1 errno=0 state=SSLv3 read server ce
rtificate B: certificate verify failed (https://rubygems.global.ssl.fastly.net/quick/Marshal.4.8/jekyll-1.3.0.gemspec.rz
)
ERROR:  Possible alternatives: jekyll
解决方法：
下载认证文件，
D:\Ruby200-x64>curl http://curl.haxx.se/ca/cacert.pem -o cacert.pem
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  223k  100  223k    0     0  82478      0  0:00:02  0:00:02 --:--:-- 94724
然后把生成在Ruby目录下的cacert.pem移动到里面的bin目录下

参考[在Windows中配置Jekyll  ](http://fangge-sun.blog.163.com/blog/static/4895625720142315473777/)

更多[build-blog-jekyll-github-pages](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)