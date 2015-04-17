#工作日志-by Ailn
##2015-04-07
	熟悉了OSX操作系统
	单指滑动移动光标
	双指滑动移动滚动条
	三指滑动移动窗体、选框
	四指横向滑动全屏程序切换
	全屏状态下四指向上全屏程序缩小到上方，向下则返回全屏
	cmd+control+f最大化 还原当前窗口
	cmd+m最小化当前窗口
	cmd+delete删除选中项目 
	cmd+space切换输入法
	cmd+w关闭当前窗口
	列出目录ls path
	移动工作目录cd path
	brew的安装使用
	brew serach /package/
	brew install package
	brew uninstall package
	brew info package
	OSX下nginx的安装与配置
	OSX下python的安装配置
##2015-04-08
	cmd+shift+4全屏幕截图
	继续学习nginx服务器
	vi编辑器的使用
	curl http://www.baidu.com 访问某网站
	学习了OSX下git的使用
	git clone url
	git add filename
	git commit
	git push
	学习了markdown语法
##2015-04-09
	查看本地网络信息ifconfig
	学习了flask框架
	学习了jinja2模板引擎 
	新建文件夹mkdir dicname
	前往->实用工具->钥匙串访问  可以查看本机存储的密码
	四指收缩可打开app列表 四指张开返回
	git clone https://github.com/laoqiu/pypress.git学习此代码
	学习postgresql数据库
	cmd+t打开一个新窗口
##2015-04-10
	安装python redis 组件 sudo pip install redis
	安装python postgressql 组件 sudo pip install psycopg2
###python语法
	python 行尾 \可以将一行代码写在两行上，python解释器仍然认为一行
	#python单行注释
	“”
	python多行注释
	“”
	python locals() globals() 获取局部 全局变量
	#################################################################
	python __import__(name,globals={},locals={},fromlist=[],level=-1）用来导入多个模块
		name:包名 字符串
		globals:全局变量 字典
		locals:局部变量 字典
		fromlist:模块列表 列表
		level:
	#################################################################
	python getattr(object,name)	获取对象属性object.name
	python '''abc"""'''三个‘或者单个“可表示真实字符串所见即所得
	
###Flask
	创建一个Flask应用app = Flask(__name__)
	从对象加载Flask.config Flask.config.from_object(object)
	from_envvar(variable_name, silent=False)从一个环境变量加载Flask.config
	export variable name='/path/to/config/file'//从文件加载环境变量
	@app.errorhandler(http error code)定义错误处理
	@app.context_processor环境处理器将自定义看书注册到模板中
	@app.template_filter()过滤器
	app.register_blueprint()将视图对应到处理函数
##2015-04-13
	Osx 系统安装U盘制作
	安装Osx系统
##2015-04-14
	重新搭建开发环境
	brew nginx
	pip install Flask
	下载安装PostgreSql9.3.6
	brew install redis
	sudo pip install redis
	*psycopg2 安装后导入 openssl 出错
	*替换/usr/lib 中的两个文件
	*Symbol not found: _lo_lseek64 错误
	以上*参考链接http://stackoverflow.com/questions/28515972/problems-using-psycopg2-on-mac-os-yosemite
	lsof -i:8080 查看某端口的信息
	python @property 把方法当做属性
	netstat -nat 查看TCP/UDP连接信息
###安装Flask所需python插件
	flask-sqlalchemy 数据库ORM:sudo pip install flask-sqlalchemy
	jinja2 html模板引擎 已经安装如需：pip install jinja2
	Flask-WTF表单验证插件：sudo pip install Flask-WTF
	flask-login登陆验证控件：sudo pip install flask-login
	Flash-Cache安装：sudo pip install Flask-Cache
##2015-04-15
	raise python中引发异常
###SQLAlchemy
	SQLAlchemy是python下得一个orm框架	
	model
	class type(base):
		__tablename__=tablename
		column= Column(datatype,...)
		def funcname():
			pass
	query
	user.query.filter_by(name=name)
	insert
	#create session
	session.add(user)
	session.commit()
	session.close()
###WTForms
	wtforms 是Python下得一个表单框架
	class FormName(base):
		fieldname=FieldType()
	def validata_fieldname(self,field):
		#check
		raise validators.ValidationError(errormessage)
#总结
	至此，基本熟悉了osx 下的python flask web 框架开发,主要掌握了
	1.osx 终端下的 软件管理器 brew
	2.python 包管理器pip的安装与使用
	3.基本了解了flask框架
	4.了解并安装了PostgreSql 以及postgresql python 接口 psycopg2
	5.了解并安装了no sql redis 以及python redis
	6.了解其他的一些python web 包与框架，wtforms(表单)jinja2(模板渲染引擎) SQLAlchemy（数据库ORM框架）
	7.git 的简单使用
	8.nginx的安装与简单配置
	9.osx 系统的重装与基本操作	
##2015-04-16
	""" """python多行注释
	class(base): python 继承
	学习Werkzeug
	学习gevent.wsgi
	python {key:value}字典无序的k、v集合
	python {}.get(k,d)如果字典中存在键K则list[k]否则返回d
	python 
	[]列表 有序序列
	()元组 有序不可变序列
	{}字典无序集合
	初步了解了协程的概念
##2015-04-17
	git branch dev 创建dev分支
	git checkout dev 切换都分支dev
	git checkout -b dev 创建并切换到分支dev
	git branch 列出所有分支当前分支前有*
	git merge dev 合并dev分支到当前分支
	git branch -d dev 删除分支dev
	git init 在当前目录创建本地仓库
	git status 显示git状态
	git reset --hard 版本id 回退或回到将来到某个版本
	git reset --hard HEAD^ 回退到上一个版本
	git reset --hard HEAD^^回退到上两个版本
	git reset --hard HEAD~100回退到上100个版本
	git diff HEAD --readme.txt 查看 readme 工作区合版本库 最新版的区别
	git checkout --readme.txt 撤销最后一次修改
	git rm readme.txt 删除文件
	git commit
	git checkout readme.txt 找回删除文件
	git remote origin url 添加远程仓库
	git push -u origin master 第一次推送并关联master分支
	
