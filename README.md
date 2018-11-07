# caoyuncong.github.io

ajax参数

Ajax参数就是在发送Ajax请求的时候，带往服务器的数据，Ajax请求也是请求，请求参数包括querystring,
和formdata.

通常get请求传递的是querystring ，post请求传递的是formdata

mybatis中的#和$的区别

	# 将传入的数据都当成一个字符串，会对自动传入的数据加一个双引号

	$ 将传入的数据直接显示生成在sql中

	#方式能够很大程度防止sql注入。

	$方式无法防止sql注入。

	$方式一般用于传入数据库对象，例如传入表名

	MyBatis排序时使用order by 动态参数时需要注意，用$而不是#
