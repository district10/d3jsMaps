Learning d3.js Mapping
======================

## Fix

I prefer local js file (the network sucks in china.), so...

```bash
perl -pi -e "s:http\://d3js\.org/topojson\.v1\.min\.js:../topojson.v1.min.js:" **/*.html
perl -pi -e "s:http\://d3js\.org/d3\.v3\.min\.js:d3.min.js:" **/*.html
rm **/*.bak
```

## koan

How could perl prevent us from editing a file inplace without a backup, I really need that.
Cause I can `git reset --hard HEAD` to revert. Not any backup protection needed.

## HTTP Server

many choices:

```bash
python -m SimpleHTTPServer 8888          # python 2
python -m http.server      8888          # python 3+
php -S localhost:8888                    # php
ruby -run -e httpd . -p 8888             # ruby
http-server                              # node.js: [c]npm install http-server -g
java -jar jetty-runner.jar --port 8888 . # java
```

downloads:

- [Windows: mongoose-free-5.5.exe (免安装，win binary)](http://whudoc.qiniudn.com/2016/mongoose-free-5.5.exe)
- [Java: jetty-runner](http://central.maven.org/maven2/org/eclipse/jetty/jetty-runner/9.3.0.M0/jetty-runner-9.3.0.M0.jar)
