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
		《Netty实战》
		《Netty权威置南》

	视频:
		# 尚硅谷Netty视频教程（2019发布） https://www.bilibili.com/video/BV1DJ411m7NR		// start 2020-10-17 09:00:00
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