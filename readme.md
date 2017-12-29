http://www.cnblogs.com/xrq730/p/4919025.html

Spring提供了4种实现AOP的方式：
1.经典的基于代理的AOP
2.@AspectJ注解驱动的切面
3.纯POJO切面
4.注入式AspectJ切面




spring aop代理原理 
1.注意点：
如果目标对象实现了接口，默认情况下会采用JDK的动态代理实现AOP
如果目标对象实现了接口，可以强制使用CGLIB实现AOP
如果目标对象没有实现了接口，必须采用CGLIB库，spring会自动在JDK动态代理和CGLIB之间转换
2.强制把jdk代理转换成cglib代理
添加CGLIB库，SPRING_HOME/cglib/*.jar
在spring配置文件中加入这里写图片描述