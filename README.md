# caoyuncong.github.io
itchat4j -- 用Java扩展个人微信号的能力  https://github.com/yaphone/itchat4j

项目网站：进销存系统 https://www.oschina.net/project/tag/74/erp

Q1 ：xml有哪些解析技术?区别是什么?  https://blog.csdn.net/lingzhm/article/details/48350449

过滤器和拦截器的区别
记忆：原理 依赖关系  作用  应用
拦截器 基于Java反射机制，过滤器基于函数回调
拦截器不依赖于servlet容器，过滤器依赖
拦截器只对action请求起作用，过滤器对几乎所有请求起作用
拦截器可以访问action上下文、值栈里的对象，过滤器不能
在action生命周期中，拦截器可以多次被调用，过滤器只能在容器初始化被调用一次
拦截器可以获取IOC容器中的bean，而过滤器就不行，在拦截器里注入一个service，可以调用业务逻辑
拦截器可以获取ioc中 service bean 实现业务逻辑



Q2 : shiro 框架介绍  https://www.cnblogs.com/jpfss/p/8352031.html

shiro是一个权限框架，执行身份验证，

事务的并发问题

1》 脏读 事务A读到了事务B还没有提交的数据

2》不可重复读  在一个事务里面读取了两次某个数据，读出来的数据不一致

3》 幻读  在一个事务里面的操作中发现了未被操作的数据

小结：不可重复读的和幻读很容易混淆，不可重复读侧重于修改，幻读侧重于新增或删除。解决不可重复读的问题只需锁住满足条件的行，解决幻读需要锁表

数据库存json,mybatis如何 取json数据

https://www.cnblogs.com/kylindai/p/3563818.html

1.  ajax参数

Ajax参数就是在发送Ajax请求的时候，带往服务器的数据，Ajax请求也是请求，请求参数包括querystring,
和formdata.

通常get请求传递的是querystring ，post请求传递的是formdata

@requestParam  @pathvariable 区别
都是从request接收请求的，@requestParam是从request拿取值，@pathvariable从一个uri模板填充
http://localhost:8080/springmvc/hello/101?param1=10&param2=20

上面的一个url你可以这样写：

@RequestMapping("/hello/{id}")
    public String getDetails(@PathVariable(value="id") String id,
    @RequestParam(value="param1", required=true) String param1,
    @RequestParam(value="param2", required=false) String param2){
.......
}



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

事务只有在发生runtime及其子类异常才会回滚 

5.  前后端分离
前端告诉我们需要什么样的数据，然后给前端返回json数据的接口，微信，支付宝只需要调用这个接口就可以了

6.  spring自定义注解
注解只是spring做的一个标记，比如  @Autowired : 告诉spring需要在哪注入对象, spring通过反射机制知道这个类的相关信息，实现对象注入
