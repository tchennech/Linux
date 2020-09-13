## 核心容器
**核心容器由**spring-core，spring-beans，spring-context，spring-context-support和spring-expression(Spring 表达式语言)模块组成。

spring-core和spring-beans模块提供 framework 的基本部分，包括 IoC 和依赖注入 features。 BeanFactory是工厂 pattern 的复杂 implementation。它消除了对程序化单例的需求，并允许您从实际程序逻辑中分离 configuration 和依赖项规范。

Context(spring-context)模块构建在核心和 Beans模块提供的坚实基础之上：它是一种以 framework-style 方式访问 objects 的方法，类似于 JNDI 注册表。 Context 模块从 Beans 模块继承其 features 并添加对国际化(使用，例如，资源包)，event 传播，资源加载以及透明的上下文创建的支持，例如，Servlet 容器。 Context 模块还支持 Java EE features，例如 EJB，JMX 和基本远程处理。 ApplicationContext接口是 Context 模块的焦点。 spring-context-support支持将 common third-party libraries 集成到 Spring application context 中，用于缓存(EhCache，Guava，JCache)，邮件(JavaMail)，调度(CommonJ，Quartz)和模板引擎(FreeMarker，JasperReports，Velocity)。

spring-expression模块提供了一个强大的表达语言，用于在运行时查询和操作 object 图。它是 JSP 2.1 规范中指定的统一表达式语言(统一 EL)的扩展。该语言支持设置和获取 property 值，property 赋值，方法调用，访问数组，集合和索引器的内容，逻辑和算术操作符，命名变量以及 Spring 的 IoC 容器中的 name 检索 objects。它还支持列表投影和选择以及 common 列表聚合。