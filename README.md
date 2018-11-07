# caoyuncong.github.io

1.  ajax参数

Ajax参数就是在发送Ajax请求的时候，带往服务器的数据，Ajax请求也是请求，请求参数包括querystring,
和formdata.

通常get请求传递的是querystring ，post请求传递的是formdata

2.  mybatis中的#和$的区别

	#将传入的数据都当成一个字符串，会对自动传入的数据加一个双引号

	$ 将传入的数据直接显示生成在sql中

	#方式能够很大程度防止sql注入。

	$方式无法防止sql注入。

	$方式一般用于传入数据库对象，例如传入表名

	MyBatis排序时使用order by 动态参数时需要注意，用$而不是#

3.  easyui datagrid传输数据到后台

有内置的Ajax，是直接有参数url进行数据传输，

4.  MySQL中用tinyint代表boolean，0为false，非0为true

图片在数据库中以字符串存储，存的是图片的路径，

5.  前后端分离
前端告诉我们需要什么样的数据，然后给前端返回json数据的接口，微信，支付宝只需要调用这个接口就可以了

6.  spring自定义注解
注解只是spring做的一个标记，比如  @Autowired : 告诉spring需要在哪注入对象, spring通过反射机制知道这个类的相关信息，实现对象注入
