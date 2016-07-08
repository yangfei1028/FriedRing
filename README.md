#FriedRing
##基础
1、mitmproxy

2、multimechanize

3、requests

##安装mitmproxy和multimechanize
###Mac or Unbuntu
	pip install mitmproxy
	pip install -U multi-mechanize
	pip install requests
###Windows
	python -m pip install --upgrade pip(最支持版本8.1.2,多次运行可以升级到对应版本)
	python -m pip install netlib pyopenssl pyasn1 urwid pil lxml flask
	python -m pip install pyamf protobuf
	python -m pip install pil
	python -m pip install nose pathod countershape
	python -m pip install matplotlib
	python -m pip install mitmproxy
	pip install -U multi-mechanize
	pip install requests
##安装FiredRing



##使用FriedRing

首先，输入命令

	 python fr.py -p 8888 -w scriptsolution
	 
-p 端口号，-w 测试脚本文件夹

其次，在测试浏览器或者测试手机中设置代理（ip为运行主机ip，端口为888）
按照功能测试流程进行功能测试，在当前文件夹中会产生一个scriptsolition的文件夹，结构如下：
	
	scriptsolution/config.cfg(multimechan的配置文件）
	
	scriptsolution/test _ scripts/v_user.py（默认的初始化脚步）
	
	scriptsolution/test _ scripts/script.py（生成的测试脚步）

在录制完成后，需要修改scriptsolution/test _ scripts/script.py文件，去掉不属于本次测试的请求。

同时可以通过加入assert等信息做断言（详情可以参考requests包）



##运行脚本
###Mac or Unbuntu
在scriptsolution的父文件夹，执行

	multimech-run scriptsolution

###Windows

在scriptsolution的父文件夹，执行

	C:\FriedRing>python c:\Python27\Lib\site-packages\multimechanize\utilities\run.py scriptsolution
	
##查看结果
结果在scriptsolution文件夹下的results里面，按照时间顺序生产的文件夹，里面有一个result.html，用浏览器打开就可以看到结果信息了。