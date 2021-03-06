《The Java® Virtual Machine Specification Java SE 8 Edition》 Java8虚拟机规范 		// start 2020-9-12 18:07:48  done 2020-9-16 22:50:07

Preface to the Java SE 8 Edition xiii

	1 Introduction 1 															// done 2020-9-12 18:40:28

		1.1 A Bit of History 1
		1.2 The Java Virtual Machine 2
		1.3 Organization of the Specification 3
		1.4 Notation 4
		1.5 Feedback 4
		
	2 The Structure of the Java Virtual Machine 5 								// done 2020-9-13 17:37:20

		2.1 The class File Format 5
		2.2 Data Types 6
		2.3 Primitive Types and Values 6
			2.3.1 Integral Types and Values 7
			2.3.2 Floating-Point Types, Value Sets, and Values 8
			2.3.3 The returnAddress Type and Values 10
			2.3.4 The boolean Type 10 											// done 2020-9-13 09:39:57
		2.4 Reference Types and Values 11
		2.5 Run-Time Data Areas 11
			2.5.1 The pc Register 12
			2.5.2 Java Virtual Machine Stacks 12
			2.5.3 Heap 13
			2.5.4 Method Area 13
			2.5.5 Run-Time Constant Pool 14
			2.5.6 Native Method Stacks 14
		2.6 Frames 15
			2.6.1 Local Variables 16
			2.6.2 Operand Stacks 17
			2.6.3 Dynamic Linking 18
			2.6.4 Normal Method Invocation Completion 18
			2.6.5 Abrupt Method Invocation Completion 18
		2.7 Representation of Objects 19
		2.8 Floating-Point Arithmetic 19
			2.8.1 Java Virtual Machine Floating-Point Arithmetic and IEEE 754 19
			2.8.2 Floating-Point Modes 20
			2.8.3 Value Set Conversion 20
		2.9 Special Methods 22
		2.10 Exceptions 23 														// done 2020-9-13 11:39:29
		2.11 Instruction Set Summary 25 										// done 2020-9-13 17:30:06
			2.11.1 Types and the Java Virtual Machine 26 						
			2.11.2 Load and Store Instructions 29
			2.11.3 Arithmetic Instructions 30
			2.11.4 Type Conversion Instructions 32
			2.11.5 Object Creation and Manipulation 34
			2.11.6 Operand Stack Management Instructions 34
			2.11.7 Control Transfer Instructions 34
			2.11.8 Method Invocation and Return Instructions 35
			2.11.9 Throwing Exceptions 36
			2.11.10 Synchronization 36
		2.12 Class Libraries 37
		2.13 Public Design, Private Implementation 37
		
	3 Compiling for the Java Virtual Machine 39 								// done 2020-9-13 19:00:39

		3.1 Format of Examples 39
		3.2 Use of Constants, Local Variables, and Control Constructs 40
		3.3 Arithmetic 45
		3.4 Accessing the Run-Time Constant Pool 46
		3.5 More Control Examples 47
		3.6 Receiving Arguments 50
		3.7 Invoking Methods 51
		3.8 Working with Class Instances 53
		3.9 Arrays 55
		3.10 Compiling Switches 57
		3.11 Operations on the Operand Stack 59
		3.12 Throwing and Handling Exceptions 60
		3.13 Compiling finally 63
		3.14 Synchronization 66
		3.15 Annotations 67
		
	4 The class File Format 69 													// done 2020-9-15 21:33:14

		4.1 The ClassFile Structure 70
		4.2 The Internal Form of Names 74
			4.2.1 Binary Class and Interface Names 74
			4.2.2 Unqualified Names 75
		4.3 Descriptors 75
			4.3.1 Grammar Notation 75
			4.3.2 Field Descriptors 76
			4.3.3 Method Descriptors 77
		4.4 The Constant Pool 78
			4.4.1 The CONSTANT_Class_info Structure 79
			4.4.2 The CONSTANT_Fieldref_info, CONSTANT_Methodref_info, and CONSTANT_InterfaceMethodref_info Structures 80
			4.4.3 The CONSTANT_String_info Structure 81
			4.4.4 The CONSTANT_Integer_info and CONSTANT_Float_info Structures 82
			4.4.5 The CONSTANT_Long_info and CONSTANT_Double_info Structures 83
			4.4.6 The CONSTANT_NameAndType_info Structure 85
			4.4.7 The CONSTANT_Utf8_info Structure 85
			4.4.8 The CONSTANT_MethodHandle_info Structure 87
			4.4.9 The CONSTANT_MethodType_info Structure 89
			4.4.10 The CONSTANT_InvokeDynamic_info Structure 89
		4.5 Fields 90
		4.6 Methods 92 															// done 2020-9-14 21:47:39				
		4.7 Attributes 95 														// done 2020-9-14 23:58:31
			4.7.1 Defining and Naming New Attributes 101
			4.7.2 The ConstantValue Attribute 101
			4.7.3 The Code Attribute 102
			4.7.4 The StackMapTable Attribute 106
			4.7.5 The Exceptions Attribute 113
			4.7.6 The InnerClasses Attribute 114
			4.7.7 The EnclosingMethod Attribute 117
			4.7.8 The Synthetic Attribute 118
			4.7.9 The Signature Attribute 119
				4.7.9.1 Signatures 120
			4.7.10 The SourceFile Attribute 123
			4.7.11 The SourceDebugExtension Attribute 124
			4.7.12 The LineNumberTable Attribute 125 							// done 2020-9-14 23:07:40
			4.7.13 The LocalVariableTable Attribute 126
			4.7.14 The LocalVariableTypeTable Attribute 128
			4.7.15 The Deprecated Attribute 130
			4.7.16 The RuntimeVisibleAnnotations Attribute 131
				4.7.16.1 The element_value structure 132
			4.7.17 The RuntimeInvisibleAnnotations Attribute 135
			4.7.18 The RuntimeVisibleParameterAnnotations Attribute 136
			4.7.19 The RuntimeInvisibleParameterAnnotations Attribute 138
			4.7.20 The RuntimeVisibleTypeAnnotations Attribute 139
				4.7.20.1 The target_info union 145
				4.7.20.2 The type_path structure 149
			4.7.21 The RuntimeInvisibleTypeAnnotations Attribute 153
			4.7.22 The AnnotationDefault Attribute 154
			4.7.23 The BootstrapMethods Attribute 155
			4.7.24 The MethodParameters Attribute 157
		4.8 Format Checking 159 												// done 2020-9-14 23:58:31
		4.9 Constraints on Java Virtual Machine Code 160 						// done 2020-9-15 20:31:12
			4.9.1 Static Constraints 160
			4.9.2 Structural Constraints 164
		4.10 Verification of class Files 167 									// done 2020-9-15 21:29:56
			4.10.1 Verification by Type Checking 168
				4.10.1.1 Accessors for Java Virtual Machine Artifacts 171
				4.10.1.2 Verification Type System 175
				4.10.1.3 Instruction Representation 178
				4.10.1.4 Stack Map Frame Representation 180
				4.10.1.5 Type Checking Abstract and Native Methods 185
				4.10.1.6 Type Checking Methods with Code 188
				4.10.1.7 Type Checking Load and Store Instructions 197
				4.10.1.8 Type Checking for protected Members 199
				4.10.1.9 Type Checking Instructions 202
			4.10.2 Verification by Type Inference 322
				4.10.2.1 The Process of Verification by Type Inference 322
				4.10.2.2 The Bytecode Verifier 322
				4.10.2.3 Values of Types long and double 326
				4.10.2.4 Instance Initialization Methods and Newly Created Objects 326
				4.10.2.5 Exceptions and finally 328
		4.11 Limitations of the Java Virtual Machine 330 						// done 2020-9-15 21:33:06
		
	5 Loading, Linking, and Initializing 333 									// done 2020-9-15 23:45:32

		5.1 The Run-Time Constant Pool 333
		5.2 Java Virtual Machine Startup 336
		5.3 Creation and Loading 336 											// done 2020-9-15 22:36:34
			5.3.1 Loading Using the Bootstrap Class Loader 338
			5.3.2 Loading Using a User-defined Class Loader 339
			5.3.3 Creating Array Classes 340
			5.3.4 Loading Constraints 340
			5.3.5 Deriving a Class from a class File Representation 342
		5.4 Linking 343
			5.4.1 Verification 344
			5.4.2 Preparation 344
			5.4.3 Resolution 345
				5.4.3.1 Class and Interface Resolution 346
				5.4.3.2 Field Resolution 347
				5.4.3.3 Method Resolution 348
				5.4.3.4 Interface Method Resolution 350
				5.4.3.5 Method Type and Method Handle Resolution 351
				5.4.3.6 Call Site Specifier Resolution 355
			5.4.4 Access Control 356
			5.4.5 Overriding 356
		5.5 Initialization 357
		5.6 Binding Native Method Implementations 360
		5.7 Java Virtual Machine Exit 360
		
	6 The Java Virtual Machine Instruction Set 361

		6.1 Assumptions: The Meaning of "Must" 361
		6.2 Reserved Opcodes 362
		6.3 Virtual Machine Errors 362
		6.4 Format of Instruction Descriptions 363 								// done 2020-9-16 22:44:04
			mnemonic 364
		6.5 Instructions 366 													// pass 指令集说明，暂时略过，需要时查看
			aaload 367
			aastore 368
			aconst_null 370
			aload 371
			aload_<n> 372
			anewarray 373
			areturn 374
			arraylength 375
			astore 376
			astore_<n> 377
			athrow 378
			baload 380
			bastore 381
			bipush 382
			caload 383
			castore 384
			checkcast 385
			d2f 387
			d2i 388
			d2l 389
			dadd 390
			daload 392
			dastore 393
			dcmp<op> 394
			dconst_<d> 396
			ddiv 397
			dload 399
			dload_<n> 400
			dmul 401
			dneg 403
			drem 404
			dreturn 406
			dstore 407
			dstore_<n> 408
			dsub 409
			dup 410
			dup_x1 411
			dup_x2 412
			dup2 413
			dup2_x1 414
			dup2_x2 415
			f2d 417
			f2i 418
			f2l 419
			fadd 420
			faload 422
			fastore 423
			fcmp<op> 424
			fconst_<f> 426
			fdiv 427
			fload 429
			fload_<n> 430
			fmul 431
			fneg 433
			frem 434
			freturn 436
			fstore 437
			fstore_<n> 438
			fsub 439
			getfield 440
			getstatic 442
			goto 444
			goto_w 445
			i2b 446
			i2c 447
			i2d 448
			i2f 449
			i2l 450
			i2s 451
			iadd 452
			iaload 453
			iand 454
			iastore 455
			iconst_<i> 456
			idiv 457
			if_acmp<cond> 458
			if_icmp<cond> 459
			if<cond> 461
			ifnonnull 463
			ifnull 464
			iinc 465
			iload 466
			iload_<n> 467
			imul 468
			ineg 469
			instanceof 470
			invokedynamic 472
			invokeinterface 477
			invokespecial 481
			invokestatic 486
			invokevirtual 489
			ior 494
			irem 495
			ireturn 496
			ishl 497
			ishr 498
			istore 499
			istore_<n> 500
			isub 501
			iushr 502
			ixor 503
			jsr 504
			jsr_w 505
			l2d 506
			l2f 507
			l2i 508
			ladd 509
			laload 510
			land 511
			lastore 512
			lcmp 513
			lconst_<l> 514
			ldc 515
			ldc_w 517
			ldc2_w 519
			ldiv 520
			lload 521
			lload_<n> 522
			lmul 523
			lneg 524
			lookupswitch 525
			lor 527
			lrem 528
			lreturn 529
			lshl 530
			lshr 531
			lstore 532
			lstore_<n> 533
			lsub 534
			lushr 535
			lxor 536
			monitorenter 537
			monitorexit 539
			multianewarray 541
			new 543
			newarray 545
			nop 547
			pop 548
			pop2 549
			putfield 550
			putstatic 552
			ret 554
			return 555
			saload 556
			sastore 557
			sipush 558
			swap 559
			tableswitch 560
			wide 562
	
	7 Opcode Mnemonics by Opcode 565 											// pass 指令目录A-Z，需要时查看 2020-9-16 22:48:38
		Index 569
		A Limited License Grant 587