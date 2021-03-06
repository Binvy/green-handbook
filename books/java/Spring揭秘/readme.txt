《Spring揭秘》 											// start 2020-8-2 10:00:09 done 2020-8-24 23:48:21

	第一部分 掀起Spring的盖头来

		第1章 Spring框架的由来 							// done 2020-8-2 10:39:09

			1.1 Spring之崛起
			1.2 Spring框架概述
			1.3 Spring大观园
			1.4 小结

	第二部分　Spring的IoC容器 							

		第2章　IoC的基本概念　							// done 2020-8-2 11:11:26

			2.1 我们的理念是：让别人为你服务
			2.2 手语，呼喊，还是心有灵犀
				2.2.1 构造方法注入
				2.2.2 setter方法注入
				2.2.3 接口注入
				2.2.4 三种注入方式的比较
			2.3 Ioc的附加值
			2.4 小结

			IoC是一种可以帮助我们解耦个业务对象间依赖关系的对象绑定方式！

		第3章　掌管大局的IoC Service Provider　			// done 2020-8-2 11:26:45

			3.1 IoC Service Provider的职责
			3.2 运筹帷幄的秘密————IoC Service Provide如何管理对象间的依赖关系
				3.2.1 直接编码方式
				3.2.2 配置文件方式
				3.2.3 元数据方式
			3.3 小结
		
		第4章　Spring的IoC容器之BeanFactory　				// done 2020-8-2 17:42:58
		
			4.1 拥有BeanFactory之后的生活
			4.2 BeanFactory的对象注册和依赖绑定方式
				4.2.1 直接编码方式
				4.2.2 外部配置文件方式
					1. Properties配置格式的加载
					2. XML配置格式的加载
				4.2.3 注解方式
			4.3 BeanFactory的XML之旅
				4.3.1 <beans>和<bean>
					1. <beans>之唯我独尊
					2. <description>、<import>和<alias>
				4.3.2 孤孤单单一个人
				4.3.3 Help Me, Help You
					1. 构造方式注入的XML之道
					2. setter方法注入的XML之道
					3. <property>和<constructor-arg>中可用的配置项
					4. depends-on
					5. aotowire
					6. dependency-check
					7. lazy-init
				4.3.4 继承？我也会！
				4.3.5 bean的scope
					1. singleton
					2. protoype
					3. request、session和global session
					4. 自定义scope类型
				4.3.6 工厂方法和FactoryBean
					1. 静态工厂方法（Static Factory Method）
					2. 非静态工厂方法（Instance Factory Method）
					3. FactoryBean
				4.3.7 偷梁换柱之术
					1. 方法注入 
					2. 殊途同归
					3. 方法替换
			4.4 容器背后的秘密
				4.4.1 “战略性观望”
					1. 容器启动阶段
					2. Bean实例化阶段
				4.4.2 “插手”容器的启动
					1. PropertyPlaceholderConfigurer
					2. PropertyOverrideConfigurer
					3. CustomEditorConfiguer
				4.4.3 了解Bean的一生
					1. Bean的实例化和BeanWrapper
					2. 各色的Aware接口
					3. BeanPostProcessor
					4. InitializingBean和init-method
					5. DisposableBean和destory-method
			4.5 小结

		第5章　Spring IoC容器ApplicationContext　			// done 2020-8-2 19:11:29

			5.1 统一资源加载策略
				5.1.1 Spring中的Resource
				5.1.2 ResourceLoader，更广泛的“URL”
					1. 可用的ResourceLoader
					2. ResourePatternResolver————批量查找的ResourceLoader
					3. 回顾与展望
				5.1.3 Application和ResourceLoader
					1. 扮演ResourceLoader的角色
					2. RsourceLoader类型的注入
					3. Rsource类型的注入
					4. 在特定情况下，ApplicationContext的Resource加载行为
			5.2 国际化信息支持（I18n MessageSource）
				5.2.1 JavaSE提供的国际化支持
					1. Locale
					2. ResourceBundle
				5.2.2 MessageSource和ApplicationContext
					1. 可用的MessageSource实现
					2. MessageSourceAware和MessageSource的注入
			5.3 容器内部事件发布
				5.3.1 自定义事件发布
				5.3.2 Spring的容器内事件发布类结构分析
			5.4 多配置模块加载的简化
			5.5 小结

				ApplicationContext是Spring在BeanFactory基础容器之上，提供的另一个IoC容器实现。它拥有许多BeanFactory所没有的特性，
				包括统一的资源加载策略、国际化信息支持、容器内事件发布以及简化的多配置文件加载功能。

		第6章　Spring IoC容器之扩展篇　					// done 2020-8-2 19:29:42

			6.1 Spring2.5的基于注解的依赖注入
				6.1.1 注解版的自动绑定（@Autowired）
					1. 从自动绑定（autowire）到@Autowired
					2. @Qualifier的陪伴
				6.1.2 @Autowired之外的选择————使用JSR250标注依赖注入㽑
				6.1.3 将革命进行地更彻底一些（classpath-scanning功能介绍）
			6.2 Spring3.0展望
			6.3 小结

	第三部分　Spring AOP框架

		第7章　一起来看AOP　								// done 2020-8-3 23:43:26

			7.1 AOP的尴尬
			7.2 AOP走向现实
				7.2.1 静态AOP时代
				7.2.2 动态AOP时代
			7.3 Java平台上的AOP实现机制
				7.3.1 动态代理
					java.lang.reflect.InvocationHandler
				7.3.2 动态字节码增强
					ASM/CGLIB
				7.3.3 Java代码生成
				7.3.4 自定义类加载器 
				7.3.5 AOL扩展 
			7.4 AOP国家的公民
				7.4.1 Joinpoint
				7.4.2 Pointcut
					1. Pointcut的表述方式
					2. Pointcut运算
				7.4.3 Advice
					1. Before Advice
					2. After Advice
						- After returning Advice
						- After throwing Advice
						- After Advice
					3. Around Advice
					4. Introduction	
				7.4.4 Aspect
				7.4.5 织入与织入器
					org.springframework.aop.framework.ProxyFactory
				7.4.6 目标对象
			7.5 小结

		第8章　Spring AOP概述及其实现机制　						// done 2020-8-4 22:14:50
		
			8.1 Spring AOP概述
			8.2 Spring AOP的实现机制
				8.2.1 设计模式之代理模式
				8.2.2 动态代理
					java.lang.reflect.Proxy
					java.lang.reflect.InvocationHandler

					java: 
						// To create a proxy for some interface Foo:
				       InvocationHandler handler = new MyInvocationHandler(...);
				       Class<?> proxyClass = Proxy.getProxyClass(Foo.class.getClassLoader(), Foo.class);
				       Foo f = (Foo) proxyClass.getConstructor(InvocationHandler.class).
				                       newInstance(handler);
						   
						// or more simply:
				       Foo f = (Foo) Proxy.newProxyInstance(Foo.class.getClassLoader(),
				                                            new Class<?>[] { Foo.class },
				                                            handler);

				8.2.3 动态字节码生成
					net.sf.cglib.proxy.Callback
					net.sf.cglib.proxy.MethodInterceptor
					net.sf.cglib.proxy.Enhancer

					java: org.springframework.aop.framework.CglibAopProxy#getProxy(java.lang.ClassLoader)
						// Configure CGLIB Enhancer...
						Enhancer enhancer = new Enhancer();
						if (classLoader != null) {
							enhancer.setClassLoader(classLoader);
							if (classLoader instanceof SmartClassLoader &&
									((SmartClassLoader) classLoader).isClassReloadable(proxySuperClass)) {
								enhancer.setUseCache(false);
							}
						}
						enhancer.setSuperclass(proxySuperClass);
						enhancer.setInterfaces(AopProxyUtils.completeProxiedInterfaces(this.advised));
						enhancer.setNamingPolicy(SpringNamingPolicy.INSTANCE);
						enhancer.setStrategy(new ClassLoaderAwareGeneratorStrategy(classLoader));

						Callback[] callbacks = getCallbacks(rootClass);
						Class<?>[] types = new Class<?>[callbacks.length];
						for (int x = 0; x < types.length; x++) {
							types[x] = callbacks[x].getClass();
						}
						// fixedInterceptorMap only populated at this point, after getCallbacks call above
						enhancer.setCallbackFilter(new ProxyCallbackFilter(
								this.advised.getConfigurationOnlyCopy(), this.fixedInterceptorMap, this.fixedInterceptorOffset));
						enhancer.setCallbackTypes(types);

						// Generate the proxy class and create a proxy instance.
						enhancer.setInterceptDuringConstruction(false);
						enhancer.setCallbacks(callbacks);
						return (this.constructorArgs != null && this.constructorArgTypes != null ?
								enhancer.create(this.constructorArgTypes, this.constructorArgs) :
								enhancer.create());

			8.3 小结 

		第9章　Spring AOP一世　							// done 2020-8-5 00:04:26
		
			9.1 Spring AOP中的Joinpoint
			9.2 Spring AOP中的Pointcut
				9.2.1 常见的Pointcut
					1. NameMatchMethodPointcut
					2. JdkRegexpMethodPointcut和Perl5RegexpMethodPointcut
					3. AnnotationMatchingPointcut
					4. ComposablePointcut
					5. ControlFlowPointcut
				9.2.2 扩展Pointcut（Customize Pointcut）
					1. 自定义StaticMethodMatcherPointcut
					2. 自定义DynamicMethodMatcherPointcut
				9.2.3 IoC容器中的Pointcut
			9.3 Spring AOP中的Advice
				9.3.1 per-class类型的Advice
					1. Before Advice
					2. ThrowsAdvice
					3. AfterReturningAdvice
				9.3.2 per-instance类型的Advice
			9.4 Spring AOP中的Aspect
				9.4.1 PointcutAdvisor家族
					1. DefaultPointcutAdvisor
					2. NameMatchMethodPointcutAdvisor
					3. RegexpMethodPointcutAdvisor
					4. DefaultBeanFactoryPointcutAdvisor
				9.4.2 IntrodoctionAdvisor分支
				9.4.3 Ordered的作用
			9.5 Spring AOP中的织入
				9.5.1 如何与ProxyFactory打交道
					1. 基于接口的代理
						
						public interface ITask {
							void execute(TaskExecutionContext ctx);
						}

						public class MockTask implements ITask {
							public void execute(TaskExecutionContext ctx) {
								System.out.println("task executed");
							}
						}

						public class PerformanceMethodInterceptor implements MethodInterceptor {
							public static final Logger logger = LoggerFactory.getLogger(PerformanceMethodInterceptor.class);
							public Object invoke(MethodInvocation invocation) throws Throwable {
								StopWatch watch = new StopWatch();
								try {
									watch.start();
									return invocation.proceed();
								} finally {
									watch.stop();
									if (logger.isInfoEnabled()) {
										logger.info(watch.toString());
									}
								}
							}
						}

						// 实现了某个接口时，默认采用基于接口的动态代理。

							MockTask task = new MockTask();
							ProxyFactory weaver = new ProxyFactory(task);
							// weaver.setInterfaces(new class[]{ITask.class});
							NameMatchMethodPointcutAdvisor advisor = new NameMatchMethodPointcutAdvisor();
							advisor.setMappedName("execute");
							advisor.setAdvice(new PerformanceMethodInterceptor());
							weaver.addAdvisor(advisor);
							ITask proxyObject = (ITask)weaver.getProxy();
							proxyObject.execute(null);

					2. 基于类的代理

						public class Executable {
							public void execute() {
								System.out.println("Executable without any Interfaces");
							}
						}


						// 默认没有实现任何接口时，默认采用基于类的代理-CGLIB代理：

							ProxyFactory weaver = new ProxyFactory(new Executable());
							NameMatchMethodPointcutAdvisor advisor = new NameMatchMethodPointcutAdvisor();
							advisor.setMappedName("execute");
							advisor.setAdvice(new PerformanceMethodInterceptor());
							weaver.addAdvisor(advisor);
							Executable proxyObject = (Executable)weaver.getProxy();
							proxyObject.execute(null);
							System.out.println(proxyObject.getClass());

						// 实现了某个接口时，通过proxyTargetClass属性强制proxyFactory采用基于类的代理

							MockTask task = new MockTask();
							ProxyFactory weaver = new ProxyFactory(task);
							// weaver.setInterfaces(new class[]{ITask.class});
							weaver.setProxyTargetClass(true);
							NameMatchMethodPointcutAdvisor advisor = new NameMatchMethodPointcutAdvisor();
							advisor.setMappedName("execute");
							advisor.setAdvice(new PerformanceMethodInterceptor());
							weaver.addAdvisor(advisor);
							MockTask proxyObject = (MockTask)weaver.getProxy();
							proxyObject.execute(null);
							System.out.println(proxyObject.getClass());

						// 满足以下任一条件，则创建CGLIB代理：
							1. the optimize flag is set
							2. the proxyTargetClass flag is set
							3. no proxy interfaces have been specified

				9.5.2 看清ProxyFactory的本质

					public class DefaultAopProxyFactory implements AopProxyFactory, Serializable {

						/**
						 * Whether this environment lives within a native image.
						 * Exposed as a private static field rather than in a {@code NativeImageDetector.inNativeImage()} static method due to https://github.com/oracle/graal/issues/2594.
						 * @see <a href="https://github.com/oracle/graal/blob/master/sdk/src/org.graalvm.nativeimage/src/org/graalvm/nativeimage/ImageInfo.java">ImageInfo.java</a>
						 */
						private static final boolean IN_NATIVE_IMAGE = (System.getProperty("org.graalvm.nativeimage.imagecode") != null);


						@Override
						public AopProxy createAopProxy(AdvisedSupport config) throws AopConfigException {
							if (!IN_NATIVE_IMAGE &&
									(config.isOptimize() || config.isProxyTargetClass() || hasNoUserSuppliedProxyInterfaces(config))) {
								Class<?> targetClass = config.getTargetClass();
								if (targetClass == null) {
									throw new AopConfigException("TargetSource cannot determine target class: " +
											"Either an interface or a target is required for proxy creation.");
								}
								if (targetClass.isInterface() || Proxy.isProxyClass(targetClass)) {
									return new JdkDynamicAopProxy(config);
								}
								return new ObjenesisCglibAopProxy(config);
							}
							else {
								return new JdkDynamicAopProxy(config);
							}
						}

						/**
						 * Determine whether the supplied {@link AdvisedSupport} has only the
						 * {@link org.springframework.aop.SpringProxy} interface specified
						 * (or no proxy interfaces specified at all).
						 */
						private boolean hasNoUserSuppliedProxyInterfaces(AdvisedSupport config) {
							Class<?>[] ifcs = config.getProxiedInterfaces();
							return (ifcs.length == 0 || (ifcs.length == 1 && SpringProxy.class.isAssignableFrom(ifcs[0])));
						}

					}

				9.5.3 容器中的织入器————ProxyFactoryBean
					1. ProxyFactoryBean的本质
					2. ProxyFactoryBean的使用
				9.5.4 加快织入的自动化进程
					1. 自动代理得以实现的原理
						BeanPostProcessor
					2. 可用的AutoProxyCreator
						- BeanNameAutoProxyCreator
						- DefaultAdvisorAutoProxyCreator
			9.6 TargetSource
				9.6.1 可用的TargetSource实现类
					1. SingletonTargetSource
					2. PrototypeTargetSource
					3. HotSwappableTargetSource
					4. CommonsPoolTargetSource
					5. ThreadLocalTargetSource
				9.6.2 如何自定义TargetSource
					class XXX extends TargetSource	
			9.7 小结

		第10章　Spring AOP二世　							// done 2020-8-9 14:33:38
		
			10.1 @AspectJ形式的Spring AOP

				10.1.1 @Aspect形式AOP使用之先睹为快
					1. 编程方式织入
						AspectJProxyFactory factory = new AspectJProxyFactory();
						factory.setProxyTargetClass(true);
						factory.setTarget(new Foo());
						factory.addAspect(PerformanceTraceAspect.class);
						Object proxy = factory.getProxy();
						((Foo)proxy).method1();
						((Foo)proxy).method2();
					2. 通过自动代理织入
						<bean class="org.springframework.aop.aspectj.annotation.AnnotationAwareAspectJAutoProxyCreator">
							<property name="proxyTargetClass" value="true"></property>
						</bean>
						<bean id="performanceAspect" class="...PerformanceTraceAspect"></bean>
						<bean id="target" class="...Foo">
				10.1.2 @Aspect形式的Pointcut
					1. @Aspect形式Pointcut的声明方式
					2. @Aspect形式Pointcut表达式的标识符
						-execution
						-within
						-this、target
						-args
						-@within
						-@annotation
					3. @Aspect形式Pointcut在SpringAOP中的真实面目
						Pointcut: AspectJExpressionPointcut
				10.1.3 @Aspect形式的Advice
					1. Before Advice: org.aspectj.lang.annotation.Before
					2. After Throwing Advice: org.aspectj.lang.annotation.AfterThrowing
					3. After Returning Advice: org.aspectj.lang.annotation.AfterReturning
					4. After (Finally) Advice: org.aspectj.lang.annotation.After
					5. Around Advice: org.aspectj.lang.annotation.Around
					6. Introduction: org.aspectj.lang.annotation.DeclearParents
				10.1.4 @AspectJ中的Aspect更多话题
					1. Advice的执行顺序
					2. Aspect的实例化模式	

			10.2 基于Schema的AOP

				10.2.1 基于Schema的AOP配置概览
					<aop:config proxy-target-class="true">
						<aop:pointcut/>
						<aop:advisor/>
						<aop:aspect></aop:aspect>
					</aop:config>
				10.2.2 向基于Schema的AOP迁移
					1. 单纯的迁移
					2. 深入挖掘<aop:advisor>
				10.2.3 @Aspect到“基于Schema的AOP”迁移
					1. 基于Schema的Aspect声明
					2. 基于Schema的Pointcut声明
					3. 基于Schema的Advice声明
						<aop:aspect id="myaspect" ref="genericSchemaBaseAspect" order="2">
							<aop:pointcut id="privatePointcut" expression="execution(public void *.doSth())"/>
							<aop:before pointcut-ref="privatePointcut" method="doBefore"/>
							<aop:after-returning pointcut-ref="privatePointcut" method="doAfterReturning" returning="retValue"/>
							<aop:after-throwing pointcut-ref="privatePointcut" method="doAfterThrowing" throwing="e"/>
							<aop:after pointcut-ref="privatePointcut" method="doAfter"/>
							<aop:around pointcut-ref="privatePointcut" method="doProfile"/>
							<aop:declear-parents types-matching="...*" implement-interface="...ICounter" default-impl="...CounterImpl">
						</aop:aspect>
					4. 其他需要关注的地方
						- Advice的参数化
						- Advcie的执行顺序
						- Advcie的实例化模式

			10.3 小结
				三种Spring AOP的使用方式
					- Spring AOP 1.x基于接口定义的Advice声明方式
					- @AspectJ形式的AOP，注解方式
					- 基于Schema的AOP，XML+注解

		第11章　AOP应用案例　								// done 2020-8-9 14:53:23

			11.1 异常处理
				11.1.1 Java异常处理
					Java异常类型：
						- unchecked exception: 编译器不会对这些类型的异常进行编译期检查。
							java.lang.Error, java.lang.RuntimeException及其子类
							
						- checked exception: 编译期会对这些类型的异常进行编译期检查，如果有方法抛出该类异常，调用程序必须对这些异常进行处理。
							java.lang.Exception及其子类，除去java.lang.RuntimeException分支

				11.1.2 Fault Barrier

			11.2 安全检查

				Spring Security

			11.3 缓存

			11.4 小结
		
		第12章　Spring AOP之扩展篇　						// done 2020-8-9 15:05:22

			12.1 有关公开当前调用的代理对象的探讨

				12.1.1 问题的现象

					public class NestableInvocationBO {

						public void method1() {
							method2();
							System.out.println("method1 executed");
						}

						public void method2() {
							System.out.println("method2 executed");
						}

					}

					如果定义Aspect进行横切拦截，当执行method1的时候，只有method1会拦截成功，method1中的method2方法执行没有被拦截。

				12.1.2 原因的分析

					Spring AOP的实现机制造成的。 Spring AOP采用代理模式实现AOP，具体的横切逻辑会被添加到动态生成的代理对象中，只要调用的是目标对象的代理
					对象上的方法，通常就可以保证目标对象上的方法执行可以被拦截。 但代理的执行，终归要调用目标对象上的同一方法来执行最初所定义的方法逻辑。
					如果目标对象中原始方法调用依赖于其他对象，那没问题，可以为目标对象注入所依赖对象的代理，保证响应的Joinpoint被拦截并织入横切逻辑。而一旦
					目标对象中的原始方法调用直接调用自身方法的时候，也就是说，它依赖于自身所定义的其他方法的时候，问题就来了。

				12.1.3 解决方案
					
					public class NestableInvocationBO {

						public void method1() {
							((NestableInvocationBO)AopContext.currentProxy()).method2();
							System.out.println("method1 executed");
						}

						public void method2() {
							System.out.println("method2 executed");
						}

					}	

			12.2 小结


	第四部分　使用Spring访问数据

		第13章　统一的数据访问异常层次体系　					// done 2020-8-10 21:00:00
		
			13.1 DAO模式的背景

			13.2 梦想照进现实

			13.3 发现问题，解决问题

			13.4 不重复发明轮子

			13.5 小结

		第14章　JDBC API的最佳实践　							// done 2020-8-10 22:39:32
		
			14.1 基于Template的JDBC使用方式

				14.1.1 JDBC的尴尬
				14.1.2 JdbcTemplate的诞生
					1. 模板方法模式简介
					2. JdbcTemplate的演化
					3. 使用DataSourceUtils进行Connection的管理
					4. 使用NativeJdbcExtractor来获得“真相”
					5. 控制JdbcTemplate的行为
					6. SQLException到DataAccessException体系的转译
				14.1.3 JdbcTemplate和它的兄弟们
					1. 使用JdbcTemplate进行数据访问
					2. NamedParameterJdbcTemplate
					3. SimpleJdbcTemplate
				14.1.4 Spring中的DataSource
					1. DataSource的种类
					2. DataSource的访问方式
					3. 自定义DataSource实现
				14.1.5 JdbcDaoSupport

			14.2 基于操作对象的JDBC使用方式

				14.2.1 基于操作对象的查询
					1. MappingSqlQueryWithParameters
					2. MappingSqlQuery
					3. SqlFunction
					4. UpdatableSqlQuery
					5. 基于操作对象的LOB查询
				14.2.2 基于操作对象的更新
					1. SqlUpdate
					2. BatchSqlUpdate
					3. 基于操作对象的LOB更新
				14.2.3 基于操作对象的存储过程调用

			14.3 小结	
			

		第15章　Spring对各种ORM的集成　						// done 2020-8-10 23:17:12
		
			15.1 Spring对Hibernate的集成

				15.1.1 旧日“冬眠”时光
				15.1.2 “春天”里的“冬眠”
					1. HibernateTemplate的登场
					2. Spring中的SessionFactory的配置及获取
					3. HibernateDaoSupport

			15.2 Spring对iBatis的集成

				15.2.1 iBatis实践之“前生”篇
				15.2.2 iBatis实践之“今世”篇
					1. SqlMapClientTemplate的实现
					2. SqlMapClientTemplate的使用
					3. SqlMapClientDaoSupoort

			15.3 Spring对其他ORM方案的集成概述

				15.3.1 Spring对JDO的集成
					1. Spring中的JDO资源管理
					2. Spring中的JDO异常转译
					3. JdoDaoSupport
				15.3.2 Spring对TopLink的集成
					1. Spring中的TopLink资源管理
					2. TopLink数据访问异常到Spring异常体系的转译
					3. TopLinkDaoSupport
				15.3.3 Spring对JPA的集成
					1. Spring中JPA的资源管理	
					2. Spring中JPA的异常转译

			15.4 小结		

		第16章　Spring数据访问之扩展篇　						// done 2020-8-10 23:26:13

			16.1 活用模板方法模式及Callback
				16.1.1 FtpClientTemplate
				16.1.2 HttpClientTemplate

			16.2 数据访问中多数据源
				
				16.2.1 “主权独立”的多数据源

					`xml:

						<bean id="mainDataSource" class="org.apache.commons.dbcp.BasicDataSource" destory-method="close">
							<property name="url" value="..." />
							<property name="driverClassName" value="..." />
							<property name="username" value="..." />
							<property name="password" value="..." />
							<!-- other property settings -->
						</bean>

						<bean id="infoDataSource" class="org.apache.commons.dbcp.BasicDataSource" destory-method="close">
							<property name="url" value="..." />
							<property name="driverClassName" value="..." />
							<property name="username" value="..." />
							<property name="password" value="..." />
							<!-- other property settings -->
						</bean>

						<bean id="mainJdbcTemplate" class="org.springframework.jdbc.core.JbdcTemplate">
							<property name="dataSource" ref="mainDataSource">
						</bean>

						<bean id="infoJdbcTemplate" class="org.springframework.jdbc.core.JbdcTemplate">
							<property name="dataSource" ref="infoDataSource">
						</bean>

						<bean id="dataAccessResourceSupport" abastract="true">
							<property name="mainJdbcTemplate" ref="mainJdbcTemplate" />
							<property name="infoJdbcTemplate" ref="infoJdbcTemplate" />
						<bean/>

						<bean id="someDaoWithMainDS" class="...">
							<property name="mainJdbcTemplate" ref="mainJdbcTemplate" />
						</bean>

						<bean id="someDaoWithInfoDS" class="...">
							<property name="infoJdbcTemplate" ref="infoJdbcTemplate" />
						</bean>

						<bean id="someDaoWithBothDS" parent="dataAccessResourceSupport">
						</bean>

				16.2.2 “合纵连横”的多数据源

					`java:

						public class PrototypeLoadBalanceDataSource extends AbstractRoutingDataSource {

							private Lock lock = new ReentrantLock();
							private int counter = 0;
							private int dataSourceNumber = 3;

							@Override
							public Object determineCurrentLookupKey() {
								lock.lock();
								try {
									counter++;
									int lookupKey = counter % getDataSourceNumber();
									return new Integer(lookupKey);
								} finally {
									lock.unlock();
								}
							}
							// ...
						}

					`xml:	

						<bean id="dataSource1" class="org.apache.commons.dbcp.BasicDataSource" destory-method="close">
							<property name="url" value="..." />
							<property name="driverClassName" value="..." />
							<property name="username" value="..." />
							<property name="password" value="..." />
							<!-- other property settings -->
						</bean>

						<bean id="dataSource2" class="org.apache.commons.dbcp.BasicDataSource" destory-method="close">...</bean>

						<bean id="dataSource3" class="org.apache.commons.dbcp.BasicDataSource" destory-method="close">...</bean>

						<util:map id="dataSources">
							<entry key="0" value-ref="dataSource1" />
							<entry key="1" value-ref="dataSource2" />
							<entry key="2" value-ref="dataSource3" />
						</util:map>

						<bean id="dataSourceLookup" class="org.springframework.jdbc.datasource.lookup.MapDataSourceLookup">
							<contructor-arg>
								<ref bean="dataSource">
							</contructor-arg>
						</bean>

						<bean id="dataSource" class="...PrototypeLoadBalanceDataSource">
							<property name="defaultTargetDataSource" ref="dataSource1" />
							<property name="targetDataSource" ref="dataSources" />
							<property name="dataSourceLookup" ref="dataSourceLookup" />
						</bean>

						<bean id="jdbcTemplate" class="org.springframework.jdbc.core.JbdcTemplate">
							<property name="dataSource" ref="dataSource">
						</bean>

						<bean id="someDao" class="...SomeDaoImpl">
							<property name="jdbcTemplate" ref="jdbcTemplate" />
						</bean>

				16.2.3 结束语

			16.3 Spring3.0展望

			16.4 小结

	第五部分　事务管理 										// done 2020-8-11 23:54:15

		第17章　有关事务的楔子　								// done 2020-8-12 21:08:30						

			17.1 认识事物本身

				事务： 以可控的方式对数据资源进行访问的一组操作。

				属性：

					原子性（Atomicity）： 事务所包含的全部操作是一个不可分割的整体，要么全部成功，要失败就全部失败。

					一致性（Consistency）： 数据资源在事务执行前后都保持数据间的一致性状态。

					隔离性（Isolation）： 规定了各个事务之间互相影响的程度。

						隔离级别：

							read uncommited: 一个事务可以读取另一个事务未提交的更新结果。问题：脏读、幻读、不可重复读

							read commited: 一个事务的更新操作只有在该事务提交之后，另一个事务才可能读取到更新后的结果。问题：幻读、不可重复读（Oracle的默认隔离级别）

							repeatable read: 保证在整个事务的过程中，对同一笔数据的读取结果是相同的，不管其他事务是否同时在对同一笔数据进行更新，以及事务是否提交。 问题：幻读（MySQL的默认隔离级别）

							serializable: 所有的事务操作依次顺序执行。

						tips:	

							Oracle只支持READ COMMITTED 和 SERIALIZABLE这两种事务隔离级别。所以Oracle不支持脏读。 MySQL支持以上4种隔离级别。

						并发问题：	

							脏读： 如果一个事务对数据进行更新，但未提交事务，另一个事务就可以看到该事务未提交的更新结果。事务回滚之后，第二个事务读取的数据是笔脏数据。

							幻读： 同一个查询在整个事务过程中多次执行后，查询所得的结果集不一样，针对的是多笔记录。

							不可重复读： 同一个事务在整个事务过程中对同一笔数据进行读取，每次读取结果不同。

					持久性（Durability）： 一旦整个事务提交成功，对数据所做的变更将被记载并不可逆转。

			17.2 初始事务家族成员

			17.3 小结	

		第18章　群雄逐鹿下的Java事务管理　						// done 2020-8-12 21:12:49

			18.1 Java平台的局部事务支持

			18.2 Java平台的分布式事务支持

				18.2.1 基于JTA的分布式事务管理

				18.2.2 基于JCA的分布式事务管理

			18.3 继续前行之前的反思

				1. 局部事务的管理绑定到了具体的数据访问方式

				2. 事务的异常处理

				3. 事务处理API的多样性

				4. CMT声明式事务的局限

			18.4 小结	

		第19章　Spring事务王国的架构　						
		
			19.1 统一中原的过程

				核心接口： org.springframework.transaction.PlatformTransactionManager

			19.2 和平时代

				19.2.1 TransactionDefinition

					1. TransactionDefinition简介: 具体细节参考spring-refrence-guide

						隔离级别：#getIsolationLevel

							ISOLATION_DEFAULT:

							ISOLATION_READ_UNCOMMITTED:

							ISOLATION_READ_COMMITTED:

							ISOLATION_REPEATABLE_READ:

							ISOLATION_SERIALIZABLE:

						传播行为：#getPropagationBehavior

							PROPAGATION_REQUIRED: 

							PROPAGATION_SUPPORTS:

							PROPAGATION_MANDATORY:

							PROPAGATION_REQUIRES_NEW:

							PROPAGATION_NOT_SUPPORTED:

							PROPAGATION_NEVER:

							PROPAGATION_NESTED:

						超时时间：#getTimeout

							TIMEOUT_DEFAULT = -1

						是否只读：#isReadOnly

					2 TransactionDefinition相关实现

						默认实现类： org.springframework.transaction.support.DefaultTransactionDefinition

						编程式事务管理的模板方法类： org.springframework.transaction.support.TransactionTemplate

						声明式事务管理类： org.springframework.transaction.interceptor.TransactionAttribute

							默认实现： org.springframework.transaction.interceptor.DefaultTransactionAttribute

				19.2.2 TransactionStatus
				
				19.2.3 PlatformTransactionManager

					1. PlatformTransactionManager实现类概览

					2. 窥一斑而知全豹

			19.3 小结

		第20章　使用Spring进行事务管理　						// done 2020-8-12 22:25:30						

			20.1 编程式事务管理

				20.1.1 直接使用PlatformTransactionManager进行编程式事务管理

				20.1.2 使用TransactionTemplate进行编程式事务管理

				20.1.3 编程创建基于Savapoint的嵌套事务

			20.2 声明式事务管理

				20.2.1 引子

				20.2.2 XML元数据驱动的声明式事务

					1. 使用ProxyFactory(ProxyFactoryBean) + TransactionInterceptor

					2. 使用“一站式”的TransactionProxyFactoryBean

					3. 使用BeanNameAutoProxyCreator

					4. 使用Spring2.0的声明事务配置方式

				20.2.3 注解元数据驱动的声明式事务

					@Transactional

					xml: <tx:annotation-driven transaction-manager="transactionManager">	

			20.3 小结

		第21章　Spring事务管理之扩展篇　						// done 2020-8-12 23:25:12				

			21.1 理解并活用ThreadLocal

				21.1.1 理解ThreadLocal的存在背景

					目的： 通过避免对象的共享来保证应用程序实现中的线程安全。

				21.1.2 理解ThreadLocal的实现

				21.1.3 ThreadLocal的应用场景

					- 管理应用程序实现中的线程安全： 对于某些有状态的或者非线程安全的对象，在多线程程序中为每个线程都分配相应的副本，而不是让多线程共享该对象。

						如： JDBC中的Connection

					- 实现当前程序执行流程内的数据传递

						如： 跟踪线程内的日志序列。

					- 某些情况下的性能优化： 有些情况下，系统中一些没有必要共享的对象被设置成了共享，为了保证应用程序的线程安全以及对象状态的正确，我们往往就得通过同步
					等方式对多线程的访问进行管理和控制。

					- per-thread Singleton： 当某些资源的初始化代价有些大，并且整个执行流程中还会多次访问，为了避免在访问时每次都需要去初始化该资源，可以第一次初始化
					完成之后，直接通过ThreadLocal将其绑定到当前线程，之后，所有对该资源的访问都从当前线程获取即可。

				21.1.4 使用ThreadLocal管理多数据源切换的条件
				
			21.2 谈Strategy模式在开发过程中的应用
			
				- 本部分的事务抽象框架

				- Ioc bean实例化策略： InstantiationStrategy -> CglibSubclassingInstantiationStrategy | SimpleInstantiationStrategy

				- Spring Validation框架： Validator -> ... | ...

				- jakarta commons logging: Log -> Jdk14Logger | Log4jLogger | SimpleLog

			21.3 Spring与JTA背后的奥秘
			
			21.4 小结	

	第六部分　Spring的Web MVC框架 			 				// done 2020-8-19 22:44:32				

		第22章　迈向Spring MVC的旅程　						// done 2020-8-15 11:32:56	
		
			22.1 Servlet独行天下的时代

			22.2 繁盛一时的JSP时代

			22.3 Servlet与JSP的结盟

			22.4 数英雄人物，还看今朝

				请求驱动的Web框架： Struts, WebWork, Spring MVC

				事件驱动的Web框架： Tapestry, JSF

			22.5 小结


		第23章　Spring MVC初体验　							// done 2020-8-15 13:04:46

			23.1 鸟瞰Spring MVC

				DispatcherServlet的处理流程：

					1. HandlerMapping先生（Web请求的处理协调人）

					2. org.springframework.web.servlet.Controller（Web请求的具体处理者）

					3. ViewResolver和View（视图独立战争的领导者）


				DispatcherServlet 		HandlerMapping 		Controller 					ViewResolver 		View

						1.getHandler(request)
							_________\

							return Controller
							_ _ _ _ _ _
							\

							2.handlerRequest(request, response)
						________________________________________\	

																2.1 new()
																___________\ ModelAndView
					
								return ModelAndView
						/_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _


							3. resolveViewName(viewName.Locale)
						_______________________________________________________________________\

								return view
						/_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

														4. render(model, request, response)
						_______________________________________________________________________________________\



			23.2 实践出真知

				23.2.1 Spring MVC 应用的物理结构

					1. ContextLoaderListener与/WEB-INF/applicationContext.xml

					2. DispatcherServlet与XXX-servlet.xml

				23.2.2 按部就班的开始工作
			
			23.3 小结


		第24章　近距离接触Spring MVC主要角色　 					// doen 2020-8-18 00:14:22

			24.1 忙碌的协调人 HandlerMapping

				24.1.1 可用的 HandlerMapping

				24.1.2 HandlerMapping执行序列（Chain of HandlerMapping）

			24.2 我们的亲密伙伴 Controller

				24.2.1 AbstractController
				
				24.2.2 MultiActionController
				
				24.2.3 SimpleFormController
				
					1. 了解数据绑定

						org.springframework.beans.BeanWrapperImpl

						java.beans.PropertyEditor

						org.springframework.validation.DataBinder

					2. 	Spring框架数据验证简介

						org.springframework.validation.Validator

						org.springframework.validation.Errors

				24.2.4 AbstractWizardFormController
				
				24.2.5 其他可用的Controller实现

			24.3 ModelAndView

				24.3.1 ModelAndView中的视图信息

					org.springframework.web.servlet.View

				24.3.2 ModelAndView中的数据模型

					org.springframework.ui.ModelMap

			24.4 视图定位器 ViewResolver

				24.4.1 可用的ViewResolver实现类

					1. 面向单一视图类型的ViewResolver

						org.springframework.web.servlet.view.InternalResourceViewResolver

						org.springframework.web.servlet.view.freemarker.FreeMarkerViewResolver

						org.springframework.web.servlet.view.groovy.GroovyMarkupViewResolver

						org.springframework.web.servlet.view.xslt.XsltViewResolver

					2. 面向多视图类型的ViewResolver

						org.springframework.web.servlet.view.ResourceBundleViewResolver

						org.springframework.web.servlet.view.XmlViewResolver

						org.springframework.web.servlet.view.BeanNameViewResolver
				
				24.4.2 ViewResolver查找序列（Chain of ViewResolver）
				
			24.5 各司其职的 View

				24.5.1 View实现原理回顾

				24.5.2 可用的View实现类

					1. 使用JSP技术的View实现

						org.springframework.web.servlet.view.InternalResourceView

						org.springframework.web.servlet.view.JstlView

						org.springframework.web.servlet.view.tiles3.TilesView

					2. 使用通用模板技术的View实现

						org.springframework.web.servlet.view.freemarker.FreeMarkerView

						org.springframework.web.servlet.view.groovy.GroovyMarkupView

					3. 使用二进制文档格式的View实现

						org.springframework.web.servlet.view.document.AbstractPdfView

						org.springframework.web.servlet.view.document.AbstractXlsView

						org.springframework.web.servlet.view.document.AbstractXlsxView

				24.5.3 自定义View实现

			24.6 小结

		第25章　认识更多Spring MVC家族成员　					// done 2020-8-18 23:13:45
		
			25.1 文件上传与MultipartResolver
				
				25.1.1 使用MultipartResolver进行文件上传的简单分析

				25.1.2 文件上传实践

			25.2 Handler与HandlerAdaptor

				25.2.1 问题的起源

				25.2.2 深入了解Handler

				25.2.3 近看HandlerAdaptor的奥秘

				25.2.4 告知Handler与HandlerAdapator的存在

			25.3 框架内处理流程拦截与HandlerInterceptor

				25.3.1 可用的HandlerInterceptor实现

				25.3.2 自定义实现HandlerInterceptor

				25.3.3 HandlerInterceptor寻根

				25.3.4 HandlerInterceptor之外的选择

			25.4 框架内的异常处理与HandlerExceptionResolver

			25.5 国际化视图与LocaleResolver

				25.5.1 可用的LocaleResolver

				25.5.2 LocaleResolver的足迹

				25.5.3 Locale的变更与LocalChangeHandler

			25.6 主题（Theme）与ThemeResolver
			
				25.6.1 提供主题资源的ThemeSource

				25.6.2 管理主题的ThemeResolver

				25.6.3 切换主题的ThemeChangeInterceptor

			25.7 小结

		第26章　Spring MVC中基于注解的Controller　 			// done 2020-8-19 22:41:52

			26.1 初识基于注解的Controller

			26.2 基于注解的Controller原型分析

				26.2.1 自定义基于注解的Controller的HandleMapping

					org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping

				26.2.2 自定义基于注解的Controller的HandleAdaptor

					org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter

			26.3 近看基于注解的Controller

				26.3.1 声明基于注解Controller

					1. 再谈@Controller

					2. @RequsetMapping详解

					3. 请求处理方法签名规则说明

				26.3.2 请求参数到方法参数的绑定

					1. 默认绑定行为

					2. 使用@RequestParam明确地绑定关系

					3. 添加自定义数据绑定规则

						- 使用@InitBinder标注的初始化方法

						- 指定自定义的WebBindingInitializer

				26.3.3 使用@ModelAttribute访问模型数据

			26.4 小结

		第27章　Spring MVC之扩展篇　						// done 2020-8-19 22:43:49

			27.1 Spring MVC 也 Convertion Over Configuration

 				27.1.1 Convertion Over Configuration简介

 					约定大于配置

 				27.1.2 Spring MVC 中的 Convertion Over Configuration	

			27.2 Spring 3.0 展望

			27.3 小结

	第七部分　Spring框架对J2EE服务的集成和支持

		第28章　Spring框架内的JNDI支持　						// done 2020-8-24 22:56:31
		
			28.1 JNDI简单回顾

				JNDI: Java Naming and Directory Interface, Java命名与目录接口

			28.2 Spring框架内JNDI访问的基石————JndiTemplate

			28.3 JNDI对象的依赖注入————JndiObjectFactoryBean

			28.4 小结

		第29章　Spring框架对JMS的集成　 						// done 2020-8-24 23:00:37
		
			29.1 说说JMS的身世

			29.2 使用JMS API进行应用开发的传统套路

			29.3 Spring改进后的JMS实战格斗术

				29.3.1 消息发送和同步接收

					1. JmsTemplate亲密接触

					2. 同步消息处理场景浅析

				29.3.2 异步消息接收

					1. 了解MessageListenerContainer

					2. 消息驱动POJO

				29.3.3 JMS相关异常处理

				29.3.4 框架内的事务管理支持

			29.4 小结

		第30章　使用Spring发送E-mail　						// done 2020-8-24 23:03:27
		
			30.1 思甜前，先忆苦

			30.2 Spring的E-mail抽象层分析

				30.2.1 直接创建邮件消息并发送

				30.2.2 使用MimeMessagePreparator发送邮件

			30.3 Spring的E-mail支持在实际开发中的应用

			30.4 小结

		第31章　Spring中的任务调度和线程池支持　				// done 2020-8-24 23:10:16

			31.1 Spring与Quartz	

				31.1.1 初始Quartz

				31.1.2 融入Spring大家庭的Quartz

					1. Job的实现策略

					2. JobDetail的更多选择

					3. Trigger的可配置化

					4. Scheduler的新家

			31.2 Spring对JDK Timer的集成

				31.2.1 JDK Timer小记

				31.2.2 Spring集成后的 JDK Timer

					1. 逃离TimerTask的魔咒

					2. TimerTask模块化封装————ScheduledTimeTask

			31.3 Executor的孪生兄弟TaskExecutor

				31.3.1 可用的TaskExecutor

					1. SyncTaskExecutor

					2. SimpleSyncTaskExecutor

					3. ThreadPoolTaskExecutor

					4. ConcurrentTaskExecutor

					5. TimerTaskExecutor、 SimpleThreadPoolTaskExecutor和WorkManagerTaskExecutor

				31.3.2 TaskExecutor使用示例

			31.4 小结

		第32章　Spring框架对J2EE服务的集成之扩展篇　			// done 2020-8-24 23:13:17
			
			32.1 MailMonitor的延伸

			32.2 Spring3.0展望

			32.3 小结

		第33章　Spring远程方案								// done 2020-8-24 23:45:43

			33.1 从“对面交谈”到“千里传声”

			33.2 Spring Remoting架构分析

				33.2.1 Spring Remoting之远程访问异常体系

				33.2.2 统一风格的远程服务公开和访问方式

					Server Accessor:

						org.springframework.remoting.rmi.RmiProxyFactoryBean

						org.springframework.remoting.httpinvoker.HttpInvokerProxyFactoryBean

						org.springframework.remoting.caucho.HessianProxyFactoryBean

					Server Exporter: 								

						org.springframework.remoting.rmi.RmiServiceExporter

						org.springframework.remoting.httpinvoker.HttpInvokerServiceExporter

						org.springframework.remoting.caucho.HessianServiceExporter

			33.3 Spring Remoting提供的远程服务支持

				33.3.1 基于 RMI 的 Remoting方案
				
				33.3.2 基于 HTTP 的轻量级 Remoting方案

				33.3.3 基于 Web服务 的 Remoting方案

				33.3.3 基于 JMS 的 Remoting方案
			
			33.4 扩展 Spring Remoting
			
			33.5 Spring Remoting之扩展篇

				33.5.1 拉开JMX演出的序幕

				33.5.2 Spring 3.0 展望
