[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu) 

ngx_lua_waf改版基于原[ngx_lua_waf](https://github.com/loveshell/ngx_lua_waf)作者二次更改，代码很简单，高性能和轻量级。


**欢迎所有有兴趣的同学进行协同开发，在留言处@我**
=========================================================

## 【**】正在二次开发中的功能  
1、针对疑似机器人访问行为，浮层滑块验证，不再是单纯返回403，加入可以选功能图片验证码  
【Bug修复】  
 
  
## 【2020.07.X】 
1、更新白名单UA规则  
2、使用redis存储正常的白名单蜘蛛IP，减少网络查询。并提供了一些验证过的IP大致范围（PS后期自己更新）  
参考IP：  
  
    #http://hoohtml.com/tools/webspider/
    #http://www.so.com/help/spider_ip.html
  
插入redis命令：  
  
    lpush white_spider#Baiduspider 123.125.66.*
    lpush white_spider#Baiduspider 220.181.108.*
    lpush white_spider#Baiduspider 123.125.71.*
    lpush white_spider#Baiduspider 180.76.5.*
    lpush white_spider#Baiduspider 220.181.32.*
    lpush white_spider#Baiduspider 61.135.168.*
    lpush white_spider#Baiduspider 61.135.186.*
    lpush white_spider#Baiduspider 111.206.198.*
    lpush white_spider#Baiduspider 111.206.221.*
    lpush white_spider#Baiduspider 116.179.32.*

    lpush white_spider#Googlebot 203.208.60.*
    lpush white_spider#Googlebot 66.249.64.*
    lpush white_spider#Googlebot 66.249.65.*
    lpush white_spider#Googlebot 66.249.66.*
    lpush white_spider#Googlebot 66.249.68.*
    lpush white_spider#Googlebot 66.249.69.*
    lpush white_spider#Googlebot 66.249.70.*
    lpush white_spider#Googlebot 66.249.71.*
    lpush white_spider#Googlebot 66.249.72.*
    lpush white_spider#Googlebot 66.249.73.*
    lpush white_spider#Googlebot 66.249.75.*
    lpush white_spider#Googlebot 66.249.79.*
    
    lpush white_spider#Google-proxy 66.102.6.*
    lpush white_spider#Google-proxy 66.102.7.*
    lpush white_spider#Google-proxy 66.102.8.*
    lpush white_spider#Google-proxy 66.102.9.*
    
    lpush white_spider#Sogou 123.126.113.*
    lpush white_spider#Sogou 218.30.103.*
    lpush white_spider#Sogou 61.135.189.*
    lpush white_spider#Sogou 123.183.224.*
    
    lpush white_spider#YisouSpider 42.156.136.*
    lpush white_spider#YisouSpider 42.156.137.*
    lpush white_spider#YisouSpider 42.156.138.*
    lpush white_spider#YisouSpider 42.156.139.*
    lpush white_spider#YisouSpider 42.120.160.*
    lpush white_spider#YisouSpider 42.120.161.*
    lpush white_spider#YisouSpider 106.11.152.*
    lpush white_spider#YisouSpider 106.11.153.*
    lpush white_spider#YisouSpider 106.11.154.*
    lpush white_spider#YisouSpider 106.11.155.*
    lpush white_spider#YisouSpider 106.11.156.*
    lpush white_spider#YisouSpider 106.11.157.*
    lpush white_spider#YisouSpider 106.11.158.*
    lpush white_spider#YisouSpider 106.11.159.*
    lpush white_spider#YisouSpider 42.156.254.*
    lpush white_spider#YisouSpider 42.156.255.*
    
    lpush white_spider#bingbot 157.55.39.*
    lpush white_spider#bingbot 40.77.167.*
    lpush white_spider#bingbot 207.46.13.*
    lpush white_spider#bingbot 65.52.110.*
    
    lpush white_spider#Bytespider 111.225.149.*
    lpush white_spider#Bytespider 110.249.202.*
    lpush white_spider#Bytespider 110.249.201.*
    lpush white_spider#Bytespider 111.225.148.*
    lpush white_spider#Bytespider 220.243.135.*
    lpush white_spider#Bytespider 220.243.136.*
    lpush white_spider#Bytespider 60.8.123.*

    lpush white_spider#YoudaoBot 61.135.249.220

    lpush white_spider#PetalBot 114.119.160.*
    lpush white_spider#PetalBot 114.119.161.*
    lpush white_spider#PetalBot 114.119.162.*
    lpush white_spider#PetalBot 114.119.163.*
    lpush white_spider#PetalBot 114.119.164.*
    lpush white_spider#PetalBot 114.119.165.*
    lpush white_spider#PetalBot 114.119.166.*
    lpush white_spider#PetalBot 114.119.167.*
    
    lpush white_spider#360Spider 180.153.232.*
    lpush white_spider#360Spider 180.153.234.*
    lpush white_spider#360Spider 180.153.236.*
    lpush white_spider#360Spider 180.163.220.*
    lpush white_spider#360Spider 42.236.101.*
    lpush white_spider#360Spider 42.236.102.*
    lpush white_spider#360Spider 42.236.103.*
    lpush white_spider#360Spider 42.236.10.*
    lpush white_spider#360Spider 42.236.12.*
    lpush white_spider#360Spider 42.236.13.*
    lpush white_spider#360Spider 42.236.14.*
    lpush white_spider#360Spider 42.236.15.*
    lpush white_spider#360Spider 42.236.16.*
    lpush white_spider#360Spider 42.236.17.*
    lpush white_spider#360Spider 42.236.46.*
    lpush white_spider#360Spider 42.236.48.*
    lpush white_spider#360Spider 42.236.49.*
    lpush white_spider#360Spider 42.236.50.*
    lpush white_spider#360Spider 42.236.51.*
    lpush white_spider#360Spider 42.236.52.*
    lpush white_spider#360Spider 42.236.53.*
    lpush white_spider#360Spider 42.236.54.*
    lpush white_spider#360Spider 42.236.55.*
    lpush white_spider#360Spider 42.236.99.*
  
  
  
## 【2020.07.14】 
1、使用redis存储CC攻击时的统计数据  
2、使用redis存储攻击日记统计数据，应对大日志（超过1G）分析过慢及CPU负载较高  
3、使用redis记录攻击重点的客户端IP，统计分析展现  
4、新增url访问配置文件保护规则，参考  
https://github.com/SpiderLabs/owasp-modsecurity-crs/blob/v3.3/dev/rules/restricted-files.data  
5、新增UA限制规则，参考  https://github.com/SpiderLabs/owasp-modsecurity-crs/blob/v3.3/dev/rules/scanners-user-agents.data  
和 https://github.com/SpiderLabs/owasp-modsecurity-crs/blob/v3.3/dev/rules/scripting-user-agents.data  
6、新增GET/POST参数个数限制，以防溢出攻击（ps：默认最大是100个）  
**【Bug修复】**   
1、修复手机号码正则表达式不准确问题  
2、openresty的unescape_uri函数处理百分号 ，参考：https://www.cnxct.com/openresty-unescape_uri-feature-to-decode-char-after-percent-sign/解决： 你自己修改后重新编译  
3、调整国家限制功能位置，不能放在最后。同时mmdb数据库应该填写完整路径。   
【效果展示】  
![image](https://raw.githubusercontent.com/wiki/w38351479/ngx_lua_waf/waf01.png)   
![image](https://raw.githubusercontent.com/wiki/w38351479/ngx_lua_waf/waf02.png)   
  
  
## 【2020.07.06】 
1、添加user-agent规则。支持如wordpress/pingback等常见CC变种型攻击防护  
2、头部字段Referer限制，防止恶意请求或防盗链  
3、HTTP/HTTPS协议请求方法限制（限制TRACE/TRACK/OPTIONS/PUT/PATCH/DELETE/CONNECT）,不允许未知方法或空  
4、防信息泄露：支持数据脱敏（身份证、手机号）,参考某云平台WAF的  
5、针对特殊URL进行独立限速，主要针对短信接口等非页面URL    
6、针对白名单的蜘蛛，进行蜘蛛验证  
7、优化日志记录  
8、基于日志服务，提供全量访问日志的攻击比例分析   
9、根据连续异常响应码分布，限制IP访问（拦截黑客针对不存在的URL地址发起的大量恶意访问）  
10、HTTP慢速攻击  
11、添加X-Forwarded-For黑名单，主要防护127.0.0.1等，绕过waf   
**【Bug修复】**  
1、修复User-agent为空时直接绕过UA规则检查。要求强制有UA才可以访问  
2、取消#77 bug修复，因为可能引起攻击崩溃。同时“针对特殊URL进行独立限速”功能已经基本满足  
3、修复获取客户端IP，XFF多级时返回异常  
  
  
## 【2020.06.22】Bug修复，适用于此日期前的所有版本 
1.自己的bug。  
* 描述：针对开启国家地域黑白名单时，出现内网或无法解析的IP采取直接放行，导致后面的规则不生效。  
解决办法：  
  规则优先级应该放在最后    
  
问题来源： https://github.com/loveshell/ngx_lua_waf/issues  
2、waf 记录日志的bug及修复 #129：
* 描述：当nginx 同一个server段的server_name 的list里有多个servername时，log函数只会匹配到第一个servername。并且，如果servername 出现通配符时，log函数会按照原样打入log。  
解决办法（采纳意见）：  
  ngx.var.server_name  
  --改为  
  ngx.var.host  
  
3、正则表达式有问题 #149  或   使用了ngx_lua_waf这个模块后，页面上传超过256M的文件，nginx会报400的错误。请问ngx_lua_waf对文件上传限制在哪儿进行修改？ #123
* 描述：POST匹配文件的表达式中表达式有误，看了很多这个项目的小伙伴后觉得还是不对 
  此处涉及多处修改和逻辑修改  
  
4、通过URL传参时容易造成CC攻击误报  
* 描述：有些架构都需要访问index.php?id=xxx,具体资源有id来指定，那么index.php这个页面容易触发cc规则访问被deny，这样会造成大量的误报，有什么办法解决这个问题吗？ #77  
解决办法：  
  生成token时引入ngx.var.request_uri而不是单纯的uri，并且使用url安全的进行encode_base64url 数据编码方式   
  
5、上传zip文件被post规则匹配到，导致403 #130  
* 描述：原因是 被 post 里面的 匹配到疑似攻击内容  
解决办法：  
  对上传文件新增独立检查开关，而不是直接关闭post检查   
  
6、发现用了waf开启Post功能，上传图片大的会上传不了，请问哪里取消图片容量限制？ #115  
* 描述：原因是应该是nginx允许上传的参数不够大  
解决办法： 
  调整您配置的两个参数，参数含义自己查，生产建议不高于100m。  
  client_body_buffer_size 5m;  
  client_max_body_size 512m;  
  
其他自己发现的bug  
7、匹配文件后缀时，采用match导致部分匹配，误拒绝POST上传  
  if ngx.re.match(ext,rule,"isjo") then  
  --改为  
  if string.lower(rule) == ext then  
  
8、上传文件时，上传js,py,html文件时日志变为cat文件，优化记录日记和错误拦截  
  log("-","file attack with ext "..ext .. " rule: " .. rule)  
  --改为  
  log("-","file attack with ext. rule: " .. rule)   
  --还有log函数，略..。  
  
**【新增功能】**  
1、post文件上传时单独对文件内容检查设置一个小开关  
2、上传文件的后缀黑名单改为允许上传的后缀白名单（因为未知的文件后缀数量太多，而且具有不确定性），并且对文件没有后缀的跳过次检查（ps你也可以强制改为必须有后缀，但感觉意义不大）  
3、对上传成功的文件和，上传失败的，单独记录日志，便于查找  
**【修改nginx配置lua环境参数】**  
    lua_package_path  "/usr/local/openresty/nginx/conf/waf/?.lua;;";  
    lua_package_cpath  "/usr/local/openresty/lualib/?.so;;";  
    lua_shared_dict urllimit 10m;  
    lua_shared_dict iplimit 10m;  
    init_by_lua_file   /usr/local/openresty/nginx/conf/waf/init.lua;  
    access_by_lua_file /usr/local/openresty/nginx/conf/waf/waf.lua;   
  
  
  
  
## 【2020.06.19】  
1、国家级别的地域限制（黑白名单）。国家代码参考[ISO_3166-2](https://en.wikipedia.org/wiki/ISO_3166-2)。"GeoLite2-City.mmdb/GeoLite2-Country.mmdb"后期请自行更新  


## 【2020.06.18】  
1、获取客户端IP，支持代理，多级代理情况下只取最后一级  
2、修改原来单一针对IP做cc检测。添加URL频率cc攻击检测，其次才是Ip 频率cc攻击检测（需要修改nginx配置，lua_shared_dict部分）  
3、优化局部变量，减少高并发时变量覆盖  
4、优化日志记录提醒  
5、优化规则执行顺序  


## 【2020.06.17】  
1、增加黑白名单IP段掩码限制方法，例如：ipWhitelist={"127.0.0.1","192.168.1.0/24"}



## 【别人的】增加功能如下  
1、增加黑白名单网段IP限制，例如：ipWhitelist={"127.0.0.1","172.16.1.0-172.16.1.255"}  
2、增加User-Agent白名单，用来过滤蜘蛛的。在wafconf文件夹下white-user-agent文件中添加  
3、增加server_name白名单。  




### 初始功能：

	防止sql注入，本地包含，部分溢出，fuzzing测试，xss,SSRF等web攻击
	防止svn/备份之类文件泄漏
	防止ApacheBench之类压力测试工具的攻击
	屏蔽常见的扫描黑客工具，扫描器
	屏蔽异常的网络请求
	屏蔽图片附件类目录php执行权限
	防止webshell上传


  
  
  
  
  
## 【安装】	 
### 【1】环境推荐安装:  
1.1）推荐使用lujit2.1做lua支持  
1.2）ngx_lua如果是0.9.2以上版本，建议正则过滤函数改为ngx.re.find，匹配效率会提高三倍左右。  
1.3）推荐直接使用openresty部署，而不是自己手动部署nginx+lua，下面安装示例使用“openresty/1.15.8.3”  
1.4）推荐编译安装openresty时添加后端检查模块 “[--add-module=../nginx_upstream_check_module](https://github.com/yaoweibin/nginx_upstream_check_module)”,并添加模块参数“--add-module=../ngx_http_geoip2_module”(https://github.com/leev/ngx_http_geoip2_module)  


### 【2】安装使用说明：  
openresty安装路径假设为: /usr/local/openresty  
2.1）下载文件：  
* 把ngx_lua_waf下载到/usr/local/openresty/nginx/conf/目录下,解压命名为waf  
* 确保lua_package_cpath配置中包含cjson.so（openrestym默认包含）  

2.1.1）安装lua 库依赖 libmaxminddb 实现对 mmdb 的高效访问  (使用yum安装的，版本较低。yum install libmaxminddb-devel -y)

    wget https://github.com/maxmind/libmaxminddb/releases/download/1.4.2/libmaxminddb-1.4.2.tar.gz
    tar -zxvf libmaxminddb-1.4.2.tar.gz
    cd libmaxminddb-1.4.2
    ./configure
    make
    make check
    sudo make install
    echo /usr/local/lib  >> /etc/ld.so.conf.d/local.conf
    sudo ldconfig  

2.1.2) 安装gd.so依赖

    复制gd.so依赖到 /usr/local/openresty/lualib    
    
2.1.3) 安装lfs.so依赖
    
    git clone https://github.com/keplerproject/luafilesystem.git  
    cd luafilesystem  
    make LUA_INC='-I/usr/local/openresty/luajit/include/luajit-2.1'  
    make install  
    cp src/lfs.so /usr/local/openresty/lualib/  
    
    
2.2）在nginx.conf的http段添加  

    lua_package_path  "/usr/local/openresty/nginx/conf/waf/?.lua;;";  
    lua_package_cpath  "/usr/local/openresty/lualib/?.so;;";  
    lua_shared_dict urllimit 10m;  
    lua_shared_dict iplimit 10m;  
    lua_shared_dict checkcode 1m;  
    lua_shared_dict respstatus 3m;  
    init_by_lua_file   /usr/local/openresty/nginx/conf/waf/init.lua;  
    access_by_lua_file /usr/local/openresty/nginx/conf/waf/waf.lua;  
    header_filter_by_lua_file /usr/local/openresty/nginx/conf/waf/response_header_waf.lua;  
    body_filter_by_lua_file /usr/local/openresty/nginx/conf/waf/response_body_waf.lua;  
    log_by_lua_file  /usr/local/openresty/nginx/conf/waf/log_waf.lua;  

其次添加管理端访问，并限制源  

    server {
        listen       8110;
        server_name_in_redirect off;
        location /waf_analysis {
            default_type text/html;
            content_by_lua_file /usr/local/openresty/nginx/conf/waf/analysis_log.lua;
            allow 192.168.0.0/16;
            allow 172.16.0.0/12;
            allow 10.0.0.0/8;
            allow 127.0.0.1;
            deny all;
        }
    }  
    
    
2.3）配置config.lua里的waf规则目录

    RulePath = "/usr/local/openresty/nginx/conf/waf/wafconf/"

路径如有变动，需对应修改，然后重启nginx即可  
2.4）配置config.lua里的日志目录(该目录需要自己提前创建)  

    logdir = "/usr/local/openresty/nginx/waflogs/"

2.5）配置文件详细说明：  

	其他参数说明直接卸载配置文件中了  
		
### 【3】检查规则是否生效  
部署完毕可以尝试如下命令：

        curl http://xxxx/test.php?id=/etc/passwd
        返回"Please go away~~"字样，说明规则生效。
		
注意:默认，本机在白名单不过滤，可自行调整config.lua配置





## 【特别说明】  
以上代码参考以下项目：  
> https://github.com/loveshell/ngx_lua_waf  
> https://github.com/whsir/ngx_lua_waf  
> https://github.com/oneinstack/ngx_lua_waf  
> https://github.com/taihedeveloper/ngx_lua_waf  
感谢ngx_lua模块的开发者，感谢openresty的春哥！！！  


## 【其他资源说明】  
* [GeoLite2-City.mmdb/GeoLite2-Country.mmdb](https://dev.maxmind.com/geoip/geoip2/geolite2/)  
* [maxminddb.lua](https://dev.maxmind.com/geoip/geoip2/downloadable/#MaxMind_APIs)  
* [libmaxminddb](https://github.com/maxmind/libmaxminddb/releases)  
