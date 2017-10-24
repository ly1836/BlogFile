---
title: springmvc搭建JavaWeb应用
date: 2017-09-27 15:26:44
tags: [java,springMvc,spring]
---
<script>
(function(){
    var bp = document.createElement('script');
    var curProtocol = window.location.protocol.split(':')[0];
    if (curProtocol === 'https') {
        bp.src = 'https://zz.bdstatic.com/linksubmit/push.js';        
    }
    else {
        bp.src = 'http://push.zhanzhang.baidu.com/push.js';
    }
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(bp, s);
})();
</script>

本次记录利用springmvc框架搭建web应用，用到的IDE工具为 IntelliJ IDEA 2017.1.4 x64
# 一:新建项目,因为本次版本管理工具采用maven,左侧选中maven,选中<span style="background-color: #ccc;">[Create from archetype]</span>,如下图选中cocoon-22-archetype-webapp构建web应用
<!-- more -->
<img src="https://github.com/ly1836/img/blob/master/springmvc/1.png?raw=true"/>
# 二:填写maven的GroupId和ArtifactId
<img src="https://github.com/ly1836/img/blob/master/springmvc/2.png?raw=true"/>
# 三:选择当前计算机安装的mavem安装位置及配置文件地址和本地仓库位置
<img src="https://github.com/ly1836/img/blob/master/springmvc/3.png?raw=true"/>
# 四:在main目录下新建java文件夹，用于存放java代码，在project structure 中设置java文件夹为Source
<img src="https://github.com/ly1836/img/blob/master/springmvc/4.png?raw=true"/>
# 五:在webapp/WEB-INF/下新建spring-mvc-servlet.xml文件,新建view文件夹用于存放视图，当前项目结构如下图:
<img src="https://github.com/ly1836/img/blob/master/springmvc/7.png?raw=true"/>
# 六:在pom.xml中加入springmvc所需的包，如下引完包之后用maven clear下
## (1)在<span style="background-color: #ccc;">project</span>标签下加入如下定义
```
<!-- spring 当做springmvc的父模块 -->
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>1.5.8.RELEASE</version><!--  -->
  </parent>
```
## (2)在<span style="background-color: #ccc;">dependencies</span>标签下加入springmvc的所需jar包及jsp标准库和日志库
```
<!-- spring mvc -->
 <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-webmvc</artifactId>
    </dependency>

    <dependency>
      <groupId>org.springframework</groupId>
      <artifactId>spring-context-support</artifactId>
      <scope>runtime</scope>
    </dependency>
    <!-- jsp标准标签库 -->
    <dependency>
      <groupId>org.glassfish</groupId>
      <artifactId>javax.servlet.jsp.jstl</artifactId>
      <version>3.0.1</version>
    </dependency>

    <dependency>
      <groupId>org.slf4j</groupId>
      <artifactId>slf4j-api</artifactId>
    </dependency>

    <dependency>
      <groupId>org.apache.logging.log4j</groupId>
      <artifactId>log4j-slf4j-impl</artifactId>
    </dependency>

    <dependency>
      <groupId>org.apache.logging.log4j</groupId>
      <artifactId>log4j-web</artifactId>
    </dependency>
```
# 七:在web.xml中配置springmvc的核心过滤器,用于在web程序初始化的时候启动springmvc
```
<listener>
    <listener-class>
      org.springframework.web.context.ContextLoaderListener
    </listener-class>
  </listener>

  <servlet>
    <servlet-name>spring-mvc</servlet-name>
    <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>

    <load-on-startup>2</load-on-startup>
  </servlet>
  <servlet-mapping>
    <servlet-name>spring-mvc</servlet-name>
    <url-pattern>/</url-pattern>
  </servlet-mapping>

  <!-- 解决工程编码过滤器 -->
  <filter>
    <filter-name>characterEncodingFilter</filter-name>
    <filter-class>org.springframework.web.filter.CharacterEncodingFilter</filter-class>
    <init-param>
      <param-name>encoding</param-name>
      <param-value>UTF-8</param-value>
    </init-param>
  </filter>
  <filter-mapping>
    <filter-name>characterEncodingFilter</filter-name>
    <url-pattern>/*</url-pattern>
  </filter-mapping>
```
# 八:配置spring-mvc-servlet.xml文件
```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	   xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:context="http://www.springframework.org/schema/context"
	   xmlns:mvc="http://www.springframework.org/schema/mvc"
	   xmlns:aop="http://www.springframework.org/schema/aop"
	   xsi:schemaLocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans.xsd
        http://www.springframework.org/schema/context
        http://www.springframework.org/schema/context/spring-context.xsd
        http://www.springframework.org/schema/mvc
  		http://www.springframework.org/schema/mvc/spring-mvc.xsd
        http://www.springframework.org/schema/aop
        http://www.springframework.org/schema/aop/spring-aop.xsd">

	<!--<mvc:annotation-driven/>相当于注册了DefaultAnnotationHandlerMapping和AnnotationMethodHandlerAdapter两个bean，配置一些messageconverter。即解决了@Controller注解的使用前提配置。 -->
	<mvc:annotation-driven />
	<!--<context:annotation-config/>是对包进行扫描，实现注释驱动Bean定义，同时将bean自动注入容器中使用。即解决了@Controller标识的类的bean的注入和使用。 -->
	<context:annotation-config />

	<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
		<!--前缀 -->
		<property name="prefix" value="/view/"/>
		<!--后缀 -->
		<property name="suffix" value=".jsp"/> <!--这里视图技术暂时采用jsp -->
		<property name="contentType" value="text/html;charset=UTF-8" />
		<property name="viewClass" value="org.springframework.web.servlet.view.JstlView" />
	</bean>


	<!-- control类 -->
	<bean id="index" class="cn.com.control.HelloSpringMvc">
	</bean>

</beans>
```
#  九:编写java代码,实现视图控制器.
这里是一个简单的页面跳转,使用@Controller注解标识这个类是一个控制器，@RequestMapping注解说明这个类进入的request请求地址，如@RequestMapping(value = "/springmvc"),springmvc相对于strtus框架来说,springmvc是方法级别的拦截，@RequestMapping注解也可以写在方法上.如下面代码:
注意:我返回的的数据类型是ModelAndView,这个是springmvc提供的模型和视图的一个解析器，可直接传入视图名，或者携带数据到前端页面new ModelAndView().addObject("object", Object);
```
package cn.com.control;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.*;
import org.springframework.web.servlet.ModelAndView;

@Controller
@RequestMapping(value = "/springmvc")
public class HelloSpringMvc {

    @RequestMapping(value = "/index")
    public ModelAndView test(ModelAndView mav){
        mav = new ModelAndView("index_page");
        mav.addObject("name","leiYang");
        return mav;
    }
}
```
# 十:index_page.jsp代码如下:
```
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
<head>
    <title>spring mvc</title>
</head>
<body>
    <p>你好 ${name}</p>
</body>
</html>

```
# 十一:如下图配置好tomcat
<img src="https://github.com/ly1836/img/blob/master/springmvc/9.png?raw=true"/>
<img src="https://github.com/ly1836/img/blob/master/springmvc/8.png?raw=true"/> 
# 十二:打开浏览器访问地址,
<img src="https://github.com/ly1836/img/blob/master/springmvc/10.png?raw=true"/> 