Netty学习笔记：

	简介: 
	 	Netty is an asynchronous event-driven network application framework 
	    for rapid development of maintainable high performance protocol servers & clients.

	官网: https://netty.io/

		User guide: https://netty.io/wiki/user-guide-for-4.x.html#wiki-h3-17 			// done 2020-10-17 17:36:05

		All documentation: https://netty.io/wiki/all-documents.html

	Git: https://github.com/netty/netty	

	本地: D:\workspace\GitHub\netty-4.1

	书籍:
		《Netty in Action》 								// start 2020-10-20 08:00

			PART1 GETTING STARTED

				1. Netty and Java NIO APIs
				2. Your first Netty Application
				3. Netty from the ground up

			PART2: CORE FUNCTIONS/PARTS	

				4. Transports 							// done 2020-10-28 22:22:56
				5. Buffers
				6. ChannelHandler 						// done 2020-11-1 11:18:34
				7. Codec 								// done 2020-11-1 11:54:59
				8. Provided ChannelHandlers and codecs	// done 2020-11-1 16:44:57
				9. Bootstrapping Netty applications		// done 2020-11-1 18:11:50
				10. Unit-test your code 				// done 2020-11-1 18:41:47
				11. WebSockets
				12. SPDY
				13. Broadcasting events via UDP 		// done 2020-11-2 17:25:06
				14. Implement a custom codec 			// done 2020-11-2 20:54:41
				15. Choosing the right thread model 	// done 2020-11-2 21:38:27
				16. De-register / Re-register with EventLoop 	// done 2020-11-2 21:57:50


		《Netty权威置南》

	视频:
		# 尚硅谷Netty视频教程（2019发布） https://www.bilibili.com/video/BV1DJ411m7NR		// start 2020-10-17 09:00:00 	done 2020-10-26 22:21 

			P1 001_尚硅谷_课程说明和要求 19:16
			P2 002_尚硅谷_Netty是什么 12:11 
			P3 003_尚硅谷_应用场景和学习资料 07:10 
			P4 004_尚硅谷_IO模型 28:49 
			P5 005_尚硅谷_BIO 介绍说明 06:36
			P6 006_尚硅谷_BIO实例及分析 28:23
			P7 007_尚硅谷_BIO内容梳理小结 02:43
			P8 008_尚硅谷_NIO介绍说明 13:24
			P9 009_尚硅谷_NIO的Buffer基本使用 10:29
			P10 010_尚硅谷_NIO三大核心组件关系 15:23 		// done 2020-10-17 10:00:00	

			P11 011_尚硅谷_Buffer的机制及子类 24:37
			P12 012_尚硅谷_Channel基本介绍 12:41
			P13 013_尚硅谷_Channel应用实例1 13:49
			P14 014_尚硅谷_Channel应用实例2 11:24
			P15 015_尚硅谷_Channel应用实例3 18:33
			P16 016_尚硅谷_Channel拷贝文件 05:40 
			P17 017_尚硅谷_Buffer类型化和只读 12:46 
			P18 018_尚硅谷_MappedByteBuffer使用 13:07 
			P19 019_尚硅谷_Buffer的分散和聚集 24:23 
			P20 020_尚硅谷_Channel和Buffer梳理 07:54	 	// done 2020-10-18 11:00:00

			P21 021_尚硅谷_Selector介绍和原理 06:45 
			P22 022_尚硅谷_Selector API介绍 13:36 
			P23 023_尚硅谷_SelectionKey在NIO体系 13:07 
			P24 024_尚硅谷_NIO快速入门(1) 27:39 
			P25 025_尚硅谷_NIO快速入门(2) 14:26 
			P26 026_尚硅谷_NIO快速入门小结 05:25 
			P27 027_尚硅谷_SelectionKey API 13:26 
			P28 028_尚硅谷_SocketChannel API 05:51 
			P29 029_尚硅谷_NIO 群聊系统(1) 18:06 
			P30 030_尚硅谷_NIO 群聊系统(2) 18:37 
			P31 031_尚硅谷_NIO 群聊系统(3) 15:47 
			P32 032_尚硅谷_NIO 群聊系统(4) 22:33 
			P33 033-_尚硅谷_零拷贝原理剖析 18:20 
			P34 034_尚硅谷_零拷贝应用实例 22:47 
			P35 035_尚硅谷_零拷贝AIO内容梳理 14:09 		// done 2020-10-19 21:53:34

			P36 036_尚硅谷_Netty概述 14:15 
			P37 037_尚硅谷_线程模型概述 09:32 
			P38 038_尚硅谷_Reactor模式图解剖析 20:31 
			P39 039_尚硅谷_单Reactor单线程模式 13:36 
			P40 040_尚硅谷_单Reactor多线程模式 14:08 
			P41 041_尚硅谷_主从Reactor模式 21:38 
			P42 042_尚硅谷_Netty模型-通俗版 11:25 
			P43 043_尚硅谷_Netty模型-详细版 17:00 
			P44 044_尚硅谷_Netty入门-服务端1 26:07 
			P45 045_尚硅谷_Netty入门-服务端2 15:40 
			P46 046_尚硅谷_Netty入门-客户端 17:04 		// done 2020-10-20 22:34:55

			P47 047_尚硅谷_Netty案例源码分析 22:16 
			P48 048_尚硅谷_Netty模型梳理 13:59 
			P49 049_尚硅谷_taskQueue自定义任务 17:56 
			P50 050_尚硅谷_scheduledTaskQueue 12:16 
			P51 051_尚硅谷_异步模型原理剖析 13:47 
			P52 052_尚硅谷_FutureListener机制 05:23 
			P53 053_尚硅谷_Http服务程序实例 28:03 
			P54 054_尚硅谷_Http服务过滤资源 12:49 
			P55 055_尚硅谷_阶段内容梳理 08:34 
			P56 056_尚硅谷_Netty核心模块(1) 09:06 
			P57 057_尚硅谷_Netty核心模块(2) 13:18 
			P58 058_尚硅谷_pipeline组件剖析 13:35 
			P59 059_尚硅谷_Netty核心模块梳理 06:19 
			P60 060_尚硅谷_EventLoop组件 22:45 			// done 2020-10-21 22:22:08

			P61 061_尚硅谷_Unpooled应用实例1 14:57 
			P62 062_尚硅谷_Unpooled应用实例2 15:16 
			P63 063_尚硅谷_Netty群聊系统服务端 36:14 		// done 2020-10-22 08:30:31

			P64 064_尚硅谷_Netty群聊系统客户端 18:13 
			P65 065_尚硅谷_Netty私聊实现思路 06:08 
			P66 066_尚硅谷_Netty心跳机制实例 16:57 
			P67 067_尚硅谷_Netty心跳处理器 13:46 
			P68 068_尚硅谷_WebSocket长连接开发1 14:12 
			P69 069_尚硅谷_WebSocket长连接开发2 09:34 
			P70 070_尚硅谷_WebSocket长连接开发3 18:38 
			P71 071_尚硅谷_WebSocket长连接开发4 03:49 
			P72 072_尚硅谷_核心模块内容梳理 11:17 
			P73 073_尚硅谷_netty编解码器机制简述 07:12 
			P74 074_尚硅谷_ProtoBuf机制简述 10:04 
			P75 075_尚硅谷_ProtoBuf实例-生成类 15:05 
			P76 076_尚硅谷_ProtoBuf实例Codec使用 14:43 
			P77 077_尚硅谷_ProtoBuf传输多种类型 26:32 
			P78 078_尚硅谷_ProtoBuf内容小结 07:53 		// done 2020-10-24 13:20:07

			P79 079_尚硅谷_Netty入站与出站机制 25:31 
			P80 080_尚硅谷_Handler链调用机制实例1 12:53 
			P81 081_尚硅谷_Handler链调用机制实例2 18:29 
			P82 082_尚硅谷_Handler链调用机制实例3 16:14 
			P83 083_尚硅谷_Handler链调用机制实例4 15:40 
			P84 084_尚硅谷_Netty其它常用编解码器 09:16 
			P85 085_尚硅谷_Log4j 整合到Netty 04:49 
			P86 086_尚硅谷_编解码器和处理器链梳理 12:14  	// done 2020-10-24 16:05:05


			P87 087_尚硅谷_Tcp粘包拆包原理 05:24 			// done 2020-10-24 17:29:18
			P88 088_尚硅谷_Tcp粘包拆包实例演示 24:16 
			P89 089_尚硅谷_自定义协议解决TCP粘包拆包1 26:28 
			P90 090_尚硅谷_自定义协议解决TCP粘包拆包2 10:18 
			P91 091_尚硅谷_TCP粘包拆包内容梳理 08:04 

			P92 092_尚硅谷_Netty服务器启动源码剖析1 25:08 
			P93 093_尚硅谷_Netty服务器启动源码剖析2 06:27 
			P94 094_尚硅谷_Netty服务器启动源码剖析3 23:23 
			P95 095_尚硅谷_Netty接收请求源码剖析1 22:26 	// done 2020-10-25 10:01:23
			P96 096_尚硅谷_Netty接收请求源码剖析2 06:24 
			P97 097_尚硅谷_Netty接收请求源码剖析3 07:49 
			P98 098_尚硅谷_Pipeline源码剖析 23:12 
			P99 099_尚硅谷_ChannelHandler源码剖析 07:10 
			P100 100_尚硅谷_管道 处理器 上下文创建源码剖析 14:36 
			P101 101_尚硅谷_Pipeline调用Handler源码剖析 18:10 
			P102 102_尚硅谷_三大核心组件剖析梳理 04:52 	// done 2020-10-25 11:03:38

			P103 103_尚硅谷_Netty心跳源码剖析1 14:18 
			P104 104_尚硅谷_Netty心跳源码剖析2 22:45 
			P105 105_尚硅谷_EventLoop源码剖析1 22:12 
			P106 106_尚硅谷_EventLoop源码剖析2 05:34 		// done 2020-10-25 14:01:07
			P107 107_尚硅谷_任务加入异步线程池源码剖析1 13:17 
			P108 108_尚硅谷_任务加入异步线程池源码剖析2 22:06 
			P109 109_尚硅谷_任务加入异步线程池源码剖析3 13:42 

			P110 110_尚硅谷_RPC调用流程分析 10:11 
			P111 111_尚硅谷_用Netty实现DubboRPC-1 12:38 
			P112 112_尚硅谷_用Netty实现DubboRPC-2 07:38 
			P113 113_尚硅谷_用Netty实现DubboRPC-3 19:03 
			P114 114_尚硅谷_用Netty实现DubboRPC-4 15:07 
			P115 115_尚硅谷_用Netty实现DubboRPC-5 19:40 
			P116 116_尚硅谷_用Netty实现DubboRPC-6 20:19 	// done 2020-10-26 22:20:31