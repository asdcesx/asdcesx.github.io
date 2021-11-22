## 概述

###  01java语言概述
	* A: java语言概述
		* a: Java是sun公司开发的一门编程语言,目前被Oracle公司收购，编程语言就是用来编写软件的。
		* b: Java的应用
			* 开发QQ、迅雷程序(桌面应用软件)
			* 淘宝、京东(互联网应用软件)
		* c: Java的擅长
			* 互联网：电商、P2P等等
			* 企业级应用：ERP、CRM、BOS、OA等等
		* d: Java语言平台
			* JavaSE（标准版）部分,基础班学习JavaSE,JavaSE并不能开发大型项目。
			* JavaEE（企业版）部分,就业班学习JavaEE,学习完JavaEE部分就可以开发各种大型项目了。
## 基本配置
	
###  02常用的DOS命令
	* A: 常用的DOS命令
		* a: 打开Dos控制台
			* win+r--cmd--回车			
		* b: 常用dos命令
			* cd.. : 退回到上一级目录
			* cd\  : 退回到根目录
			* cd tools: 进入tools文件夹
			* d:   : 回车	盘符切换
			* cd d:\234 :进入d盘的234文件夹,再切换盘符(d:)才能进入d:\234
			* dir  : 列出当前目录下的文件以及文件夹
			* cls  : 清除屏幕
			* ipconfig: 查看本机的相关网络配置
		* c: dos控制台运行记事本程序
			* D:\>C:\windows\notepad.exe
			* 还可以省略“.exe”后缀，例如：D:\>C:\windows\notepad
			
			
###  03java语言开发环境JDK
	* A: java语言开发环境JDK
		* a: JDK是Java开发环境
		* b: 课程中使用的JDK版本是JDK7，当前最新版本是JDK8

	

###  04JDK的下载和安装
	* A: JDK的下载
		* a: 官网 http://www.oracle.com/cn/index.html
		* b: 演示下载流程
	* B: JDK的安装
		* a: 傻瓜式安装
			* 双击安装程序，然后一路next即可(但是不建议)
		* b: 安装的推荐方式
			* 安装路径不要有中文或者特殊符号如空格等。
			* 所有和开发相关的软件最好安装目录统一。
				* 举例：我的JDK安装路径
					* D:\develop\Java\jdk1.7.0_72
			* 当提示安装JRE时，可以选择不安装。建议还是安装上。
					* D:\develop\Java\jre\
			* 安装路径中没有的文件夹,会自动创建
			
	* C: 验证安装是否成功
		* a:通过DOS命令，切换到JDK安装的bin目录下。
			* D:\develop\Java\jdk1.7.0_72\bin
		* b:然后分别输入javac和java，如果正常显示一些内容，说明安装成功

###  05JDK和JRE跨平台
	* A: JDK与JRE的关系
		* a: JDK：它是Java开发运行环境，在程序员的电脑上当然要安装JDK；
		* b: JRE：Java Runtime Environment它是Java运行环境，如果你不需要开发只需要运行Java程序，那么你可以安装JRE。例如程序员开发出的程序最终卖给了用户，用户不用开发，只需要运行程序，所以用户在电脑上安装JRE即可。
		* c: JDK包含了JRE。
	* B: 跨平台特性
		* a: 平台指的是操作系统 （Windows，Linux，Mac）。
		* b: Java程序可以在任意操作系统上运行，一次编写到处运行
		* c: 实现跨平台需要依赖Java的虚拟机 JVM （Java Virtual Machine）
		
	

				
## 编译运行
###  06编写HelloWorld程序
	* A: 编写步骤(初学者)
		* a: 创建一个普通文本文件，将其修改为.java文件。
		* b: 完成模板代码：
			public class HelloWorld{
				public static void main(String[] args) {
						System.out.println("Hello World!");
				}
			}
	* B: 实际开发步骤
		* a: 定义类
		* b: 写main方法
		* c: 写输出语句(注意：下面的代码是原代码，是不能运行的)	
			public class HelloWorld {
				public static void main(String[] args) {
					System.out.println("HelloWorld");
				}
			} 
		* d：注意：
			* 不要隐藏文件的扩展名
			* 类名和文件名要保持一致
	* C: Java代码的编写执行过程
		* a: 源文件：编写Java源文件（我们也称之为源代码文件），它的扩展名为.java；
		* b: 编译：然后通过编译器把源文件编译成字节码文件，字节码文件扩展名为.class；
		* c: 运行：最后使用解释器来运行字节码文件。

###  07编译Java程序
	* A：程序编译
		* 作用：将程序员写的java源代码生成可以运行的Java程序(.class文件)
		* 过程：
			* a:开启DOS窗口并切换到.java文件所在的目录 比如HelloWord.java存放于d:\234\day01\code 中
			* b:切换到HelloWorld.java所在目录,但是此目录中没有javac命令,所以在编译时要写出javac命令的全路径
			* c: d:\234\day01\code>d:\develop\java\jdk1.7.0_72\bin\javac HelloWorld.java 回车
			* d:在d:\234\day01\code文件夹中多了个HelloWorld.class文件(又叫做字节码文件)

###  08运行Java程序			
	* A：运行程序
		* a: 开启DOS窗口并切换到.class文件所在的目录
		* b: 此目录中没有java命令,所以在运行时也要写出java命令的全路径
		* c: d:\234\day01\code>d:\develop\java\jdk1.7.0_72\bin\java HelloWorld 回车(注意:运行时不用后缀名.class)
		* d: 控制台打印显示结果"HelloWorld"

###  09环境变量的配置
	* A: Path环境变量配置方式一
		* a: 安装高级文本编辑器notepad++
		* b: 配置Windows的path环境变量
			* 环境变量的作用：让Java的bin目录下的javac命令可以在任意目录下执行
			* 配置方法：
				* 右键点击计算机  →  选择属性  →  更改设置  →  点击高级  →  点击环境变量  →  找到系统变量中的path  →  将java安装目录下javac所在的bin目录路径配置到path变量中，用；(英文)与其他变量分隔
			* 注意：
				* 配置path后文件的访问顺序：先访问当前路径，如果当前路径没有该文件，则再访问path配置的路径
	* B:配置过程(建议使用这种方式配置)
		* a：右键点击计算机  →  选择属性  →  更改设置  →  点击高级  →  点击环境变量  →  创建名为JAVA_HOME的环境变量  →  将jdk所在的目录路径(bin所在的路径)配置到JAVA_HOME变量中
		* b: 用;与其他变量分隔  →  在path环境变量中添加%JAVA_HOME%\bin
		
###  10notepad软件安装
	* A: 安装
		* 双击.exe文件安装 即可
		

###  11注释
	* A: 注释
		* a: 定义：用来解释和说明程序的文字，注释是不会被执行的
		* b: 分类：
			* 1：单行注释    //注释内容
			* 2：多行注释    /*注释内容*/
			* 3：文档注释	/**注释内容*/
		* c: 注意：
			* 1：对于单行和多行注释，被注释的文字，不会被JVM解释执行
			* 2：对于文档注释，可以被JDK提供的工具 javadoc 所解析，生成一套以网页文件形式体现的该程序的说明文档
			* 3：单行注释可以嵌套使用，多行注释不能嵌套使用
		* d: 案例代码
			/*
				 实现了一个Java的HelloWorld程序
				 实现步骤：
				   1. 定义类
				   2. 定义主方法
				   3. 一条命令，控制台输出了HelloWorld
			*/
			public class HelloWorld{
				//main主方法，固定格式，程序的入口点
				public static void main(String[] args){
					//系统 输出 打印    打印的内容
					System.out.println("HelloWorld");
				}
			}
			
## 基础语法
###  12关键字
	* A: 关键字
		* a: 定义
			* 是被Java语言赋予特殊含义，具有专门用途的单词，比如之前接触的class，int，double均为Java已经预设好的
		* b: 特点
			* 组成关键字的字母全部小写(代码中的蓝色部分) ,注意String不是关键字
		* c: 常见关键字
			* public static void class等
		* d: 注意事项
			* goto与const是Java中的保留字，即没有赋予特殊含义却仍被Java占用的单词,类似Editplus这样的高级记事本,针对关键字有特殊的颜色标记，非常直观 
	
###  13标识符
	* A: 标识符
		* a: 定义
			* 就是给类,接口,方法,变量等起名字时使用的字符序列
		* b: 组成规则(只能包含下面的内容,不能有其它内容)
			* 1: 英文大小写字母
			* 2：数字字符
			* 3：$和_
		* c: 注意事项
			* 1：数字不能开头
			* 2：不可以使用关键字
			* 3：严格区分大小写，不限制长度
			* 4：起名时，尽量达到见名知意
	* B：标识符中常见的命名规则(这些规定是不受语法约束的)
		* a: 包名：多单词组成时所有字母均小写，使用.连接  aaa.bbb.ccc
		* b: 类名&接口名：大驼峰式   AaaBbbCcc
		* c: 变量名&方法名：小驼峰式   aaaBbbCcc
	* d: 常量名：多单词组成是所有字母均大写，使用_连接AAA_BBB_CCC
	* C: 案例代码
		/*
		   标识符
		   Java中，自己定义的内容
		   自定义类的名字，上一个案例 HelloWorld
		   标识符的规则：
			 组成： 字母52个A-Z a-z 数字0-9 _ 下划线 $ 美元符

			 注意： 不能数字开头，不能是关键字
			 
			 定义名字：
				_abc  0a  a0  a#a  a$a   void
				 YES  NO  YES NO   YES   NO
				 
			 类的名字： 首字母大写，第二个单词首字母大写
			  BeiJingShiHaiDianQuYiYuan
			  MeiGuoJiaLiFuNiYa
			 
			 方法的名字：首字母小写，每个单词首字母大写
			   addStudent  
		*/
		public class Demo{
			
		}

## 数据类型
###  14Java中的数据类型
	* A:为什么有数据类型
		* Java语言是强类型语言，对于每一种数据都定义了明确的具体数据类型
	* B:Java中数据类型的分类
		* 基本数据类型: 基本数据类型是Java语言中内置的类型，分别是整数类型、小数类型、字符类型、布尔类型。
			这四类基本类型是最简单、最基础的类型。
			* 整数(byte、short、int、long)、小数(float、double)、字符类型(char)、布尔类型(boolean)
		* 引用数据类型: 是强大的数据类型，它是基于基本数据类型创建的。JavaSE中提供了一个超级类库，类库中包含了近万种引用数据类型。
			不过现在我们先要学习的是基本类型！
			* 数组、类、接口
			 
###  15Java中的常量
	* A: 常量的定义
		* 常量就是不变的数据量, 在程序执行的过程中其值不可以发生改变
	* B: 常量分类
		* a: 整数类型
			* 十进制表示方式：正常数字   如 13、25等
			* 二进制表示方式：以0b(0B)开头    如0b1011 、0B1001 
			* 十六进制表示方式：以0x(0X)开头   数字以0-9及A-F组成  如0x23A2、0xa、0x10 
			* 八进制表示方式：以0开头   如01、07、0721
		* b: 小数类型
			* 如1.0、-3.15、3.168等
		* c: 布尔类型
			* true、false
		* d: 字符类型
			* 如'a'，'A', '0', '家'
			* 字符必须使用’’ 包裹，并且其中只能且仅能包含一个字符。
		* e: 字符串类型
			* 字符串String类型是一种引用类型，我们先了解作为常量类型的使用方式
			* 如“我爱Java”，“0123”，“”，“null”
			* 字符串必须使用“”包裹，其中可以包含0~N个字符。

###  16程序中输出Java中的常量
	* A: 案例代码
		/*
		   Demo_1类，演示Java中的所有类型的常量
		   程序当中输出：
			 输出整数常量
			 小数常量
			 布尔常量
			 字符常量
			 字符串常量
		*/
		public class Demo_1{
			public static void main(String[] args){
				//输出整数 十进制
				System.out.println(50);
				
				//输出整数，二进制, 数字开头0B
				System.out.println(0B11);
				
				//输出整数，八进制，数字开头0
				System.out.println(051);
				
				//输出整数，十六进制，数组开头0X  0-9 A-F
				System.out.println(0XE);
				
				//输出浮点数据
				System.out.println(5.0);
				
				//输出布尔数据，只有2个值，true，false 关键字
				System.out.println(true);
				System.out.println(false);
				
				//输出字符常量，单引号包裹，只能写1个字符
				System.out.println('a');
				
				//输出字符串常量，双引号包裹，可以写0-n个字符
				System.out.println("HelloWorld");
			}
		}


### 01变量概述
	* A: 什么是变量?
		* a: 变量是一个内存中的小盒子（小容器），容器是什么？生活中也有很多容器，例如水杯是容器，用来装载水；你家里的大衣柜是容器，用来装载衣裤；饭盒是容器，用来装载饭菜。那么变量是装载什么的呢？答案是数据！结论：变量是内存中装载数据的小盒子，你只能用它来存数据和取数据。
	
### 02计算机存储单元
	* A: 计算机中储存和运算的最小单位是?
		* a: 一个字节,也就是一个byte.
			* win+r--cmd--回车			
		* b: 常用储存单位
			*1B（字节） = 8bit
			*1KB = 1024B
			*1MB = 1024KB
			*1GB = 1024MB
			*1TB = 1024GB
			*1PB = 1024TB

			
			
### 03Java中数据类型四类八种
	* A: 数据类型四类八种
		*四类	八种	字节数	数据表示范围
		*整型	byte	1	-128～127
			short	2	-32768～32767
			int	4	-2147483648～2147483648
			long	8	-263～263-1
		*浮点型	float	4	-3.403E38～3.403E38
			double	8	-1.798E308～1.798E308
		*字符型	char	2	表示一个字符，如('a'，'A'，'0'，'家')
		*布尔型	boolean	1	只有两个值true与false


### 04常量和数据类型
	* A:常量的定义
		* a: 整形常量默认是int类型
		* b: 小数常量默认是double类型
		* c: 定义长整形数据如果值超过int取值范围后面要+"L"
		* d: 定义float类型的数据后面要+"f" 否则默认是double
	

### 05变量创建的三要素
	* A: 定义变量的语法格式：
		数据类型  变量名  =  变量值;
		* int         a    =  100;		
        * B:代码:
		public class Variable {
			public static void main(String[] args) {
				int a = 10;
				double b = 3.14;
				char c = 'z';
				String s = "i love java";
			
				a = 20;
				System.out.println(a);
			}
		}
	


				

### 06定义所有的基本数据类型变量
	* A: 案例演示
		* a: 八种基本类型数据的创建

### 07定义字符串变量
	* A：案例演示
		* 创建字符串数据类型变量
		* String 是引用数据类型
### 08变量定义使用注意事项			
	* A：变量使用的注意事项
		* a: 变量定义后可以不赋值，使用时再赋值。不赋值不能使用。
			public static void main(String[] args) {
			int x;
			x = 20; //为x赋值20
			System.out.println(x);//读取x变量中的值，再打印
			}
			
		* c:	变量使用时有作用域的限制。
			public static void main(String[] args) {
			int x = 20;
			{
			    int y = 20;
			}
			System.out.println(x);//读取x变量中的值，再打印
			System.out.println(y);//读取y变量中的值失败，失败原因，找不到y变量，因为超出了y变量作用范围，所以不能使用y变量
			}

			
	




### 09数据类型转换_自动转换
	* A: 	自动类型转换
		* a:表示范围小的数据类型转换成范围大的数据类型，这种方式称为自动类型转换
			自动类型转换格式：
			范围大的数据类型 变量 = 范围小的数据类型值；
			如：
				    double d = 1000;
				或
				    int i = 100;
				    double d2 = i;

		
### 10数据类型转换_强制转换
	* A: 强制类型转换
		*a: 表示范围大的数据类型转换成范围小的数据类型，这种方式称为强制类型转换
		*b: 强制类型转换格式：
		范围小的数据类型  变量 = (范围小的数据类型) 范围大的数据类型值;
		如：
		int  i = (int)6.718;   //i的值为6
		或
		double  d = 3.14;
		int  i2 = (int)d;     //i2的值为3
		
## 运算符


### 11算数运算符_1
	* A: 常见操作
		运算符	运算规则	范例		结果
		+	正号		+3		3
		+	加		2+3		5
		+	连接字符串	“中”+“国”	“中国”
		-	负号		int a=3;-a	-3
		-	减		3-1		2
		*	乘		2*3		6
		/	除		5/2		2
		%	取模		5/2		1
		++	自增		int a=1;a++/++a	2
		--	自减		int b=3;a--/--a	2
	* B: 注意事项
		*a:加法运算符在连接字符串时要注意，只有直接与字符串相加才会转成字符串。
		*b:除法“/”当两边为整数时，取整数部分，舍余数。当其中一边为浮点型时，按正常规则相除。 
		*c:“%”为整除取余符号，小数取余没有意义。结果符号与被取余符号相同。
		*d:整数做被除数，0不能做除数，否则报错。
		*e:小数做被除数，整除0结果为Infinity，对0取模结果为NaN
	* C:代码演示
	public class OperatorDemo1 {
		public static void main(String[] args) {
		/*
		 * 常量使用算数运算符
		 */
		System.out.println(10+20);
		
		/*
		 * 变量使用算数运算符
		 */
		int x = 10;
		int y = 20;
		//"+"作为加法运算使用
		int z = x + y; 
		//"+"作为连接字符串使用
		System.out.println("x="+x);
		System.out.println("y="+y);
		System.out.println("z="+z);
	}
}
### 12算数运算符_2
	* A:算数运算符++、--的使用
		* a: ++运算符，会在原有值的基础上自增1
		* b: --运算符，会在原有值的基础上自减1。
	* B:++  -- 位置的使用
		* a:++,--运算符后置时，先使用变量a原有值参与运算操作，运算操作完成后，变量a的值自增1或者自减1；
		* b:++，--运算符前置时，先将变量a的值自增1或者自减1，然后使用更新后的新值参与运算操作。
### 13赋值运算符
	* A: 赋值运算符的使用
		运算符	运算规则	范例		结果
		=	赋值		int a=2		2
		+=	加后赋值	int a=2，a+=2	4
		-=	减后赋值	int a=2，a-=2	0
		*=	乘后赋值	int a=2，a*=2	4
		/=	整除后赋值	int a=2，a/=2	1
		%=	取模后赋值	int a=2，a%=2	0

	* B：案例演示
		
		 * 赋值运算符
		 * +=, -=, *=, /=, %= ： 
		 * 上面的运算符作用：将等号左右两边计算，会将结果自动强转成等号左边的数据类型,再赋值给等号左边的
		 * 注意：赋值运算符左边必须是变量
	 
		public class OperatorDemo2 {
			public static void main(String[] args) {
				byte x = 10;
				x += 20;// 相当于 x = (byte)(x+20);
				System.out.println(x);
			}
		}

======================第四节课开始=========
### 14比较运算符
	* A:比较运算符的使用
		运算符	运算规则	范例	结果
		==	相等于		4==3	False
		!=	不等于		4!=3	True
		<	小于		4<3	False
		>	大于		4>3	True
		<=	小于等于	4<=3	False
		>=	大于等于	4>=3	True

			 
### 15逻辑运算符
	* A: 逻辑运算符的使用
		运算符	运算规则	范例		结果
		&	与		false&true	False
		|	或		false|true	True
		^	异或		true^flase	True
		!	非		!true		Flase
		&&	短路与		false&&true	False
		||	短路或		false||true	True

		规律小结:
			短路与&&:参与运算的两边数据，有false，则运算结果为false；
			短路或||:参与运算的两边数据，有true，则运算结果为true；
			逻辑非! : 参与运算的数据，原先是true则变成false，原先是false则变成true。

	

### 16三元运算符
	* A: 格式:
		(条件表达式)？表达式1：表达式2；
		
	* B: 代码案例
		方式一：
		System.out.println( 3>2 ? “正确” : “错误” ); 
		// 三元运算符运算后的结果为true，运算结果为表达式1的值“正确”，然后将结果“正确”，在控制台输出打印
	
		方式二：
		int a = 3;
		int b = 4;
		String result = (a==b) ? “相等” : “不相等”;  
		//三元运算符运算后的结果为false，运算结果为表达式2的值“不相等”，然后将结果赋值给了变量result

		方式三：
		int n = (3>2 && 4>6) ? 100 : 200;
		//三元运算符运算后的结果为false，运算结果为表达式2的值200,然后将结果200赋值给了变量n


		
		
### 17运算符优先级
	优先级	描述		运算符
	1	括号		()、[]
	2	正负号		+、-
	3	自增自减，非	++、--、!
	4	乘除，取余	*、/、%
	5	加减		+、-
	6	移位运算	<<、>>、>>>
	7	大小关系	>、>=、<、<=
	8	相等关系	==、!=
	9	按位与		&
	10	按位异或	^
	11	按位或		|
	12	逻辑与		&&
	13	逻辑或		||
	14	条件运算	?:
	15	赋值运算	=、+=、-=、*=、/=、%=
	16	位赋值运算	&=、|=、<<=、>>=、>>>=

### 18	商场库存清单案例
	A: 案例分析.
		* a:观察清单后，可将清单分解为三个部分（清单顶部、清单中部、清单底部）
		* b:清单顶部为固定的数据，直接打印即可
		* c:清单中部为商品，为变化的数据，需要记录商品信息后，打印
			经过观察，我们确定一项商品应该有如下几个属性：
			品牌型号: 即商品名称，String型
			尺寸：物品大小，double型
			价格：物品单价，double型
			配置：这一项为每种商品的配置信息，String型
			库存数：这一项为每种商品的库存个数，int型

		* d:清单底部包含了统计操作，需经过计算后，打印
			我们发现两个单独的可变化量
			总库存数：所有商品总个数，int型
			库存商品总金额：所有商品金额，double型

	B: 案例代码实现
		//步骤一:  创建Demo01库存清单.java文件，编写main主方法
		public class Demo01库存清单 {
			public static void main(String[] args) {
			}
		}
		//步骤二:  记录每种库存商品信息
		//苹果笔记本电脑
		String macBrand = "MacBookAir";
		double macSize = 13.3;
		double macPrice = 6988.88;
		int macCount = 5;

		//联想Thinkpad笔记本电脑
		String thinkpadBrand = "ThinkpadT450";
		double thinkpadSize = 14.0;
		double thinkpadPrice = 5999.99;
		int thinkpadCount = 10;

		//华硕ASUS笔记本电脑
		String ASUSBrand = "ASUS-FL5800";
		double ASUSSize = 15.6;
		double ASUSPrice = 4999.50;
		int ASUSCount = 18;

		//步骤三: 统计库存总个数、库存总金额
		int totalCount = macCount + thinkpadCount + ASUSCount;
		double totalMoney = (macCount * macPrice) + (thinkpadCount * thinkpadPrice) + (ASUSCount * ASUSPrice);

		//步骤四: 列表顶部
		System.out.println("------------------------------商城库存清单-----------------------------");
		System.out.println("品牌型号	尺寸	价格	库存数");

		步骤四:打印库存清单中部信息
		//列表中部
		System.out.println(macBrand+"	"+macSize+"	"+macPrice+"	"+macCount);
		System.out.println(thinkpadBrand+"	"+thinkpadSize+"	"+thinkpadPrice+"	"+thinkpadCount);
		System.out.println(ASUSBrand+"	"+ASUSSize+"	"+ASUSPrice+"	"ASUSCount);
		打印库存清单底部信息
		//列表底部
		System.out.println("-----------------------------------------------------------------------");
		System.out.println("总库存数："+totalCount); 
		System.out.println("库存商品总金额："+totalMoney);


### 01创建引用类型变量公式
	* A: 创建引用类型变量公式
		* a: 我们要学的Scanner类是属于引用数据类型，我们先了解下引用数据类型。
		* b: 引用数据类型的定义格式
			* 与定义基本数据类型变量不同，引用数据类型的变量定义及赋值有一个相对固定的步骤或格式。
			* 数据类型  变量名  =  new 数据类型();
		* c: 引用数据类型的使用
			* 每种引用数据类型都有其功能，我们可以调用该类型实例的功能。
			* 变量名.方法名();
		
## Scanner  Random类
### 02Scanner类的使用
	* A: Scanner类的使用
		* a: 导包import java.util.Scanner;
		* b：创建键盘录入对象 Scanner sc = new Scanner(System.in);
		* c: 读取键盘录入的一个整数
			* int enterNumber = sc.nextInt();
		* d: 读取键盘录入的字符串
			* String enterString = sc.next();
	* B: 案例代码
		import java.util.Scanner;
		public class Demo05Scanner{
			public static void main(String[] args) 
			{
				Scanner sc = new Scanner(System.in);

				int enterNumber = sc.nextInt();
				System.out.println("用户输入的整数为"+enterNumber);

				String enterString = sc.next();
				System.out.println("用户输入的字符串为"+enterString);
			}
		}
			
			
### 03Random随机数类的使用_1
	* A: Random随机数类的使用_1
		* a: 功能
			* 生成随机数需要使用到引用类型随机数Random类
		* b: 使用方式
			* import导包：所属包java.util. Random
			* 创建实例格式：Random  random = new Random ();
			* 调用方法
				* nextInt(int maxValue)	产生[0,maxValue)范围的随机数,包含0不包含maxValue
				* nextDouble()  产生[0,1)范围的随机数
				如：
					Random  random = new Random ();
					int  myNumber = random.nextInt(100);//结果为0-99的一个数
	* B: 案例代码
		import java.util.Random;
		public class RandomDemo{
			public static void main(String[] args){
			   Random ran = new Random();
			   // Random类中的,产生随机数的功能
			   int i = ran.nextInt(100);
			   System.out.println(i);
			   
			   //问题? 产生随机数,范围 1-100之间
			   // nextInt(100) 0-99 + 1
			}
		}

	

### 04Random随机数类的使用_2
	* A: Random随机数类的使用_2
		* a: 调用方法
			* nextDouble()  产生[0,1)范围的随机数
			如：
				Random  random = new Random ();
				int  myNumber = random.nextDouble();//结果为0.0-1.0之间的数(包括0.0不包括1.0)


## 循环控制语句
### 05if语句格式第一种
	* A: if语句格式第一种
		* a: 书写格式
			if(比较表达式) {
				语句体;
			}
		* b：执行流程：
			* 先计算比较表达式的值，看其返回值是true还是false。
			* 如果是true，就执行语句体；
			* 如果是false，就不执行语句体；
	* B: 案例代码
		public class IfDemo{
			public static void main(String[] args){
				  int i = 5 ;
				  //对变量i进行if判断
				  if(i > 5){
					  System.out.println("if中的条件是true");
					  i++;
				  }
				  
				  System.out.println(i);
			}
		}
					

### 06if语句格式第二种
	* A: if语句格式第二种
		* a: 书写格式
			if(比较表达式) {
				语句体1;
			}else {
				语句体2;
			}
		* b：执行流程：
			* 首先计算比较表达式的值，看其返回值是true还是false。
			* 如果是true，就执行语句体1；
			* 如果是false，就执行语句体2；
	* B: 案例代码
		public class IfElseDemo{
			public static void main(String[] args){
			     int i = 16 ;
				 //判断变量,是奇偶数, 除以2,看余数是0还是1
				 if( i % 2 == 0 ){
					 System.out.println(i+" 是偶数");
				 }else{
					 System.out.println(i+" 是奇数");
				 }
		    }
		}


### 07if语句格式第三种
	* A: if语句格式第三种
		* a: 书写格式
				if(比较表达式1) {
					语句体1;
				}else if(比较表达式2) {
					语句体2;
				}else if(比较表达式3) {
					语句体3;
				}
				...
				else {
					语句体n+1;
				}
		* b：执行流程：
			* 首先计算比较表达式1看其返回值是true还是false，
			* 如果是true，就执行语句体1，if语句结束。
			* 如果是false，接着计算比较表达式2看其返回值是true还是false，
			
			* 如果是true，就执行语句体2，if语句结束。
			* 如果是false，接着计算比较表达式3看其返回值是true还是false，
			
			* 如果都是false，就执行语句体n+1。
	* B: 案例代码
		public class IfElseIfDemo{
			public static void main(String[] args){
				//成绩判断要求 ,成绩>80  成绩>70  成绩>60  不及格
				//定义变量,保存成绩
				int grade = 75;
				//使用if else if 语句对成绩判断
				if( grade > 80 ){
					System.out.println(grade+" 成绩是优");
				}else if ( grade > 70){
					System.out.println(grade+" 成绩是良");
				}else if ( grade > 60){
					System.out.println(grade+" 成绩是中");
				}else{
					System.out.println(grade+" 成绩是差");
				}
			 	
			}
		}

### 08if语句和三元运算符的互换			
	* A: 三元运算符
		* a: 概念
			* 用来完成简单的选择逻辑，即根据条件判断，从两个选择中选择一种执行
		* b: 使用格式
			* (条件表达式)？表达式1：表达式2；
		* c: 运算规则
			* 1: 判断条件表达式，结果为一个布尔值
			* 2: true，运算结果为表达式1
			* 3: false，运算结果为表达式2
	* B: 案例代码
		public class IfElseDemo_1{
			public static void main(String[] args){
				int j = 6;
				int i = 15;
				//使用if语句,判断出最大值
				if(i>j){
				int j = 6;
					System.out.println(i+" 是最大值");
				}else{
					System.out.println(j+" 是最大值");
				}
				
				//使用三元运算实现
				int k = i>j ? i : j;
				System.out.println(k+" 是最大值");
			}
		}
	* C: 使用if语句还是三元表达式
		* 判断条件多,使用if
	 	* 三元,必须有结果的, if 可以没有结果的




### 09while循环
	* A: while循环结构
		* a: 使用格式
			初始化表达式；
			while(条件){
				循环体
			}
		* b: 执行顺序
			  当条件是true,就执行循环体,执行完循环体后
			  程序再次执行while中的条件,如果条件还是true,继续执行循环体
			  直到条件是false的时候,循环就结束
	* B: 案例代码
		public class WhileDemo{
			public static void main(String[] args){
				//输出 1-4之间的整数
				//定义变量,整数类型, 循环的条件
				int i = 1;
				while( i < 5 ){
					System.out.println(i);
					i++;
				}
			}
		}

		
### 10for循环_1
	* A: for循环_1
		* a: 使用格式
			 for(初始化变量 ; 条件 ; 增量){
				 循环体;
			 }
		* b: 各模块解释
			初始化变量: 定义变量,作用是用来控制循环的次数
		    条件: 当条件是true,执行循环体,条件是false,结束循环
		    增量: 变量自增情况 
	* B: 案例代码
		public class ForDemo{
			public static void main(String[] args){
				//for循环,输出0-10
				for(int i = 0 ; i < 11 ; i++){
					System.out.println(i);
				}
			}
		}
		
### 11for循环_2
	* A: for循环的执行流程
		for（① ; ② ; ③）{
			④
		}
		第一步，执行①
		第二步，执行②，如果判断结果为true，执行第三步，如果判断结果为false，执行第五步
		第三步，执行④
		第四步，执行③，然后重复执行第二步
		第五步，退出循环
		

### 12for循环_3
	* A: 案例
		* a: 利用for循环,计算1+4的结果
	* B: 案例代码
		public class ForDemo_1{
			public static void main(String[] args){
				// 定义变量,记录求和后的数据
				int sum = 0;
				// 利用循环,将变量从1变化到4
				for(int i = 1 ; i <= 4 ; i++){
					//对变量进行求和
					sum = sum + i;
				}
				System.out.println(sum);
			}
		}
	
### 13do_while循环
	* A: do_while循环
		* a: 使用格式
			do{
			   循环体;
		    }while(条件);
		* b: 执行顺序
			先执行一次循环体，然后再判断条件，如果条件为true，继续执行循环体，
			如果条件为false，循环结束。
		* c: 特点
			* 无条件先执行一次
	* B: 案例代码
		public class DoWhileDemo{
			public static void main(String[] args){
				int i = 0; 
				do{
					System.out.println(i);
					i++;
				}while( i <  5);
			}
		}


### 14死循环
	* A: 死循环概述
		* 无限循环存在的原因是并不知道循环多少次，而是根据某些条件，来控制循环
	* B: 死循环格式
		* while(true){}
		* for(;;){}
			 


### 15嵌套for循环_1
	* A: 嵌套循环的概述
		* 嵌套循环是指在一个循环语句的循环体中再定义一个循环语句的语法结构。while、do…while、for循环语句都可以进行嵌套，并且它们之间也可以互相嵌套，如最常见的在for循环中嵌套for循环。
	* B: 嵌套循环的格式
		for(初始化表达式; 循环条件; 操作表达式) {
			………
			for(初始化表达式; 循环条件; 操作表达式) {
				执行语句
				………
			}
			………
		}
	* C: 各模块解释
		* 总的循环次数 =  内循环次数 * 外循环的次数
		* 内循环,是外循环的循环体
		   
		* 外循环,控制的是行数
		* 内循环,控制的是每行的个数
	

### 16嵌套for循环_2
	* A: 案例
		* a: 打印正三角形
	* B: 案例代码
		public class ForForDemo{
			public static void main(String[] args){
				for(int i = 0 ; i < 9 ; i++){
					for(int j = 0; j < i+1 ;j++){
						System.out.print("* ");
					}
					System.out.println();
				}
			}
		}


### 17break语句
	* A: break语句
		* a: 作用
			* 跳出所在的循环体
		* b: 书写位置
			* 必须出现在循环或选择结构内
		* c: 举例
			for(int i=0; i<10; i++) {
				if(i>5) {
				break;
			}
				System.out.println(“我爱Java”+i);
			}
			//会从0-5输出6次“我爱Java”
	* B: break详细解释
		* a: 作用
			* 在loop/switch选择或者循环过程中，我们总是满足布尔表达条件才能执行对应的代码，然而在这些逻辑过程中，
				可以使用一些关键字直接跳出正在执行的代码，去执行后边或者指定位置的代码，
				这些关键字一旦出现就可以跳转语句执行顺序。
		* b: 使用方式
			* 无法单独使用，必须将break关键字置于switch或循环语句中
		* c: 运行规律
			* 不需要判断任何条件，只要遇到break变直接跳出执行后续代码。会完全跳出选择或者循环结构
			* 只能跳出最近的代码块，不能跨越多级代码块
	
	* C：循环标号
		* a: 为什么使用循环标号
			* 当在双层循环或者循环内有switch选择语句时，我们发现，使用break或者continue所作用的对象均是内层语句，无法直接跳出外层循环，这时就需要使用标号语句跳转了.
		* b: 使用方式
			* 在外层循环外的某行前边，使用后边跟有冒号”:”的标识符，即定义完毕。
			  使用时当在内层循环使用break或continue时后边紧跟之前定义的标号即可
		* c: 运行规律
			* 当外层循环外定义了标号
			* 内层使用break，终止内外双层循环。
			* 内层使用continue，终止内层循环，继续外层循环。
### 18continue语句
   * A: continue语句
		* a: 作用
			* 提前结束本次循环，继续进行下次循环
		* b: 使用方式
			* 无法单独使用，必须将continue关键字置于循环语句中
		* c：运行规律
			* 不需要判断任何条件，只要遇到continue变直接跳出本轮循环进行下次循环
		* d：案例代码
		
    public class ContinueDemo{
	    public static void main(String[] args){
            for(int i = 0 ; i < 10 ; i++){
                if(i%2==0){
                    continue;
                }
                System.out.println(i);
            }
	    }
   }
			//会把0-9之间所有的奇数打印到控制台上


### 19猜数字小游戏
   * A: 猜数字小游戏		
		* a: 分析
			* 用户给的数可能大于、小于、或等于被猜的数，这样就会出现三种情况，用前面讲的三元运算符可以实现，
				但是得用三元运算符的嵌套，比较麻烦！可以用更简单的方式if条件判断，可以有三个以上的条件
		* b: 需求分析
			* 后台预先生成一个随机数1-100，用户键盘录入猜数字
			* 如果猜对了，打印“恭喜您，答对了”
			* 如果猜错了
			* 猜大了：打印“sorry，您猜大了!”
			* 猜小了：打印“sorry，您猜小了!”
					直到数字猜到为止
					最多只能猜5次，否则提示“sorry，您没有机会了!”
        * B: 案例代码

    /*
			猜数字小游戏
			
			完成猜数字小游戏：
			1、产生随机数
			后台预先生成一个随机数1-100，用户键盘录入猜数字
			2、通过if语句对用户猜的数与随机数进行比较
			如果猜对了，打印“恭喜您，答对了”
			如果猜错了
			猜大了：打印“sorry，您猜大了!”
			猜小了：打印“sorry，您猜小了!”
			3、通过for循环完成用户猜数的循环
			直到数字猜到为止
			最多只能猜5次，否则提示“sorry，您没有机会了!”

		*/
		import java.util.Random;
		import java.util.Scanner;
		//通过*的方式可以一次导入该包下所有的类，但是不建议使用。建议使用哪个导哪个。
		//import java.util.*;
		public class GuessNumber{
			public static void main(String[] args) {
				//1、产生随机数
				//后台预先生成一个随机数1-100，用户键盘录入猜数字
				//创建随机数对象
				Random random = new Random();
				//产生一个1-100的随机数
				int randomNumber = random.nextInt(100)+1;
				//System.out.println("我产生的随机数是："+randomNumber+"你猜猜是多少？");  作弊专用

				//产生控制台录入的Scanner对象
				Scanner sc = new Scanner(System.in);
				//3、通过for循环完成用户猜数的循环
				//通过for循环完成猜数字逻辑
				for(int i=1; i<=5; i++){
					//提示用户输入要猜的数，用变量接收
					System.out.println();
					System.out.println("请您输入一个1-100的数：");
					int guessNumber = sc.nextInt();
					
					//2、通过if语句对用户猜的数与随机数进行比较
					//如果猜对了
					if(guessNumber==randomNumber) {
						//打印猜对后的提示
						System.out.println("恭喜您，猜对了！");
						//跳出循环，不用再猜了
						break;
					}else {//如果猜错了
						//如果猜大了
						if(guessNumber>randomNumber) {
							System.out.println("sorry，您猜大了!");
						}else {//如果猜小了
							System.out.println("sorry，您猜小了!");
						}
					}
					//如果猜到了最后的第5次仍然没有猜对就跳出循环
					if(i==5) {
						System.out.println("对不起，点太背，下次再来吧！");
						break;
					}
					//每次猜错后，都提示还有多少次机会
					System.out.println("请注意，您还有"+(5-i)+"次机会，请慎重作答！");
				}
			}
		}


### 01switch语句解构
​	* A:switch语句解构
    * a:switch只能针对某个表达式的值作出判断，从而决定程序执行哪一段代码。

      	* b:格式如下:
      	      swtich(表达式){
      			  case 常量1 :
      			    要执行的语句;
      			  break;
      			  
      			  case 常量2 :
      			    要执行的语句;
      			  break;
      			  
      			  case 常量3 :
      			    要执行的语句;
      			  break;
      			  
      			  default:
      			    要执行的语句;
      			  break;
      		  }
      	* c: 执行流程:  表达式,和case后面的常量进行比较和哪个case后的常量相同,就执行哪个case后面的程序,遇到break,就全结束
      	  
      	* d: 关键字: switch case default break

        	* e:举例
      		如果等于1，则输出星期一
      	​	如果等于2，则输出星期二
      	​	如果等于3，则输出星期三
      	​	如果等于4，则输出星期四
      	​	如果等于5，则输出星期五
      	​	如果等于6，则输出星期六
      	​	如果等于7，则输出星期天


### 02switch语句的星期判断
   * A:switch语句的星期判断
   * a:明确需求:初始化int类型变量(1-7)代表星期几,使用switch语句进行判断,并打印出该整数对应的星期。​								
   * b:代码实现：
   
    public class SwitchDemo01 {
		public static void main(String[] args) {
			int week = 5;
			switch (week) {
			case 1:
				System.out.println("星期一");
				break;
			case 2:
				System.out.println("星期二");
				break;
			case 3:
					ystem.out.println("星期三");
				break;
			case 4:
				System.out.println("星期四");
				break;
			case 5:
				System.out.println("星期五");
				break;
			case 6:
				System.out.println("星期六");
				break;
			case 7:
				System.out.println("星期天");
				break;
			default:
				System.out.println("输入的数字不正确...");
				break;
					}
				}
			}


​			
### 03switch语句接受的数据类型
    ​* A: switch语句接受的数据类型

    * a:注意事项
        switch语句中的表达式的数据类型,是有要求的
        JDK1.0 - 1.4  数据类型接受 byte short int char
        JDK1.5   数据类型接受 byte short int char enum(枚举)
        JDK1.7   数据类型接受 byte short int char enum(枚举), String	
​	

### 04case穿透
​	* A:case穿透

    ​	* a: 在使用switch语句的过程中，如果多个case条件后面的执行语句是一样的，则该执行语句只需书写一次即可，这是一种简写的方式。
    ​	* b: 例如，要判断一周中的某一天是否为工作日，同样使用数字1~7来表示星期一到星期天，当输入的数字为1、2、3、4、5时就视为工作日，否则就视为休息日。



​				
## 数组
### 05数组的概述
​	* A: 数组的概述
 
        * a:数组的需求
            现在需要统计某公司员工的工资情况，例如计算平均工资、最高工资等。假设该公司有50名员工，用前面所学的知识完成，
            那么程序首先需要声明50个变量来分别记住每位员工的工资，这样做会显得很麻烦.

	 	
	    * b:数组的概述
            数组是指一组数据的集合，数组中的每个数据被称作元素。在数组中可以存放任意类型的元素，但同一个数组里存放的元素类型必须一致。

### 06数组的定义
​	* A：数组的定义
​	* b:格式:
​		数据类型[] 数组名 = new 数据类型[元素个数或数组长度];

	* c:举例:
			int[] x = new int[100];
	* c:要点说明
	  	1)数据类型: 数组中存储元素的数据类型
		2) [] 表示数组的意思
		3) 变量名  自定义标识符  
		4) new  创建容器关键字
		5)数据类型: 数组中存储元素的数据类型
		6)[]  表示数组的意思
		7)元素个数,就是数组中,可以存储多少个数据 (恒定, 定长)
		  
		数组是一个容器: 存储到数组中的每个元素,都有自己的自动编号
		自动编号,最小值是0, 最大值,长度-1
		自动编号专业名次, 索引(index), 下标, 角标
		访问数组存储的元素,必须依赖于索引, 公式 数组名[索引]
		
		Java提供一个属性,操作索引的
		数组的一个属性,就是数组的长度, 属性的名字 length
		使用属性:  数组名.length  数据类型 int
		
		数组的最小索引是0, 最大索引数组.length-1





### 07JVM内存划分			
​	* A：内存划分
​	* JVM对自己的内存划分为5个区域
​	  	* a: 寄存器:内存和CUP之间
​	  	* b: 本地方法栈: JVM调用了系统中的功能
​	  	* c: 方法和数据共享: 运行时期class文件进入的地方
​	  	* d: 方法栈:所有的方法运行的时候进入内存
​	  	* e: 堆:存储的是容器和对象
​		


### 08数组的内存
​	* A: 数组的内存
​	* int[] x;	            	// 声明一个int[]类型的变量
​	*	x = new int[100];		// 创建一个长度为100的数组
​	*	接下来，通过两张内存图来详细地说明数组在创建过程中内存的分配情况。
​	*	第一行代码 int[] x; 声明了一个变量x，该变量的类型为int[]，即一个int类型的数组。变量x会占用一块内存单元，它没有被分配初始值
​	*	第二行代码 x = new int[100]; 创建了一个数组，将数组的地址赋值给变量x。在程序运行期间可以使用变量x来引用数组，这时内存中的状态会发生变化


​		
### 09使用索引访问数组的元素
​	* A: 使用索引访问数组的元素
​		* 组中有100个元素，初始值都为0。数组中的每个元素都有一个索引(也可称为角标)，要想访问数组中的元素可以通过“x[0]、x[1]、……、x[98]、x[99]”的形式。
​		* 需要注意的是，数组中最小的索引是0，最大的索引是“数组的长度-1”
​		

### 10数组的length属性
​	* A: lenth属性
​		* a 在Java中，为了方便我们获得数组的长度，提供了一个length属性，在程序中可以通过“数组名.length”的方式来获得数组的长度，即元素的个数。
​		* b 求数组的长度
​			public class ArrayDemo01 {
​		 		public static void main(String[] args) {
​		 			int[] arr; // 声明变量
​		 			arr = new int[3]; // 创建数组对象
​		 			System.out.println("arr[0]=" + arr[0]); // 访问数组中的第一个元素
​		 			System.out.println("arr[1]=" + arr[1]); // 访问数组中的第二个元素
​		 			System.out.println("arr[2]=" + arr[2]); // 访问数组中的第三个元素
​		 			System.out.println("数组的长度是：" + arr.length); // 打印数组长度
​		 		}
 			}

### 11为数组的元素赋值
​	* A: 为数组的元素赋值
​		* a: 如果在使用数组时，不想使用这些默认初始值，也可以显式地为这些元素赋值。
​		* 	赋值过的元素已经变为新的数值,没有赋值的元素默认初始化的数值
​		* b: 案例
​		 	public class ArrayDemo02 {
​		 		public static void main(String[] args) {
​		 			int[] arr = new int[4]; // 定义可以存储4个整数的数组
​		 			arr[0] = 1; // 为第1个元素赋值1
​		 			arr[1] = 2; // 为第2个元素赋值2
​		 			// 下面的代码是打印数组中每个元素的值
​		 			System.out.println("arr[0]=" + arr[0]);
​		 			System.out.println("arr[1]=" + arr[1]);
​		 			System.out.println("arr[2]=" + arr[2]);
​					System.out.println("arr[3]=" + arr[3]);
​		 		}
 			}




### 12数组的定义_2
​	* A: 定义数组格式2
​		* a: 数组初始化
​			动态初始化 : 在定义数组时只指定数组的长度，由系统自动为元素赋初值的方式称作动态初始化。
​			1、类型[] 数组名 = new 类型[长度];
​			int[] arr = new int[4];
​			静态初始化: 在初始化数组时还有一种方式叫做静态初始化，就是在定义数组的同时就为数组的每个元素赋值。
​			2、类型[] 数组名 = new 类型[]{元素，元素，……};
​			int[] arr = new int[]{1,2,3,4};
​			3、类型[] 数组名 = {元素，元素，元素，……};	 
​			int[] arr = { 1, 2, 3, 4 };
​	
​		


### 13遍历数组
​	* A:遍历数组
​		* 在操作数组时，经常需要依次访问数组中的每个元素，这种操作称作数组的遍历
​	* B:练习
​		public class ArrayDemo04 {
​			public static void main(String[] args) {
​				int[] arr = { 1, 2, 3, 4, 5 }; // 定义数组
​				// 使用for循环遍历数组的元素
​				for (int i = 0; i < arr.length; i++) {
​					System.out.println(arr[i]); // 通过索引访问元素
​				}
​			}
​		}
​		上述代码中，定义一个长度为5的数组arr，数组的角标为0~4。由于for循环中定义的变量i的值在循环过程中为0~4，因此可以作为索引，依次去访问数组中的元素，并将元素的值打印出来


### 14数组中常见的异常
​	* A: 数组操作中,常见的两个异常
​    	 数组的索引越界异常
​	 	 空指针异常

	* B: 练习
		public class ArrayDemo_4{
			public static void main(String[] args){
				//数组的索引越界异常
				//int[] arr = {5,2,1};
				//数组中3个元素,索引 0,1,2
				//System.out.println(arr[3]);//java.lang.ArrayIndexOutOfBoundsException: 3
				
				//空指针异常
				int[] arr2 = {1,5,8};
				System.out.println(arr2[2]);
				arr2 = null; // arr2 不在保存数组的地址了
				System.out.println(arr2[2]);//java.lang.NullPointerException
			}
		}

### 15数组最值
​	* A: 数组获取最值的原理思想
​		* 定义数组的第一个元素arr[0]为最大值;循环arr数组,判断如果有比arr[0] 大的就交换,直到arr数组遍历完毕,那么arr[0]中就保存了最大的元素

​		


### 16数组获取最值代码实现
​	* A: 代码实现
​		public class ArrayDemo05 {
​			public static void main(String[] args) {
​				int[] arr = { 4, 1, 6, 3, 9, 8 }; 	// 定义一个数组
​				int max = arr[0]; 					// 定义变量max用于记住最大数，首先假设第一个元素为最大值
​				// 下面通过一个for循环遍历数组中的元素
​				for (int x = 1; x < arr.length; x++) {
​					if (arr[x] > max) { 			// 比较 arr[x]的值是否大于max
​						max = arr[x]; 				// 条件成立，将arr[x]的值赋给max
​					}
​				}
​				System.out.println("max=" + max); 	// 打印最大值
​			}
​		}


### 17二维数组的定义
​	* A 二维数组的作用
​		* 要统计一个学校各个班级学生的考试成绩，又该如何实现呢？
​		* 这时就需要用到多维数组，多维数组可以简单地理解为在数组中嵌套数组。
​	* B 定义格式
​		* a 第一种定义格式:
​			*  int[][] arr = new int[3][4];
​			*  上面的代码相当于定义了一个3*4的二维数组，即二维数组的长度为3，二维数组中的每个元素又是一个长度为4的数组
​		* b 第二种定义格式
​			*  int[][] arr = new int[3][];
​			*  第二种方式和第一种类似，只是数组中每个元素的长度不确定
​		* c 第三种定义格式
​			*  	int[][] arr = {{1,2},{3,4,5,6},{7,8,9}};
​			*  	二维数组中定义了三个元素，这三个元素都是数组，分别为{1,2}、{3,4,5,6}、{7,8,9}





### 18二维数组元素的访问
​	 * A: 二维数组的访问
​	 * 案例:
​	  class ArrayDemo08 {
​		public static void main(String[] args){
​		
			//定义二维数组的方式
			int[][] arr = new int[3][4];
			System.out.println( arr );
			System.out.println("二维数组的长度: " + arr.length);
			//获取二维数组的3个元素
			System.out.println( arr[0] );
			System.out.println( arr[1] );
			System.out.println( arr[2] );
			
			System.out.println("打印第一个一维数组的元素值");
			System.out.println( arr[0][0] );
			System.out.println( arr[0][1] );//访问的为二维数组中第1个一维数组的第2个元素
			System.out.println( arr[0][2] );
			System.out.println( arr[0][3] );
			
			System.out.println("打印第二个一维数组的元素值");
			System.out.println( arr[1][0] );
			System.out.println( arr[1][1] );
			System.out.println( arr[1][2] );
			System.out.println( arr[1][3] );
			
			System.out.println("打印第三个一维数组的元素值");
			System.out.println( arr[2][0] );
			System.out.println( arr[2][1] );
			System.out.println( arr[2][2] );
			System.out.println( arr[2][3] );
		}
	}


### 19二维数组内存图
​	 * A: 二维数组内存图
​	 * 举例:int[][] arr = new int[3][2];
​	 * 外层数组长在内存开辟连续的3个大的内存空间,每一个内存空间都对应的有地址值
​	 * 每一个大内存空间里又开辟连续的两个小的内存空间.



### 20二维数组的定义和访问
​	 * A: 二维数组的定义和访问
​		 * 格式1: 
​		 * 	int[][] arr = new int[3][]; 不推荐
​		 * 格式2
​		 *  int[][] arr = {{1,2,4},{4,7},{0,9,3}};
​		 *  
​	 * B: 二维数组的访问
​	 	 举例:int[][] arr = {{1,2,4},{5,8,7},{0,9,3}};  
​		  想要打印数组中7这个元素需要先找到大的元素索引{5,7} 索引为2 ,在找7在{5,7}中的索引2
​		  那么结果为 arr[2][2]  第一个[2]代表大数组中{5,8,7}这个元素索引
​		  第二个[2]代表{5,8,7}中7元素的索引
​		
### 22二维数组的遍历
​	  * A:二维数组遍历
​		 int[][] arr = {{1,2,4},{4,7},{0,9,3}};
  		 先使用for循环遍历arr这个二维数组,得到每一个元素为arr[i]为一维数组
​		 再外层for循环中嵌套一个for循环遍历每一个一维数组arr[i],得到每一元素

	  *	B:举例:遍历二维数组
		public class ArrayArrayDemo_2{
			public static void main(String[] args){
				int[][] arr = { {1,2,3},{4,5},{6,7,8,9},{0} };
				
				//外循环,遍历二维数组
				for(int i = 0 ; i < arr.length ;i++){
					//内循环,遍历每个一维数组 arr[0] arr[1] arr[i]
					for(int j = 0 ; j < arr[i].length; j++){
						System.out.print(arr[i][j]);
					}
					System.out.println();
				}
			}
		
	  * C:二维数组累加求和
	   class ArrayDemo09 {
			public static void main(String[] args){
			  	int[][] arr2 = { {1,2},{3,4,5},{6,7,8,9,10} };
				int sum2 = 0;
				for (int i=0; i<arr2.length; i++) {
					for (int j=0; j<arr2[i].length; j++) {
		                 //System.out.println(arr2[i][j])
						sum2 += arr2[i][j];
					}
				}
				System.out.println("sum2= "+ sum2);
			}
		}

### 23二维数组的求和练习
​	 * A 例如要统计一个公司三个销售小组中每个小组的总销售额以及整个公司的销售额。如下所示
​		* 第一小组销售额为{11, 12}万元
​		* 第二小组销售额为{21, 22, 23}万元
​		* 第三小组销售额为{31, 32, 33, 34}万元。

	  * B 代码实现
	   	public class ArrayDemo10 {
	 		public static void main(String[] args) {
	 			int[][] arr = new int[3][]; 			// 定义一个长度为3的二维数组
				arr[0] = new int[] { 11, 12 }; 			// 为数组的元素赋值
	 			arr[1] = new int[] { 21, 22, 23 };
	 			arr[2] = new int[] { 31, 32, 33, 34 };		
	 			int sum = 0; 							// 定义变量记录总销售额
	 			for (int i = 0; i < arr.length; i++) { // 遍历数组元素
	 				int groupSum = 0; // 定义变量记录小组销售总额
	 			for (int j = 0; j < arr[i].length; j++) { // 遍历小组内每个人的销售额
	 					groupSum = groupSum + arr[i][j];
	 			}
	 				sum = sum + groupSum; 			// 累加小组销售额
	 				System.out.println("第" + (i + 1) + "小组销售额为：" + groupSum + " 万元");
	 			}
	 			System.out.println("总销售额为: " + sum + " 万元");
	 		}
	 	}



### 24随机点名器案例分析
​	 * A 随机点名器案例分析
​	  
	 * B: 需求
		 * 随机点名器，即在全班同学中随机的打印出一名同学名字。
	  
	 * C:分析:
		 * 1)定义数组存数全班同学
		 * 2)生成随机数范围0 到 数组长度-1
		 * 3)根据这个索引找到数组中的同学名称




### 25随机点名器代码实现
​	 * A: 分析
​	   	 随机点名器:
​	     1  存储姓名
​		 2. 预览所有人的姓名
​		 3. 随机出一个人的姓名
​	 * B 代码实现
​		import java.util.Random;
​		public class CallName{
​			public static void main(String[] args){
​				//存储姓名,姓名存储到数组中
​				//数组存储姓名,姓名的数据类型,String
​				String[] names = {"张三","李四","王五","李蕾","韩梅梅","小名","老王","小华","约翰逊","爱丽丝"};
​				
				//预览: 遍历数组,打印所有姓名
				for(int i = 0 ; i < names.length ; i++){
					System.out.println(names[i]);
				}
				System.out.println("=============");
				
				//随机出一个人的名
				//利用随机数,生成一个整数,作为索引,到数组中找到对应的元素
				Random ran = new Random();
				//随机数,范围必须是0-数组的最大索引
				int index = ran.nextInt(names.length);//index 就是随机数,作为索引
				System.out.println(names[index]);
			}
		}

### 25随机点名器代码实现_2
​		* A 代码优化:
​		import java.util.Random;
​		public class CallName{
​			public static void main(String[] args){
​				String[] names = {"张三","李四","王五","李蕾","韩梅梅","小名","老王","小华","约翰逊","爱丽丝"};
​				System.out.println(names[new Random().nextInt(names.length)]);
​			}
​		}



## 方法

### 01方法的概述
	* A: 为什么要有方法
		* 提高代码的复用性 
	* B: 什么是方法
		* 完成特定功能的代码块。 
		
	
### 02方法的定义格式
	* A: 方法的格式
	* 
			修饰符 返回值类型 方法名(参数类型 参数名1,参数类型 参数名2...) {
				方法体语句;
				return 返回值; 
			} 
	* B: 方法的格式说明
		* 修饰符：目前就用 public static。后面我们再详细的讲解其他的修饰符。
		* 返回值类型：就是功能结果的数据类型。
		* 方法名：符合命名规则即可。方便我们的调用。
		* 参数：
			* 实际参数：就是实际参与运算的。
			* 形式参数；就是方法定义上的，用于接收实际参数的。
		* 参数类型：就是参数的数据类型
		* 参数名：就是变量名
		* 方法体语句：就是完成功能的代码。
		* return：结束方法的。
		* 返回值：就是功能的结果，由return带给调用者。 
				
			
### 03定义方法计算面积
	* A: 定义方法计算面积
		public class MethodDemo{
	
			public static void main(String[] args){
				 //调用方法, 方法执行起来
				 // 在方法main中,调用方法 getArea
		
				 int area = getArea(5,6);
				 System.out.println("面积是: "+area);
				
			}
			/*
			   要求: 计算一个长方形的面积
			   定义方法解决这个要求
			   分析方法定义过程:
			      1.明确方法计算后的结果的数据类型 int  定义格式对应的就是返回值类型
				  2.方法计算过程中,有没有未知的数据, 宽和长, 未知数据的数据类型 int
				      未知数的变量,定义在方法的小括号内
			*/
			public static int  getArea(int w, int h){
				//实现方法的功能主体
				//int area = w * h;
				return w * h;
			}
		}


### 04调用方法
	* A: 调用方法
		* a: 在main函数中调用方法，让方法执行起来
		* b: 方法的形参
			* 方法要什么参数我们就给什么类型的参数。
		* c: 方法的返回值
			* 方法返回什么类型的值我们就用对应的数据类型的变量来接收


### 05调用方法执行流程
	* A: 调用方法执行流程
		* a: 方法的定义是没有顺序的，写在main函数的上边或者下边都可以。
		* b: 方法的执行，是把实参传递给形参，从而来执行的。
		* c: 方法只有被调用才会执行。

### 06方法调用的内存图
	* A: 方法调用的内存图
		* a: 参见\day05\day05(Java基础语法)\day05_source\方法内存图.JPG



### 07方法调用的练习
	* A: 案例代码
		/*
		   方法的定义练习
		*/
		import java.util.Scanner;
		public class MethodDemo_1{
			public static void main(String[] args){
				//printRect();
				//int number = getNumber();
				//System.out.println(getNumber());
				//printRect2(3,5);
				double avg = getAvg(2,2,3);
				System.out.println(avg);
			}
		
			/*
			   定义有返回值有参数方法，如求三个数的平均值
			   明确方法计算后的数据类型, 返回值类型 double
			   明确方法未知数, 三个未知的整数
			*/
			public static double getAvg(double a, double b,double c){
				 return (a+b+c)/3;
			}
			
			/*
			    定义无返回值有参数方法，如打印指定M行，每行N个*号的矩形
				明确方法计算后结果,控制台输出图形,没有返回值的
				方法中有没有未知数,图形行数,和列数,是未知的, 数据类型整数int
			*/
			public static void printRect2(int m,int n){
				for(int i = 0 ; i < m ; i++){
					for(int j = 0 ; j < n ;  j++){
						System.out.print("*");
					}
					System.out.println();
				}
			}
		
			/*
			   定义有返回值无参数方法，如键盘录入得到一个整数
			   明确方法计算后结果的数据类型 int
			   明确有没有未知数,没
			*/
			public static int getNumber(){
				Scanner sc = new Scanner(System.in);
				//int number = sc.nextInt();
				return sc.nextInt();
			}
			
			/*
			   定义无返回值无参数方法，如打印3行，每行3个*号的矩形
			   为什么没有返回值:
			       打印矩形 ,输出效果,不需要将结果返回
				   明确未知数: 不需要未知数
			*/
			public static void printRect(){
				for(int i = 0 ; i < 3 ; i++){
					for(int j = 0 ; j < 3 ;j++){
						System.out.print("*");
					}
					System.out.println();
				}
			}
		}


### 08方法的定义和使用的注意事项
	* A: 方法的定义和使用的注意事项
		* a: 方法不能定义在另一个方法的里面
	 	* b: 写错方法名字
		* c: 写错了参数列表
		* d: 方法返回值是void,方法中可以省略return 不写
		     return 下面不能有代码
		* e 方法返回值类型,和return 后面数据类型必须匹配
		* f: 方法重复定义问题
		* g: 调用方法的时候,返回值是void, 不能写在输出语句中


### 09方法的重载
	* A: 方法的重载
		* 在同一个类中，方法名相同，参数列表不同。与返回值类型无关。
	
		* 参数列表不同：
			* A:参数个数不同
			* B:参数类型不同
			* C:参数的顺序不同(算重载,但是在开发中不用)

	* B: 案例代码
		public static int getSum(int a,int b){
			System.out.println("两个int参数");
			return a+b;
		}
		public static int getSum(int a,int b,int c){
			System.out.println("三个int参数");
			return a+b+c;
		}
		public static double getSum(double a,double b){
			System.out.println("两个double参数");
			return a+b;
		}

		
### 10方法重载注意事项
	* A: 方法重载注意事项
		* a: 参数列表必须不同
		* b: 重载和参数变量名无关
		* c: 重载和返回值类型无关
		* d: 重载和修饰符无关
	    * e: 技巧: 重载看方法名和参数列表
	    
		
### 11方法参数是基本数据类型
	* A: 方法参数是基本数据类型
		* a: 方法参数是基本类型时，传递的是值。


### 12方法参数是引用数据类型
	* A: 方法参数是引用数据类型
		* a: 方法参数是引用类型时，传递的是内存地址值。
		


	
### 13随机点名器
	* A: 案例代码
		/*
		   实现随机点名器
		     1.存储所有学生姓名
			 2.预览所有学生姓名,遍历数组
			 3.随机数作为索引,到数组中找元素
			 
			将功能独立出来, 作成方法,调用方法即可
			
			定义三个功能, 用到同一个姓名数据
			姓名存储到数组中,三个方法,使用一个数组中的数据, 方法传递参数
		*/
		import java.util.Random;
		public class CallName{
			public static void main(String[] args){
				//定义数组,存储学生姓名
				String[] names = new String[8];
				//调用添加姓名方法
				addStudent(names);
				//调用遍历数组方法
				printStudentName(names);
				//调用随机姓名的方法
				String name = randomStudentName(names);
				System.out.println(name);
			}
			/*
			  定义方法,随机数,做索引,数组中找到学生姓名
			  返回值?  学生姓名
			  参数?  数组
			*/
			public static String randomStudentName(String[] names){
				Random ran = new Random();
				int index = ran.nextInt(names.length);
				return names[index];
			}
			
			/*
			   定义方法,遍历数组
			   返回值? 没有
			   参数? 数组
			*/
			public static void printStudentName(String[] names){
				for(int i = 0 ; i < names.length ;i++){
					System.out.println(names[i]);
				}
			}
			
			/*
			   定义方法,实现向数组中添加学生姓名
			   返回值? 没有,
			   参数?  参数就是数组
			*/
			public static void addStudent(String[] names){
				names[0] = "张三";
				names[1] = "李四";
				names[2] = "王五";
				names[3] = "李蕾";
				names[4] = "韩梅梅";
				names[5] = "小名";
				names[6] = "老王";
				names[7] = "小华";
			}
		}


### 14库存案例代码实现_1
	* A: 案例代码
		/*
		   实现商品的库存管理
		     功能:
			    1.展示用户选择功能清单
				2.根据选择的功能编号,进行不同的操作
				   A. 展示所有库存
				   B. 修改库存数量
				   
			  分析:
			    1.展示用户清单:
				   输出语句, 用户输入, 选择功能序号
				2.根据选择,调用不同的方法
				    switch语句
					  case 1 2 3
				
				   A  展示库存
				     将存储商品的数组,遍历
				   B  修改库存
				        
					  修改所有的库存数量
		*/
		import java.util.Scanner;
		public class Shopp{
			public static void main(String[] args){
				
			}
			
			/*
			   定义方法,展示所有的库存清单,遍历
			   返回值,没有
			   参数, 数组
			*/
			public static void printStore(String[] brand,double[] size,double[] price,int[] count){
				System.out.println("----------商场库存清单----------");
				System.out.println("品牌型号     尺寸    价格    库存数");
				//定义变量,计算总库存数,和总价格
				int totalCount = 0;
				int totalMoney = 0;
				//遍历数组,将数组中所有的商品信息打印出来
				for(int i = 0 ; i < brand.length ; i++){
					System.out.println(brand[i]+"   "+size[i]+"    "+price[i]+"   "+count[i]);
					totalCount += count[i];
					totalMoney += count[i]*price[i];
				}
				System.out.println("总库存数: "+totalCount);
				System.out.println("商品库存总金额: "+totalMoney);
			}
			
			/*
			  定义方法,实现用户的选择功能,功能的需要返回来
			  返回值, int
			  参数, 没有
			*/
			public static int chooseFunction(){
				System.out.println("-------------库存管理------------");
				System.out.println("1.查看库存清单");
				System.out.println("2.修改商品库存数量");
				System.out.println("3.退出");
				System.out.println("请输入要执行的操作序号：");
				//接受键盘输入
				Scanner sc = new Scanner(System.in);
				int chooseNumber = sc.nextInt();
				return chooseNumber;
			}
		}
			 


### 15库存案例代码实现_2
	* A: 案例代码
		/*
		  定义方法,修改所有商品的库存
		    用户输入1个,修改1个
			返回值,没有
			参数, 库存数的数组, 品名数组
		*/
		public static void update(String[] brand, int[] count){
			//遍历数组,遍历到一个,修改一个
			//接受键盘输入
			Scanner sc = new Scanner(System.in);
			//遍历数组
			for(int i = 0; i < brand.length ; i++){
				System.out.println("请输入"+brand[i]+"的库存数");
				//键盘输入,录入库存, 存储到库存的数组中
				int newCount = sc.nextInt();
				count[i] = newCount;
			}
			//int chooseNumber = sc.nextInt();
		}

### 16库存案例代码测试
	* A: 案例
		/*
		   实现商品的库存管理
		     功能:
			    1.展示用户选择功能清单
				2.根据选择的功能编号,进行不同的操作
				   A. 展示所有库存
				   B. 修改库存数量
				   
			  分析:
			    1.展示用户清单:
				   输出语句, 用户输入, 选择功能序号
				2.根据选择,调用不同的方法
				    switch语句
					  case 1 2 3
				
				   A  展示库存
				     将存储商品的数组,遍历
				   B  修改库存
				        
					  修改所有的库存数量
		*/
		import java.util.Scanner;
		public class Shopp{
			public static void main(String[] args){
				//使用数组,保存商品的信息
				//品名,尺寸,价格,库存数, 定义5个数组
				String[] brand = {"MacBookAir","ThinkpadT450"};
				double[] size = {13.3,15.6};
				double[] price = {9998.97,6789.56};
				int[] count = {0,0};
				while(true){
					int choose = chooseFunction();
					switch(choose){
						case 1:
						  //调用查看库存清单方法
						  printStore(brand,size,price,count);
						break;
						
						case 2:
						  //调用修改库存的方法
						  update(brand,count);
						break;
						
						case 3:
						 return ;
						default:
						  System.out.println("没有这个功能");
						break;
					}
				}
			}
			/*
			  定义方法,修改所有商品的库存
			    用户输入1个,修改1个
				返回值,没有
				参数, 库存数的数组, 品名数组
			*/
			public static void update(String[] brand, int[] count){
				//遍历数组,遍历到一个,修改一个
				//接受键盘输入
				Scanner sc = new Scanner(System.in);
				//遍历数组
				for(int i = 0; i < brand.length ; i++){
					System.out.println("请输入"+brand[i]+"的库存数");
					//键盘输入,录入库存, 存储到库存的数组中
					int newCount = sc.nextInt();
					count[i] = newCount;
				}
				//int chooseNumber = sc.nextInt();
			}
			
			/*
			   定义方法,展示所有的库存清单,遍历
			   返回值,没有
			   参数, 数组
			*/
			public static void printStore(String[] brand,double[] size,double[] price,int[] count){
				System.out.println("----------商场库存清单----------");
				System.out.println("品牌型号     尺寸    价格    库存数");
				//定义变量,计算总库存数,和总价格
				int totalCount = 0;
				int totalMoney = 0;
				//遍历数组,将数组中所有的商品信息打印出来
				for(int i = 0 ; i < brand.length ; i++){
					System.out.println(brand[i]+"   "+size[i]+"    "+price[i]+"   "+count[i]);
					totalCount += count[i];
					totalMoney += count[i]*price[i];
				}
				System.out.println("总库存数: "+totalCount);
				System.out.println("商品库存总金额: "+totalMoney);
			}
			
			/*
			  定义方法,实现用户的选择功能,功能的需要返回来
			  返回值, int
			  参数, 没有
			*/
			public static int chooseFunction(){
				System.out.println("-------------库存管理------------");
				System.out.println("1.查看库存清单");
				System.out.println("2.修改商品库存数量");
				System.out.println("3.退出");
				System.out.println("请输入要执行的操作序号：");
				//接受键盘输入
				Scanner sc = new Scanner(System.in);
				int chooseNumber = sc.nextInt();
				return chooseNumber;
			}
		}

## 类
### 01引用数据类型_类
	* A: 数据类型
		* a: java中的数据类型分为：基本类型和引用类型
	* B: 引用类型的分类
		* a: Java为我们提供好的类，比如说：Scanner,Random等。
		* b: 我们自己创建的类，按照类的定义标准，可以在类中包含多个方法与属性，来供我们使用。 
		
	
### 02自定义类的概述
	* A: 自定义类的概述
		* java代码映射成现实事物的过程就是定义类的过程。
		* 举例：
			我们就拿一部手机进行分析，它能用来做什么呢？它可以打电话，上网，聊微信等，这些就是手机所提供的功能，也就是方法；手机也有它的特征，如颜色、尺寸大小、品牌型号等，这些就是手机的特征，也就是属性
		* 目前，我们只关注类中的属性，类中的方法在面向对象部分再进行学习。
				
			
### 03自定义类的格式
	* A: 自定义类的格式
		* a: 使用类的形式,对现实中的事物进行描述。
		* b: 事物由方法和属性两部分组成。
			* 方法: 这个事物具备的功能。
			* 属性: 这个事物具备的特征。
		* c: 格式
			public class 类名{
				属性定义
				  修饰符 数据类型 变量名 = 值
				
				方法定义
				  修饰符 返回值类型  方法名(参数列表){
					  
				  }
			}


### 04自定义的手机类
	* A: 自定义的手机类
		* a: 案例代码
			public class Phone{
				/*
				    定义手机的属性
				*/
				String color ;
				String brand ;
				double size ; 
			}


### 05测试手机类
	* A: 调用方法执行流程
		* a: 实现引用类型的步骤
			* 1: 导入包 , 类都是在同一个文件夹,不需要导入包
			* 2: 创建引用类型的变量
			* 3: 变量.类型中的功能
		* b: 案例代码
			public class TestPhone{
				public static void main(String[] args){
					// 2: 创建引用类型的变量
					Phone p = new Phone();
					//System.out.println(p);  //输出内存的地址
				
			     	//3: 变量.类型中的功能
					//变量 p.的方式,调用类中的属性
					//属性就是变量 , 赋值和获取值
					p.color = "土豪金";
					p.brand = "爱立信";
					p.size = 5.0;
					
					//获取属性值
					System.out.println(p.color+"  "+p.brand+"  "+p.size);
				}
			}





### 06自定义类的内存图_1
	* A: 自定义类的内存图_1
		* a: 参见\day06\day06(面向对象\day06_source\对象内存图.JPG


### 07自定义类的内存图_2
	* A: 自定义类的内存图_1
		* a: 参见\day06\day06(面向对象\day06_source\对象内存图.JPG


### 08两个引用类型变量内存图
	* A: 自定义类的内存图_1
		* a: 参见\day06\day06(面向对象\day06_source\两个引用变量内存图.JPG


### 09自定义类的练习
	* A: 实体类的代码
		/*
		    电饭锅，包含属性（品牌、容量大小、颜色等）
			定义类,描述事物,电饭锅
			  属性: 品牌,大小 ,颜色
			
			定义类,类名字,电饭锅
			类的范围,定义三个属性
		*/
		public class DianFanGuo{
			//定义三个属性
			String brand ;
		    double size ;
			String color ;
		}
		
		/*
		   汽车，包含属性（品牌、排量、类型等）
		   定义类,类名 Car
		     属性 品牌 排量 类型
		 */
		public class Car{
			//定义汽车三个属性
			String brand ;
			double paiLiang ;
			String type;
		}
		
		 /*
		   学生，包含属性（姓名，年龄，性别等）
		   定义类,类名Student
		     三个属性: 姓名,年龄,性别 (char)
		*/
		public class Student{
			String name;
			int age ;
			char sex ;
		}

	* B: 测试类的代码
		/*
		   定义的测试类
		   同时测试,电饭锅,汽车,学生
		*/
		public class Test{
			public static void main(String[] args){
				//创建电饭锅引用类型
				DianFanGuo dfg = new DianFanGuo();
				
				dfg.brand = "特斯拉";
				dfg.color = "红色";
				dfg.size = 30;
				
				System.out.println(dfg.brand+"  "+dfg.color+"  "+dfg.size);
				
				//创建汽车引用类型
				Car c = new Car();
				c.brand = "巨力";
				c.type = "拖拉机";
				c.paiLiang = 0.5;
				
				System.out.println(c.brand+"  "+c.type+"  "+c.paiLiang);
				
				//创建学生引用类型
				Student stu = new Student();
				stu.name = "张三";
				stu.age = 20;
				stu.sex = '男';
				System.out.println(stu.name+"  "+stu.age+"  "+stu.sex);
				
			}
		}


	
### 10ArrayList创建变量的步骤
	* A: ArrayList创建变量的步骤
		* a: 导入包 java.util包中
		* b: 创建引用类型的变量
			数据类型< 集合存储的数据类型>  变量名 = new 数据类型<集合存储的数据类型>();
	   		集合存储的数据类型: 要将数据存储到集合的容器中
	   		创建集合引用变量的时候,必须要指定好,存储的类型是什么
		* c: 变量名.方法 
	    	注意: 集合存储的数据,8个基本类型对应8个引用类型
	 		存储引用类型,不存储基本类型
		
### 11ArrayList创建变量举例
	* A: ArrayList创建变量的示例代码
		import java.util.ArrayList;
		public class ArrayListDemo{
			public static void main(String[] args){
				//创建集合容器,指定存储的数据类型
				//存储字符串
				ArrayList<String> array = new ArrayList<String>();
				
				//创建集合容器,存储整数
				ArrayList<Integer> array2 = new ArrayList<Integer>();
				
				//创建集合容器,存储手机类型
				ArrayList<Phone> array3 = new ArrayList<Phone>();
			}
		}


### 12ArrayList的常见方法
	* A: ArrayList的常见方法
		* a: add(参数) 向集合中添加元素
		* b: get(int index) 取出集合中的元素,get方法的参数,写入索引
		* c: size() 返回集合的长度, 集合存储元素的个数
	* B: 案例代码
		import java.util.ArrayList;
		public class ArrayListDemo_1{
			public static void main(String[] args){
				//定义集合,存储字符串元素
				ArrayList<String> array = new ArrayList<String>();
				//调用集合方法add存储元素
				array.add("abc");
				array.add("itcast");
			    array.add("love");
				array.add("java");
				//输出集合的长度,调用集合方法size, size方法的返回值类型 int
				int size = array.size();
				System.out.println(size);
				
				//获取出集合中的一个元素,获取1索引的元素
				//集合的方法get, 获取元素后结果数据类型
				String s = array.get(1);
				System.out.println(s);
				
				
				System.out.println(array.get(0));
				System.out.println(array.get(1));
				System.out.println(array.get(2));
				System.out.println(array.get(3));
			}
		}


### 13ArrayList集合的遍历
	* A: 案例代码
		/*
		   集合的遍历
		   实现思想也是索引思想
		   集合的索引从0开始,到 size()-1
		   方法get(int index)
		*/
		import java.util.ArrayList;
		public class ArrayListDemo_2{
			public static void main(String[] args){
				ArrayList<Integer> array = new ArrayList<Integer>();
				array.add(121);
				array.add(125);
				array.add(123);
				array.add(120);
				array.add(128);
				
				//对集合进行遍历
				//使用方法 size+get组合进行遍历
				for(int i = 0 ; i < array.size(); i++){
					System.out.println( array.get(i) );
				}
			}
		}


### 14ArrayList补充方法
	* A: ArrayList补充方法
		* a: add(int 索引,存储的元素) 	将元素添加到指定的索引上
		* b: set(int 索引,修改后的元素) 	将指定索引的元素,进行修改
		* c: remove(int 索引) 			删除指定索引上的元素
		* d: clear() 					清空集合中的所有元素
	* B: 案例代码
		import java.util.ArrayList;
		public class ArrayListDemo_3{
			public static void main(String[] args){
				
				ArrayList<Integer> array = new ArrayList<Integer>();
				array.add(1);
				array.add(2);
				array.add(3);
				array.add(4);
				
				//在索引2上,添加元素7
				array.add(2,7);
				
				//将0索引上的元素,修改成10
				array.set(0,10);
				
				//将4索引上的元素,删除
				array.remove(4);
				
				array.clear();
				
				//使用方法 size+get组合进行遍历
				for(int i = 0 ; i < array.size(); i++){
					System.out.println( array.get(i) );
				}
			}
		}
			 



### 15随机点名器案例分析
	* A: 随机点名器案例分析
		全班同学中随机的找出一名同学，打印这名同学的个人信息。
		我们对本案例进行分析，得出如下分析结果：
			1.存储全班同学信息（姓名、年龄）
				将容器换成集合，集合中存的是Student类型
			2.打印全班同学每一个人的信息（姓名、年龄）
				 遍历集合
			3.在班级总人数范围内，随机产生一个随机数，查找该随机数所对应的同学信息（姓名、年龄）
			随机点名器明确地分为了三个功能。如果将多个独立功能的代码写到一起，则代码相对冗长，我们可以针对不同的功能可以将其封装到一个方法中，将完整独立的功能分离出来。
			而在存储同学姓名时，如果对每一个同学都定义一个变量进行姓名存储，则会出现过多孤立的变量，很难一次性将全部数据持有。此时，我们采用ArrayList集合来解决多个学生信息的存储问题


### 16随机点名器代码实现
	* A: 随机点名器案例代码
		/*
		   随机点名器,集合改进 (学生的姓名和年龄)
		   现实中有学生这个事物,使用定义类的形式,描述学生事物
		   属性: 姓名,年龄
		   
		   姓名存储了数组, 将容器换成是集合
		   String[] s = {"",""};
		   集合中,存储的是学生的姓名吗?  应该存储Student类型
		   
		   存储学生:
		      学生类型,存储到集合中
		   总览: 遍历集合
		   随机: 随机数,作为索引,到集合中找到元素
		   三个功能,共享的数据,集合容器,
		   定义三个方法,必须参数传递集合
		*/
		import java.util.ArrayList;
		import java.util.Random;
		public class CallName{
			public static void main(String[] args){
				//定义集合,存储的是StudentName类型变量
				ArrayList <StudentName> array = new ArrayList<StudentName>();
				//调用添加方法
				add (array);
				//调用遍历集合
				printArrayList(array);
				
				randomStudentName(array);
			}
			/*
			  随机数,当作集合的索引,到集合中找到元素
			*/
			public static void randomStudentName(ArrayList<StudentName> array ){
				Random r = new Random();
				int number = r.nextInt( array.size());
				//随机数,索引,到集合中get
				StudentName s = array.get(number);
				System.out.println( s.name +"  "+s.age);
			}
			
			/*
			    总览学生的信息,遍历集合
			*/
			public static void printArrayList(ArrayList<StudentName> array){
				for(int i = 0 ; i < array.size();i++){
					//存储集合的时候, 集合.add(sn1)  sn1 是StudentName类型变量
					//获取的时候,集合.get方法,获取出来的是什么, 还是StudentName类型变量
					StudentName s = array.get(i);
					System.out.println(s.name+"  "+s.age);
				}
			}
			
			/*
			   定义方法,实现存储学生的姓名和年龄
			   创建StudentName类型变量,存储到集合中
			*/
			public static void add (ArrayList<StudentName> array){
				//创建StudentName类型变量
				StudentName sn1 = new StudentName();
				StudentName sn2 = new StudentName();
				StudentName sn3 = new StudentName();
				StudentName sn4 = new StudentName();
				StudentName sn5 = new StudentName();
				
				sn1.name = "张三1";
				sn1.age = 201;
				
				sn2.name = "张三2";
				sn2.age = 202;
				
				sn3.name = "张三3";
				sn3.age = 203;
				
				sn4.name = "张三4";
				sn4.age = 204;
				
				sn5.name = "张三5";
				sn5.age = 205;
				
				//将StudentName变量,存储到集合中
				array.add(sn1);
				array.add(sn2);
				array.add(sn3);
				array.add(sn4);
				array.add(sn5);
			}
		}


### 17库存案例分析加入集合
	* A: 库存案例分析加入集合
		* a: 参见\day06\day06(面向对象\day06_source\对象内存图.JPG

### 18库存案例添加商品信息
	* A: 案例代码
		/*
		   定义,.描述商品的类
		   商品 4个属性
		     商品名字  大小     价格    库存
			  String    double   double  int
			  
			定义类,类名Goods
			这个类型的变量,存储到集合中
		*/
		public class Goods{
			//定义商品名字
			String brand ;
			//大小属性
			double size ;
			// 价格属性
			double price ;
			//库存属性
			int count ;
		}

		/*
		    实现库存管理案例:
			  1.存储商品信息
			    存储商品类型变量
				将商品类型的变量,存储到集合中
		*/
		//import java.util.ArrayList;
		import java.util.*;
		public class Shopp{
			public static void main(String[] args){
				//创建ArrayList集合,存储Goods类型
				ArrayList<Goods> array = new ArrayList<Goods>();
				//调用添加商品信息的方法
				addGoods(array);
			}
			
			/*
			   定义方法,将商品的信息存储到集合中
			   集合是所有方法的共享数据,参数传递
			*/
			public static void addGoods (ArrayList<Goods> array){
				//创建商品类型变量 Goods类型的变量
				Goods g1 = new Goods();
				Goods g2 = new Goods();
				g1.brand = "MacBook";
				g1.size = 13.3;
				g1.price = 9999.99;
				g1.count = 3;
				
				g2.brand = "Thinkpad";
				g2.size = 15.6;
				g2.price = 7999.99;
				g2.count = 1;
				
				//Goods类型的变量,存储到集合中
				array.add(g1);
				array.add(g2);
			}
		}


### 19库存案例查看库存清单
	* A: 案例代码
		/*
		    实现库存管理案例:
			  1.存储商品信息
			    存储商品类型变量
				将商品类型的变量,存储到集合中
				
		      2.查看库存清单
			    将集合进行遍历, 获取出集合中存储的Goods类型变量
				输出每一个Goods类型的属性
				计算求和: 总库存,总金额
		*/
		//import java.util.ArrayList;
		import java.util.*;
		public class Shopp{
			public static void main(String[] args){
				//创建ArrayList集合,存储Goods类型
				ArrayList<Goods> array = new ArrayList<Goods>();
				//调用添加商品信息的方法
				addGoods(array);
			}
		
			/*
			   定义方法,查看库存清单,遍历集合
			*/
			public static void printStore(ArrayList<Goods> array){
				//输出表头
				System.out.println("----------商场库存清单----------");
				System.out.println("品牌型号     尺寸    价格    库存数");
				//定义变量,保存总库存数,和总金额
				int totalCount = 0 ;
				double totalMoney = 0;
				//遍历集合
				for(int i = 0 ; i < array.size(); i++){
					//get(索引)获取出集合中的元素,存储的是Goods类,获取的也是Goods类型
					//使用Goods类型变量,接受get方法结果
					Goods g = array.get(i);
					System.out.println(g.brand+"   "+g.size+"    "+g.price+"    "+g.count);
					totalCount = totalCount+g.count;
					totalMoney = totalMoney + g.count*g.price;
				}
				System.out.println("总库存数: "+totalCount);
				System.out.println("商品库存总金额: "+totalMoney);
			}
			
			/*
			   定义方法,将商品的信息存储到集合中
			   集合是所有方法的共享数据,参数传递
			*/
			public static void addGoods (ArrayList<Goods> array){
				//创建商品类型变量 Goods类型的变量
				Goods g1 = new Goods();
				Goods g2 = new Goods();
				g1.brand = "MacBook";
				g1.size = 13.3;
				g1.price = 9999.99;
				g1.count = 3;
				
				g2.brand = "Thinkpad";
				g2.size = 15.6;
				g2.price = 7999.99;
				g2.count = 1;
				
				//Goods类型的变量,存储到集合中
				array.add(g1);
				array.add(g2);
			}
		}

### 20库存案例修改库存清单及测试代码的实现
	* A: 案例代码
		/*
		    实现库存管理案例:
			  1.存储商品信息
			    存储商品类型变量
				将商品类型的变量,存储到集合中
				
		      2.查看库存清单
			    将集合进行遍历, 获取出集合中存储的Goods类型变量
				输出每一个Goods类型的属性
				计算求和: 总库存,总金额
			
		     3.修改商品的库存
			    集合遍历 ,获取出集合中存储的Goods类型变量
				变量调用Goods类的属性count,值进行修改 (键盘输入)
		*/
		//import java.util.ArrayList;
		import java.util.*;
		public class Shopp{
			public static void main(String[] args){
				//创建ArrayList集合,存储Goods类型
				ArrayList<Goods> array = new ArrayList<Goods>();
				//调用添加商品信息的方法
				addGoods(array);
				//进入死循环中
				while(true){
					//调用选择功能的方法,获取到用户输入的功能序号
					int number = chooseFunction();
					//对序号判断,如果=1 进入查看库存功能  = 2 进入修改库存功能  =3 结束
					switch(number){
						case 1:
						//进入查看库存,调用查看库存的方法,传递存储商品信息的集合
						printStore(array);
						break;
						
						case 2:
						//进入修改库存功能,调用修改库存的方法,传递集合
						update(array);
						break;
						
						case 3:
						return ;
						
						default:
						 System.out.println("无此功能");
						 break;
					}
				}
			}
			/*
			  方法定义,修改库存
			  键盘的输入,将Goods中的属性值,修改
			*/
			public static void update(ArrayList<Goods> array){
				Scanner sc = new Scanner(System.in);
				//遍历集合,获取集合中的每个元素
				for(int i = 0 ;  i < array.size(); i++){
					//集合方法get获取的是集合的元素,元素类型Goods
					Goods g = array.get(i);
					System.out.println("请输入"+g.brand+"的库存数");
					//Goods属性,count进行修改
					g.count = sc.nextInt();
				}
			}
			/*
			   定义方法,实现选择菜单,用户根据功能选择菜单
			*/
			public static int chooseFunction(){
				System.out.println("-------------库存管理------------");
				System.out.println("1.查看库存清单");
				System.out.println("2.修改商品库存数量");
				System.out.println("3.退出");
				System.out.println("请输入要执行的操作序号：");
				Scanner sc = new Scanner(System.in);
				int number = sc.nextInt();
				return number;
			}
			
			/*
			   定义方法,查看库存清单,遍历集合
			*/
			public static void printStore(ArrayList<Goods> array){
				//输出表头
				System.out.println("----------商场库存清单----------");
				System.out.println("品牌型号     尺寸    价格    库存数");
				//定义变量,保存总库存数,和总金额
				int totalCount = 0 ;
				double totalMoney = 0;
				//遍历集合
				for(int i = 0 ; i < array.size(); i++){
					//get(索引)获取出集合中的元素,存储的是Goods类,获取的也是Goods类型
					//使用Goods类型变量,接受get方法结果
					Goods g = array.get(i);
					System.out.println(g.brand+"   "+g.size+"    "+g.price+"    "+g.count);
					totalCount = totalCount+g.count;
					totalMoney = totalMoney + g.count*g.price;
				}
				System.out.println("总库存数: "+totalCount);
				System.out.println("商品库存总金额: "+totalMoney);
			}
			
			/*
			   定义方法,将商品的信息存储到集合中
			   集合是所有方法的共享数据,参数传递
			*/
			public static void addGoods (ArrayList<Goods> array){
				//创建商品类型变量 Goods类型的变量
				Goods g1 = new Goods();
				Goods g2 = new Goods();
				g1.brand = "MacBook";
				g1.size = 13.3;
				g1.price = 9999.99;
				g1.count = 3;
				
				g2.brand = "Thinkpad";
				g2.size = 15.6;
				g2.price = 7999.99;
				g2.count = 1;
				
				//Goods类型的变量,存储到集合中
				array.add(g1);
				array.add(g2);
			}
		}
## 练习

### 01奇数求和练习
	* A: 奇数求和练习
		* a: 题目分析
			* 为了记录累加和的值，我们需要定义一个存储累加和的变量
			* 我们要获取到1-100范围内的数
			* 判断当前数是否为奇数，是奇数，完成累加和操作
			* 累加完毕后，最终显示下累加和的值

		* b: 解题步骤
			* 定义一个用来记录累加和的变量
			* 使用for循环语句，完成1-100之间每个数的获取
			* 使用if条件语句，判断当前数是否是奇数，是奇数，进行累加和操作
			* 使用输出语句，打印累加和变量的值

		* c: 案例代码
			public class Test01 {
				public static void main(String[] args) {
					int sum = 0;
					for (int i = 0; i < 100; i++) {
						if (i%2==1) {
							sum += i;
						}
					}
					System.out.println("累加和的值 " + sum);
				}
			}
	
### 02水仙花练习功能实现
	* A: 水仙花练习功能实现
		* a: 题目分析
			* 明确什么样的数就是水仙花数。水仙花数是指一个3位数（100-999之间），其每位数字立方之和等于该3位数本身。
				如153 = 1*1*1 + 3*3*3 + 5*5*5，即 3位数本身 = 百位数立方 + 十位数立方 + 个位数立方;
			* 获取水仙花范围内的所有3位数（100-999之间的每个3位数）
			* 判断该3位数是否满足水仙花数，满足，打印该3位数
			
		* b: 解题步骤
			* 使用for循环，得到100-999之间的每个3位数
			* 获取3位数中百位数字、十位数字、个位数字
			* 使用if条件语句，判断该3位数是否满足水仙花数，满足，使用输出语句，打印该3位数
			
		* c: 案例代码
			public class Test02 {
				public static void main(String[] args) {
					for (int i = 100; i < 1000; i++) {
						int bai = i/100%10;
						int shi = i/10%10;
						int ge = i%10;
						
						if (i == bai*bai*bai + shi*shi*shi + ge*ge*ge) {
							System.out.println(i);
						}
					}
				}
			}			
			
### 03ASCII编码表
	* A: ASCII编码表
		* a: 英文全称
			* American Standard Code for Information Interchange，美国标准信息交换代码
		* b: ASCII编码表由来
			* 计算机中，所有的数据在存储和运算时都要使用二进制数表示
			* a、b、c、d这样的52个字母（包括大写）、以及0、1等数字还有一些常用的符号, 在计算机中存储时也要使用二进制数来表示
			* 具体用哪些二进制数字表示哪个符号，当然每个人都可以约定自己的一套（这就叫编码）
			* 大家如果要想互相通信而不造成混乱，那么大家就必须使用相同的编码规则，于是美国有关的标准化组织就出台了ASCII编码，
				统一规定了上述常用符号用哪些二进制数来表示。
		* c: 中文编码表
			* GB2312
			* UNICODE
		* d: 字符中重要的ASCII码对应关系
			* a : 97
			* A : 65
			* 0 : 48
			
	

### 04char类型的存储
	* A: char类型的存储
		* a: 取值范围
			* short:占两个字节,是有符号数据,取值范围-32768-32767
			* char: 占两个字节,是无符号数据,取值范围0-65536
			
		* b: 类型转换
			* char类型的数据参加运算时要线程程int数据类型
			
		* c: 案例代码
			/*
				ASCII编码表演示
				字符Java 数据类型,char
				整数Java 数据类型,int
				
				int 类型和 char 数据类型转换
				char  两个字节, int 四个字节
				
				char转成int类型的时候,类型自动提示,char数据类型,会查询编码表,得到整数
				int转成char类型的时候,强制转换,会查询编码表
				
				char存储汉字,查询Unicode编码表
				
				char可以和int计算,提示为int类型, 内存中两个字节
				char取值范围是0-65535, 无符号的数据类型
			*/
			public class ASCIIDemo{
				public static void main(String[] args){
					char c = 'a';
					int i = c + 1;
					System.out.println(i);
					
					int j = 90;
					char h = (char)j;
					System.out.println(h);
					
					System.out.println( (char)6 );
					
					char k = '你';
					System.out.println(k);
					
					
					char m = -1;
				}
			}	

### 05输出所有英文字母
	* A: 输出所有英文字母
		* a: 题目分析
			* 一共26个大小写字母，那么，可以考虑循环26次。在每次循环中，完成指定字母的大小写打印
			* 找出ABCDEFG…XYZ这些字母之间的变化规律
				通过ASCII表发现，后面的字母比它前面的字母，ASCII值大1
				下一个字母 = 上一个字母 + 1
				如： A	B	C	D
					65	66	67	68
			* 在每次循环中打印上一个字母大小写，并指定下一个字母

		* b: 解题步骤
			* 定义初始化大写变量，值为’A’； 初始化小写变量，值为’a’
			* 使用for循环，进行26次循环
			* 在每次循环中，打印大写字母、小写字母。
				每次打印完成后，更新大写字母值、小写字母值

		* c: 案例代码
			public class Test04 {
				public static void main(String[] args) {
					char da = 'A';
					char xiao = 'a';
					for (int i = 0; i < 26; i++) {
						System.out.println("大写字母 "+da+" ,小写字母 "+xiao);
						da++; //更新大写字母值
						xiao++; //更新小写字母值
					}
				}
			}
			
### 0699乘法表的分析
	* A: 99乘法表的分析
		* a: 打印格式
			1*1=1
			1*2=2  2*2=4
			1*3=3  2*3=6  3*3=9
		* b: 题目分析
			通过观察发现，如果把1*1=1这样的内容 看做一颗*的话，那么打印结果就成了如下效果：
			*
			**
			***
			****
			…
			这样，就是打印9行星，每行打印星的个数与当前行数相等。
			再观察“1*3=3 2*3=6 3*3=9”得出它们如下的变化规律：
					每行第n次 +"*"+ 行号 +"="+ 每行第n次 * 行号
				如:	1	+"*"+  2    +"="+   1*2; // 相当于1*2=2
					2	+"*"+  2    +"="+   2*2; // 相当于2*2=4	

		* c: 解题步骤
			* 定义一个外层for循环，初始值从1开始，循环9次。用来控制打印的行数
			* 在外层for循环内部，定义一个for循环，初始值从1开始，循环次数与当前行数相等。用来完成每行打印指定次数的乘法公式 如1*1=1
			* 在内层for循环中，完成每行指定次数的乘法公式打印 如1*1=1
				System.out.print(k +"*"+ j +"="+ j*k +"\t");
				// 变量k代表：每行中的第n次
				// 变量j代表：行号
			* 在外循环中，当每行指定次数的乘法公式打印完毕后，通过System.out.println()切换到下一行。
				这样，再次打印乘法公式时，就在下一行输出打印了

### 0799乘法表的功能实现
	* A: 99乘法表的功能实现
		* a: 案例代码
			/*
				利用嵌套for循环,实现99乘法表示
				实现步骤:
				  1. 定义外循环控制行数
				  2. 内循环控制个数,个数,每次都在递增
				  3. 循环中输出,乘法表的格式   1*3=3
			*/
			
			public class Test05 {
				public static void main(String[] args) {
					for (int j = 1; j < 10; j++) {
						for (int k = 1; k <= j; k++) {
							System.out.print(k +"*"+ j +"="+ j*k +"\t");
						}
						System.out.println();
					}
				}
			}

				



### 08实现数组的遍历
	* A: 实现数组的遍历
		* a: 题目分析
			* 通过循环，我们可以完成数组中元素的获取，数组名[索引]
			* 观察发现，每个数组元素之间加入了一个逗号”,”进行分隔；并且，整个数组的前后有一对中括号”[]”包裹数组所有元素。
			
		* b: 解题步骤
			* 使用输出语句完成打印 左边的中括号”[”
			* 使用循环，输出数组元素值。输出元素值分为两种情况，如下：
				* 最后一个数组元素，加上一个右边的中括号”]”
				* 非最后一个数组元素，加上一个逗号”,”
				
		* c: 案例代码
			/*
				定义方法,实现数组的遍历
				遍历中,输出结果  [11,33,565,66,78,89]
				int[] arr = {3,4,45,7};
				结果包含字符串, [  ]  ,
				实现步骤:
				  1. 定义方法实现数组的遍历
				  2. 先打印[ 中括号
				  3. 遍历数组
					输出数组的元素和逗号
					判断是否遍历到了数组的最后一个元素,如果是最后一个元素,输出]中括号
			*/
			public class ArrayMethodTest{
				public static void main(String[] args){
					int[] arr = {11,44,55,33,66};
					printArray(arr);
					
					int[] arr2 = {22,88,99,33,66};
					printArray(arr2);
					
				}
				/*
				   定义方法,实现功能
				   返回值: void
				   方法参数: 数组
				*/
				public static void printArray(int[] arr){
					//输出一半中括号,不要换行打印
					System.out.print("[");
					//数组进行遍历
					for(int i = 0 ; i < arr.length ; i++){
						//判断遍历到的元素,是不是数组的最后一个元素
						//如何判断 循环变量 到达 length-1
						if( i == arr.length-1 ){
							//输出数组的元素和]
							System.out.print(arr[i]+"]");
						}else{
						//不是数组的最后一个元素,输出数组元素和逗号
							System.out.print(arr[i]+",");
						}
					}
					System.out.println();
				}
			}
		

### 09数组逆序原理
	* A: 数组逆序原理
		* a: 题目分析(图解见day07_source/数组的逆序原理.JPG)
			* 通过观察发现，本题目要实现原数组元素倒序存放操作。即原数组存储元素为{11,22,33,44}，
				逆序后为原数组存储元素变为{44,33,22,11}。
			* 通过图解发现，想完成数组元素逆序，其实就是把数组中索引为start与end的元素进行互换。
			* 每次互换后，start索引位置后移，end索引位置前移，再进行互换
			* 直到start位置超越了end位置，互换结束，此时，数组元素逆序完成。
			
		* b: 解题步骤
			* 定义两个索引变量start值为0，变量end值为数组长度减去1（即数组最后一个元素索引）
			* 使用循环，完成数组索引start位置元素与end位置元素值互换。
			* 在循环换过程中，每次互换结束后，start位置后移1，end位置前移1
			* 在循环换过程中，最先判断start位置是否超越了end位置，若已超越，则跳出循环
			
		
### 10数组逆序功能实现			
	* A：案例代码
		/*
		   数组的逆序:
			 数组中的元素,进行位置上的交换
			 逆序 不等于 反向遍历
			 就是数组中最远的两个索引,进行位置交换,实现数组的逆序
			 使用的是数组的指针思想,就是变量,思想,可以随时变换索引
			 反转 reverse
			 实现步骤:
			   1. 定义方法,实现数组的逆序
			   2. 遍历数组
				 实现数组的最远索引换位置
				 使用临时的第三方变量
		*/
		public class ArrayMethodTest_1{
			public static void main(String[] args){
				int[] arr = {3,5,7,1,0,9,-2};
				//调用数组的逆序方法
				reverse(arr);
				//看到数组的元素,遍历
				printArray(arr);
			}
			
			/*
			   定义方法,实现数组的逆序
			   返回值: 没有返回值
			   参数:   数组就是参数
			*/
			public static void reverse(int[] arr){
				//利用循环,实现数组遍历,遍历过程中,最远端换位
				//for的第一项,定义2个变量, 最后,两个变量++ --
				for( int min = 0 , max = arr.length-1 ; min < max  ; min++,max--){
					//对数组中的元素,进行位置交换
					//min索引和max索引的元素交换
					//定义变量,保存min索引
					int temp = arr[min];
					//max索引上的元素,赋值给min索引
					arr[min] =  arr[max];
					//临时变量,保存的数据,赋值到max索引上
					arr[max] = temp;
				}
			}
		}

### 11选择排序原理
	* A: 选择排序原理
		* a: 题目分析(图解见day07_source/选择排序原理.JPG)
			* 通过观察发现，本题目要实现把数组元素{13,46,22,65,3}进行排序
			* 提到数组排序，就要进行元素值大小的比较，通过上图发现，我们想完成排序要经过若干次的比较才能够完成。
			* 上图中用每圈要比较的第一个元素与该元素后面的数组元素依次比较到数组的最后一个元素，把小的值放在第一个数组元素中，数组循环一圈后，则把最小元素值互换到了第一个元素中。
			* 数组再循环一圈后，把第二小的元素值互换到了第二个元素中。按照这种方式，数组循环多圈以后，就完成了数组元素的排序。这种排序方式我们称为选择排序。

			
		* b: 解题步骤
			* 使用for循环（外层循环），指定数组要循环的圈数（通过图解可知，数组循环的圈数为数组长度 - 1）
			* 在每一圈中，通过for循环（内层循环）完成数组要比较的第一个元素与该元素后面的数组元素依次比较到数组的最后一个元素，把小的值放在第一个数组元素中
			* 在每一圈中，要参与比较的第一个元素由第几圈循环来决定。如上图所示
				* 进行第一圈元素比较时，要比较的第一个元素为数组第一个元素，即索引为0的元素
				* 进行第二圈元素比较时，要比较的第一个元素为数组第二个元素，即索引为1的元素
				* 依次类推，得出结论：进行第n圈元素比较时，要比较的第一个元素为数组第n个元素，即数组索引为n-1的元素
				
### 12选择排序功能实现
	* A: 案例代码
		/*
		  数组的排序: 一般都是升序排列,元素,小到大的排列
		  
		  两种排序的方式
			 选择排序: 数组的每个元素都进行比较
			 冒泡排序: 数组中相邻元素进行比较
			 规则: 比较大小,位置交换
		*/
		public class ArrayMethodTest_2{
			public static void main(String[] args){
				int[] arr  = {3,1,4,2,56,7,0};
				//调用选择排序方法
				//selectSort(arr);
				printArray(arr);
			}
			/*
				定义方法,实现数组的选择排序
				返回值: 没有
				参数:  数组
				实现步骤:
				  1.嵌套循环实现排序
					外循环,控制的是一共比较了多少次
					内循环,控制的是每次比较了多少个元素
				  2. 判断元素的大小值
					小值,存储到小的索引
			*/
			public static void selectSort(int[] arr){
				for(int i = 0 ; i < arr.length - 1; i++){
					//内循环,是每次都在减少,修改变量的定义
					for(int j = i+1 ; j < arr.length ; j++){
						//数组的元素进行判断
						if(arr[i] > arr[j]){
							//数组的换位
							int temp = arr[i];
							arr[i] = arr[j];
							arr[j] = temp; 
						}
					}
				}
			}
			
			/*
			   定义方法,实现功能
			   返回值: void
			   方法参数: 数组
			*/
			public static void printArray(int[] arr){
				//输出一半中括号,不要换行打印
				System.out.print("[");
				//数组进行遍历
				for(int i = 0 ; i < arr.length ; i++){
					//判断遍历到的元素,是不是数组的最后一个元素
					//如何判断 循环变量 到达 length-1
					if( i == arr.length-1 ){
						//输出数组的元素和]
						System.out.print(arr[i]+"]");
					}else{
					//不是数组的最后一个元素,输出数组元素和逗号
						System.out.print(arr[i]+",");
					}
				}
				System.out.println();
			}
		}
		
### 13冒泡排序功能实现
	* A: 冒泡排序功能实现
			* a: 题目分析
				* 通过观察发现，本题目要实现把数组元素{13,46,22,65,3}进行排序
				* 提到数组排序，就要进行元素值大小的比较，通过上图发现，我们想完成排序要经过若干次的比较才能够完成。
				* 上图中相邻的元素值依次比较，把大的值放后面的元素中，数组循环一圈后，则把最大元素值互换到了最后一个元素中。
					数组再循环一圈后，把第二大的元素值互换到了倒数第二个元素中。按照这种方式，数组循环多圈以后，
					就完成了数组元素的排序。这种排序方式我们称为冒泡排序。
					
			* b: 解题步骤
				* 使用for循环（外层循环），指定数组要循环的圈数（通过图解可知，数组循环的圈数为数组长度 - 1）
				* 在每一圈中，通过for循环（内层循环）完成相邻的元素值依次比较，把大的值放后面的元素中
				* 每圈内层循环的次数，由第几圈循环来决定。如上图所示
					* 进行第一圈元素比较时，内层循环次数为数组长度 - 1
					* 进行第二圈元素比较时，内层循环次数为数组长度 - 2
					* 依次类推，得出结论：进行第n圈元素比较时，内层循环次数为数组长度 - n
					
			* c: 案例代码	
				/*
				  数组的排序: 一般都是升序排列,元素,小到大的排列
				  
				  两种排序的方式
					 选择排序: 数组的每个元素都进行比较
					 冒泡排序: 数组中相邻元素进行比较
					 规则: 比较大小,位置交换
				*/
				public class ArrayMethodTest_2{
					public static void main(String[] args){
						int[] arr  = {3,1,4,2,56,7,0};
						//调用选择排序方法
						//selectSort(arr);
						
						//调用冒泡排序方法
						bubbleSort(arr);
						printArray(arr);
					}
					/*
					   定义方法,实现数组的冒泡排序
					   返回值: 没有
						参数:  数组
					*/
					public static void bubbleSort(int[] arr){
						for(int i = 0 ; i < arr.length - 1; i++){
							//每次内循环的比较,从0索引开始, 每次都在递减
							for(int j = 0 ; j < arr.length-i-1; j++){
								//比较的索引,是j和j+1
								if(arr[j] > arr[j+1]){
									int temp = arr[j];
									arr[j] = arr[j+1];
									arr[j+1] = temp;
								}
							}
						}
					}
					
					/*
					   定义方法,实现功能
					   返回值: void
					   方法参数: 数组
					*/
					public static void printArray(int[] arr){
						//输出一半中括号,不要换行打印
						System.out.print("[");
						//数组进行遍历
						for(int i = 0 ; i < arr.length ; i++){
							//判断遍历到的元素,是不是数组的最后一个元素
							//如何判断 循环变量 到达 length-1
							if( i == arr.length-1 ){
								//输出数组的元素和]
								System.out.print(arr[i]+"]");
							}else{
							//不是数组的最后一个元素,输出数组元素和逗号
								System.out.print(arr[i]+",");
							}
						}
						System.out.println();
					}
				}

### 14数组的折半查找原理
	* A: 数组的折半查找原理(图解见day07_source/折半查找原理.JPG)
			* a: 题目分析
				* 通过观察发现，本题目要实现查找指定数值在元素有序的数组中存储的位置（索引），返回该位置（索引）。
				* 我们使用数组最中间位置的元素值与要查找的指定数值进行比较，若相等，返回中间元素值的索引
				* 最中间位置的元素值与要查找的指定数值进行比较，若不相等，则根据比较的结果，缩小查询范围为上次数组查询范围的一半；
					再根据新的查询范围，更新最中间元素位置，然后使用中间元素值与要查找的指定数值进行比较
						比较结果相等，返回中间元素值的索引
						比较结果不相等，继续缩小查询范围为上次数组查询范围的一半，更新最中间元素位置，继续比较，依次类推。
				* 当查询范围缩小到小于0个元素时，则指定数值没有查询到，返回索引值-1。
				
			* b: 解题步骤
				* 定义3个用来记录索引值的变量，变量min记录当前范围最小索引值，初始值为0；变量max记录当前范围最大索引值，初始值为数组长度-1；变量mid记录当前当前范围最中间元素的索引值，初始值为(min+max) / 2
				* 使用循环，判断当前范围下，最中间元素值与指定查找的数值是否相等
					若相等，结束循环，返回当前范围最中间元素的索引值mid
					若不相等，根据比较结果，缩小查询范围为上一次查询范围的一般
					中间元素值 比 要查询的数值大，说明要查询的数值在当前范围的最小索引位置与中间索引位置之间，此时，更新查询范围为:
						范围最大索引值 = 上一次中间索引位置 -1；
					中间元素值 比 要查询的数值小，说明要查询的数值在当前范围的最大索引位置与中间索引位置之间，此时，更新查询范围为:
						范围最小索引值 = 上一次中间索引位置 +1；
					在新的查询范围中，更新中间元素值的位置，再次使用最中间元素值与指定查找的数值是否相等。
						中间索引值 = (范围最小索引值 +范围最大索引值) / 2;
				* 每次查询范围缩小一半后，使用if语句判断，查询范围是否小于0个元素，若小于0个元素，则说明指定数值没有查询到，返回索引值-1。
				
### 15数组的折半查找代码实现
	* A: 案例代码
		/*
		   数组的查找功能
			 在一个数组中,找一个元素,是否存在于数组中,如果存在,就返回索引
			 
			 普通查询:
			   找到元素在数组中出现的索引,如果没有这个 元素,结果就是负数
				
		*/
		public class ArrayMethodTest_3{
			 public static void main(String[] args){
				 int[] arr = {1,3,5,7,9,11,15};
				 int index = binarySearch(arr,10);
				 System.out.println(index);
				 
			 }
			 
			 /*
				 定义方法,实现,折半查找
				 返回值: 索引
				 参数: 数组,被找的元素 
				 实现步骤:
				   1. 需要的变量定义
					  三个,三个指针
					  
				   2. 进行循环折半
					  可以折半的条件  min <= max
				   
				   3. 让被找元素,和中间索引元素进行比较
					   元素 > 中间索引  小指针= 中间+1
					   元素 < 中间索引  大指针= 中间-1
					   元素 == 中间索引  找到了,结束了,返回中间索引
					   
					4. 循环结束,无法折半
					  元素没有找到 ,返回-1
			 */
			 public static int binarySearch(int[] arr, int key){
				 //定义三个指针变量
				 int min = 0 ;
				 int max = arr.length -1 ;
				 int mid = 0;
				 //循环折半,条件 min<=max
				 while( min <= max){
					 //公式,计算中间索引
					 mid = (min+max)/2;
					 //让被找元素,和中间索引元素进行比较
					 if(key > arr[mid]){
						 min = mid + 1;
					 }else if (key < arr[mid]){
						 max = mid - 1;
					 }else{
						 //找到元素,返回元素索引
						 return mid;
					 }
				 }
				 return -1;
			 }
			 
			/*
			   定义方法,实现数组的普通查询
			   返回值: 索引
			   参数:   数组, 被找的元素
			   
			   实现步骤:
				 1. 遍历数组
				 2. 遍历过程中,使用元素和数组中的元素进行比较
					如果相同,返回元素在数组中的索引
					如果不同,返回负数
			*/
			public static int search(int[] arr, int key){
				//遍历数组
				for(int i = 0 ; i < arr.length ; i++){
					//数组元素,被查找的元素比较
					if(arr[i] == key){
						//返回索引
						return i;
					}
				}
				return -1;
			}
		}
				

### 16总结
* 把今天的知识点总结一遍。

## Eclipse

### 01Eclipse的下载安装
	* A: Eclipse的下载安装		
		* a: 下载
			* http://www.eclipse.org
		* b: 安装
			* 只需要解压后就能使用
		* c: 卸载
			* 只需要将文件夹删除就可以了
		* d: 注意 
			* 开发软件的安装目录中，尽量不要出现空格与中文
	* B: Eclipse的特点
		* a: 免费
		* b: 纯Java语言编写
		* c: 免安装
		* d: 扩展性强
		
### 02Eclipse的工作空间和新建工程
	* A: Eclipse的工作空间和新建工程
		* a: 工作空间
			*  其实就是我们写的源代码所在的目录						
		* b: 创建工程(项目)
			* 右键/Package Explore 空白区/new /Java Project/输入项目名称如day08/			
		* c: 创建包(后面讲包的概念)
			*　打开上面建立的day08项目/右键/new/package/在弹出的对话框的name中输入报名如"com.itheima.tests"/finish
		* d: 创建类
			* 创建一个java类:右击包名/new/class/在对话框的name中输入类名/finish
	* B: 编译与执行
		* a: 编译
			* 自动编译，当java代码保存的时候，自动 编译class文件
		* b: 运行
			* 方式1：点击菜单工具栏中的 绿色带有三角形的 run按钮 运行
			* 方式2：点击菜单栏中Run， 点击Run 运行  快捷键是 ctrl+F11
			* 方式3：选中要运行的java文件，或者在编写代码的空白区域，右键选择 Run As --> 运行java程序

			
### 03Eclipse的HelloWorld编写
	* A:HelloWorld编写
		* a: 编写过程(参照上个知识点)
			* 建立day08项目
			* 建立包结构(包的概念还没有学到,不建立包的话,使用默认包结构default)
			* 创建HelloWorld类(自动生成main方法)
		* b: 案例代码
			public class HelloWorld {
				public static void main(String[] args) {
					System.out.println("Hello World");
				}
			}
			
	

### 04Eclipse的字体设置
	* A: Eclipse的字体设置
		* a: 修改编译环境和运行环境
			* 编译环境：Window -- Preferences – Java - Compiler
			* 运行环境：Window -- Preferences – Java - Installed JREs
			
		* b: 显示行号与隐藏行号
			* 显示：在代码区域的左边空白区域，右键 -- Show Line Numbers
			* 隐藏：将上面的操作再做一遍
			
		* c: 更改字体大小与颜色
			* Java代码区域的字体大小和颜色：
				* window -- Preferences -- General -- Appearance -- Colors And Fonts --Java修改 -- Java Edit Text Font--edit进行修改
			* 控制台
				* window -- Preferences -- General -- Appearance -- Colors And Fonts -- Debug -- Console font
			* 其他文件
				* window -- Preferences -- General -- Appearance -- Colors And Fonts -- Basic -- Text Font
				

### 05Eclipse的窗口设置
	* A: 窗口设置
		* a: 显示的窗口乱了，还原默认显示模式
			* Window – Perspective -- Reset Prespective
		* b: 显示控制台
			* Window--Show View—Console		
			
### 06Eclipse的去掉多余的注释
	* A: Eclipse的去掉多余的注释
		* a:如何去掉默认注释
			* Window -- Preferences -- Java -- Code Style -- Code Templates -- Comments – Methods，点击Edit ，将注释部分删除 (不建议删除)
			* Window -- Preferences -- Java -- Code Style -- Code Templates -- Code -- Method body，点击Edit ，将注释部分删除
		* b: 切换工作空间
			* File – Switch Workspace – 指定工作空间 – ok
			
### 07Eclipse的快捷键
	* A: Eclipse的快捷键
		* a: 内容辅助键  Alt+/
			* 自动补齐main方法  main 然后 Alt+/
			* 自动补齐输出语句  syso 然后 Alt+/
		* b: 格式化代码
			* Ctrl+Shift+f
			* 代码区域右键 -- Source – Format
		* c: 自动导包
			* Ctrl+Shift+o
			* 如果当前类在多个包中都存在，这时候，使用Ctrl+shift+o,进行选择一个包导入即可。
		* d: 注释
			* 单行注释
				* 加注释： 先选中需要注释的内容，然后 Ctrl+/
				* 取消注释：先选中需要取消注释的内容， 然后 Ctrl+/
			* 多行注释
				* 加注释： 先选中需要注释的内容，然后 Ctrl+Shift+/
				* 取消注释：先选中需要取消注释的内容， 然后 Ctrl+Shift+\
		* e: 补充
			* 代码上下移动
				* 选中代码alt+上/下箭头
			* 查看源码
				* 选中类名(F3或者Ctrl+鼠标点击)
			* 查找具体的类 
				* ctrl + shift + t，输入要查找的类的名称-->确定
			* 查找具体类的具体方法 
				* ctrl + o
			* 给建议 
				* ctrl+1,根据右边生成左边的数据类型,生成方法
			* 删除代码 
				* ctrl + d
			* 抽取方法
				* alt + shift + m 
			* 改名
				* alt + shift + r（类名，方法名，变量名）
				
### 08Eclipse的断点调试
	* A:断点调试(又称为Debug调试)的作用
		* 调试程序
		* 查看程序执行流程
	* B:如何查看程序执行流程		
		* 什么是断点：
			* 就是一个标记，从哪里开始。
			
		* 如何设置断点：
			* 你想看哪里的程序，你就在那个有效程序的左边双击即可。
			
		* 在哪里设置断点：
			* 哪里不会点哪里。
			* 目前：我们就在每个方法的第一条有效语句上都加。
			
		* 如何运行设置断点后的程序：
			* 右键 -- Debug as -- Java Application
			
		* 看哪些地方：
			* Debug：断点测试的地方
				* 在这个地方，记住F6，或者点击也可以。一次看一行的执行过程。
			* Variables：查看程序的变量变化
			* ForDemo：被查看的源文件
			* Console：控制台
			
		* 如何去断点：
			* a:再次双击即可
			* b:找到Debug视图，Variables界面，找到Breakpoints，并点击，然后看到所有的断点，最后点击那个双叉		

### 09Eclipse的工程删除和导入
	* A:删除项目
		* 选中项目 – 右键 – 删除
			* 从项目区域中删除
			* 从硬盘上删除
	* B:导入项目
		* 在项目区域右键找到import
		* 找到General，展开，并找到
		* Existing Projects into Workspace
		* 点击next,然后选择你要导入的项目
		* 注意：这里选择的是项目名称



## 超市管理系统
### 10超市管理系统功能介绍			
	* A：超市管理系统功能介绍
		* a: 显示主菜单
		
			============欢迎光临ItCast超市============
			1: 货物 清单   2: 添加货物   3: 删除货物   4: 修改货物  5: 退出
			请您输入要操作的功能序号
			
		* b: 货物清单
		
			输入1:货物清单
			================商品库存清单================
			商品编号         商品名称                商品单价
			9527   			少林寺酥饼核桃        	   12.7
			9008   			尚康杂粮牡丹饼       	   5.6
			9879   			新疆原产哈密瓜             599.6
			
		* c: 添加新货物
		
			输入2:添加新货物	
			
			请输入新商品的编号:9523
			请输入新商品的名字:斯柯达苹果醋
			请输入新商品的单价:19.9
			商品添加成功
			
		* d: 删除货物
		
			输入3:删除货物
			
			选择的是删除功能
			请输入商品的编号:9523
			货物信息删除完毕
			
		* e: 修改货物
		
			输入4:修改货物
			
			选择的是修改功能
			请输入您要修改的商品的编号:9527
			输入新的商品编号:100
			输入新的商品名字:味道好凤梨干
			输入新的商品价格:6.5
			商品修改成功
		* f: 输入5:退出系统


### 11超市管理系统案例分析
	* A: 超市管理系统案例分析
		* 完成超市商品初始化。创建商品，将商品添加到集合
		* 显示来到超市能做的操作，也就是显示主菜单
		* 根据接收到的功能选项，执行对应的功能
		* 库存货物查询
		* 添加新货物	
		* 删除货物
		* 修改货物
		* 退出系统,结束main方法的运行
		* 循环，回到 2.显示主菜单

				
### 12自定义商品类
	* A: 自定义商品类
		* a: 目的
			* 每种库存商品都拥有多项商品信息，为了方便管理每种商品的信息，我们对商品信息进行封装，编写FruitItem.java文件
		* b：案例代码
			public class FruitItem {
				int  ID;			//商品编号
				String  name;		//商品名称
				double  price;		//商品单价
				double  number;		//商品数量
				double  money;		//商品金额
			}
		* 补充
			* 上述代码中，对商品信息（编号、名称、单价、数量、金额）进行了封装。这样做的好处在于以后只要找到这个商品，就能够知道该商品的每项信息了。

### 13初始化商品属性
	* A: 初始化商品属性
		* a: 案例代码
			import java.util.ArrayList;
			import java.util.Scanner;

			/*
			 *   超市管理系统主
			 *   实现:
			 *     1. 商品数据的初始化
			 *     2. 用户的菜单选择
			 *     3. 根据选择执行不同的功能
			 *       3.1 Read    查看商品
			 *       3.2 Create  添加商品
			 *       3.3 Delete  删除商品
			 *       3.4 Update  修改商品
			 *       
			 *       
			 *   所有功能 ,必须定义方法实现
			 *   主方法main  调用作用
			 */
			public class Shopp {

				public static void main(String[] args) {
					//创建ArrayList集合,存储商品类型,存储数据类型FruitItem类型
					ArrayList<FruitItem> array = new ArrayList<FruitItem>();
					//调用商品初始化方法,传递集合
					init(array);
					
					}
				}	
				/*
				 * 定义方法,实现商品数据的初始化
				 * 先将一部分数据,存储集合中
				 * 返回值: 无
				 * 参数 : 集合
				 * 方法名: init
				 */
				public static void init(ArrayList<FruitItem> array){
					//创建出多个FruitItem类型,并且属性赋值
					FruitItem f1 = new FruitItem();
					f1.ID = 9527;
					f1.name = "少林寺酥饼核桃";
					f1.price = 12.7;
					
					FruitItem f2 = new FruitItem();
					f2.ID = 9008;
					f2.name = "尚康杂粮牡丹饼";
					f2.price = 5.6;
					
					FruitItem f3 = new FruitItem();
					f3.ID = 9879;
					f3.name = "新疆原产哈密瓜";
					f3.price = 599.6;
					
					//创建的3个FruitItem类型变量,存储到集合中
					array.add(f1);
					array.add(f2);
					array.add(f3);
				}
				
			}


### 14主菜单功能
	* A: 主菜单功能
		* a: 案例代码
			
			import java.util.ArrayList;
			import java.util.Scanner;
			/*
			 *   超市管理系统主
			 *   实现:
			 *     1. 商品数据的初始化
			 *     2. 用户的菜单选择
			 *     3. 根据选择执行不同的功能
			 *       3.1 Read    查看商品
			 *       3.2 Create  添加商品
			 *       3.3 Delete  删除商品
			 *       3.4 Update  修改商品
			 *       
			 *       
			 *   所有功能 ,必须定义方法实现
			 *   主方法main  调用作用
			 */
			public class Shopp {

				public static void main(String[] args) {
					//创建ArrayList集合,存储商品类型,存储数据类型FruitItem类型
					ArrayList<FruitItem> array = new ArrayList<FruitItem>();
					//调用商品初始化方法,传递集合
					init(array);
					while(true){
						//调用菜单方法
						mainMenu();			
					}
				}	
				/*
				 * 定义方法,实现主菜单
				 * 提示用户哪些选择 让选择序号
				 * 返回值: 无
				 * 参数: 无
				 */
				public static void mainMenu(){
					System.out.println();
					System.out.println("============欢迎光临ItCast超市============");
					System.out.println("1: 货物 清单   2: 添加货物   3: 删除货物   4: 修改货物  5: 退出");
					System.out.println("请您输入要操作的功能序号");
				}
				
				/*
				 * 定义方法,实现商品数据的初始化
				 * 先将一部分数据,存储集合中
				 * 返回值: 无
				 * 参数 : 集合
				 * 方法名: init
				 */
				public static void init(ArrayList<FruitItem> array){
					//创建出多个FruitItem类型,并且属性赋值
					FruitItem f1 = new FruitItem();
					f1.ID = 9527;
					f1.name = "少林寺酥饼核桃";
					f1.price = 12.7;
					
					FruitItem f2 = new FruitItem();
					f2.ID = 9008;
					f2.name = "尚康杂粮牡丹饼";
					f2.price = 5.6;
					
					FruitItem f3 = new FruitItem();
					f3.ID = 9879;
					f3.name = "新疆原产哈密瓜";
					f3.price = 599.6;
					
					//创建的3个FruitItem类型变量,存储到集合中
					array.add(f1);
					array.add(f2);
					array.add(f3);
				}
				
			}				
				
### 15用户选择功能
	* A: 用户选择功能
		* a: 案例代码
			import java.util.ArrayList;
			import java.util.Scanner;

			/*
			 *   超市管理系统主
			 *   实现:
			 *     1. 商品数据的初始化
			 *     2. 用户的菜单选择
			 *     3. 根据选择执行不同的功能
			 *       3.1 Read    查看商品
			 *       3.2 Create  添加商品
			 *       3.3 Delete  删除商品
			 *       3.4 Update  修改商品
			 *       
			 *       
			 *   所有功能 ,必须定义方法实现
			 *   主方法main  调用作用
			 */
			public class Shopp {

				public static void main(String[] args) {
					//创建ArrayList集合,存储商品类型,存储数据类型FruitItem类型
					ArrayList<FruitItem> array = new ArrayList<FruitItem>();
					//调用商品初始化方法,传递集合
					init(array);
					while(true){
						//调用菜单方法
						mainMenu();
						//调用用户选择序号方法
						int choose = chooseFunction();
						switch (choose) {
						case 1:
							//调用1: 货物 清单
							showFruitList(array);
						break;
						
						case 2:
							//2: 添加货物
							addFruit(array);
						break;
						
						case 3:
							//3: 删除货物
							deleteFruit(array);
						break;
						
						case 4:
							//4: 修改货物
							updateFruit(array);
						break;
						
						case 5:
							return ;

						default:
							System.out.println("输入的序号没有");
							break;
						}
					}
				}	
				/*
				 *  定义方法,实现接受用户的键盘输入
				 *  返回编号
				 */
				public static int chooseFunction(){
					Scanner sc = new Scanner(System.in);
					return sc.nextInt();
				}
				
				/*
				 * 定义方法,实现主菜单
				 * 提示用户哪些选择 让选择序号
				 * 返回值: 无
				 * 参数: 无
				 */
				public static void mainMenu(){
					System.out.println();
					System.out.println("============欢迎光临ItCast超市============");
					System.out.println("1: 货物 清单   2: 添加货物   3: 删除货物   4: 修改货物  5: 退出");
					System.out.println("请您输入要操作的功能序号");
				}
				
				/*
				 * 定义方法,实现商品数据的初始化
				 * 先将一部分数据,存储集合中
				 * 返回值: 无
				 * 参数 : 集合
				 * 方法名: init
				 */
				public static void init(ArrayList<FruitItem> array){
					//创建出多个FruitItem类型,并且属性赋值
					FruitItem f1 = new FruitItem();
					f1.ID = 9527;
					f1.name = "少林寺酥饼核桃";
					f1.price = 12.7;
					
					FruitItem f2 = new FruitItem();
					f2.ID = 9008;
					f2.name = "尚康杂粮牡丹饼";
					f2.price = 5.6;
					
					FruitItem f3 = new FruitItem();
					f3.ID = 9879;
					f3.name = "新疆原产哈密瓜";
					f3.price = 599.6;
					
					//创建的3个FruitItem类型变量,存储到集合中
					array.add(f1);
					array.add(f2);
					array.add(f3);
				}
				
			}

### 16商品的清单功能
	* A: 商品的清单功能
		* a: 案例代码(显示商品清单的showFruitList(ArrayList<FruitItem>)方法的代码如下)
			/*
			 *  定义方法,实现显示货物清单功能
			 *  返回值: 无
			 *  参数: 集合
			 *  遍历集合,获取集合中的每个FruitItem变量,变量,调用属性
			 */
			public static void showFruitList(ArrayList<FruitItem> array){
				System.out.println();
				System.out.println("================商品库存清单================");
				System.out.println("商品编号         商品名称                商品单价");
				//遍历集合
				for(int i = 0 ; i < array.size(); i++){
					//集合get方法,获取出每个FruitItem变量,可以使用FruitItem接受get结果
					FruitItem item = array.get(i);
					//变量item调用类中属性
					System.out.println(item.ID+"   "+item.name+"        "+item.price);
				}
			}
### 17商品的添加功能
	* A: 商品的添加功能
		* a: 案例代码(商品添加功能的addFruit(ArrayList<FruitItem>)方法的代码如下)
			/*
			 * 定义方法,实现商品的添加功能
			 * 返回值:无
			 * 参数: 集合
			 * 提示用户选择的是添加商品的功能
			 * 
			 * 提示用户输入的是什么
			 * 
			 * 创建FruitItem变量,变量调用的属性
			 * 将输入的每个商品属性进行赋值
			 */
			public static void addFruit(ArrayList<FruitItem> array){
				System.out.println("选择的是添加商品功能");
				//创建Scanner变量
				Scanner sc = new Scanner(System.in);
				System.out.print("请输入新商品的编号:");
				//输入商品的编号
				int ID = sc.nextInt();
				//输入商品的名字
				System.out.print("请输入新商品的名字:");
				String name = sc.next();
				//输入商品的单价
				System.out.print("请输入新商品的单价:");
				double price = sc.nextDouble();
				//创建FruitItem变量
				FruitItem item = new FruitItem();
				//item.属性赋值
				item.ID = ID;
				item.name = name;
				item.price = price;
				array.add(item);
				System.out.println("商品添加成功");
			}
### 18商品的删除功能
	* A: 商品的删除功能(删除商品deleteFruit(ArrayList<FruitItem>)方法的代码如下)
		* a: 案例代码
			/*
			 *  定义方法,实现商品的删除功能
			 *  返回值:　无
			 *  参数：　集合
			 *  
			 *  删除依靠的是商品的编号
			 *  提示用户选择的是删除功能
			 *  键盘输入商品的编号
			 *  遍历集合，获取集合中的每个FruitItem变量
			 *  变量调用属性　ID， 和用户的输入的编号,对比,相同就删除
			 */
			public static void deleteFruit(ArrayList<FruitItem> array){
				System.out.println("选择的是删除功能");
				System.out.print("请输入商品的编号:");
				Scanner sc = new Scanner(System.in);
				
				int ID = sc.nextInt();
				//遍历集合
				for(int i = 0 ; i < array.size(); i++){
					//获取到每个FruitItem变量
					FruitItem item = array.get(i);
					//变量,调用属性ID,和用户输入的编号比较
					if( item.ID == ID){
						//移除集合中的元素
						//集合的方法remove实现
						array.remove(i);
						System.out.println("删除成功");
						return;
					}
				}
				System.out.println("你输入的编号不存在");
			}
### 19商品的修改功能
	* A: 商品的修改功能
		* a: 案例代码(修改商品updateFruit(ArrayList<FruitItem>)方法的代码如下)
			/*
			 *  定义方法,实现商品的修改功能
			 *  返回值:　无
			 *  参数：　集合
			 *  
			 *  提示用户选择的是修改功能
			 *  提示用户输入需要修改的商品编号
			 *  遍历集合,获取每个FruitItem变量
			 *  变量调用ID属性,属性和用户输入的编号比较
			 *  如果相同:
			 *    修改调FruitItem中的属性值
			 *    键盘输入
			 */
			public static void updateFruit(ArrayList<FruitItem> array){
				System.out.println("选择的是修改功能");
				System.out.print("请输入您要修改的商品的编号:");
				
				Scanner sc = new Scanner(System.in);
				int ID = sc.nextInt();
				//遍历集合,获取每个FruitItem变量
				for(int i = 0 ; i < array.size(); i++){
					FruitItem item = array.get(i);
					//获取FruitItem的属性ID,和用户输入的ID比较
					if(item.ID == ID){
						System.out.print("输入新的商品编号:");
						item.ID = sc.nextInt();
						
						System.out.print("输入新的商品名字:");
						item.name = sc.next();
						
						System.out.print("输入新的商品价格:");
						item.price = sc.nextDouble();
						System.out.println("商品修改成功");
						return ;
					}
				}
				System.out.println("输入的编号不存在");
			}


## 面向对象

### 01面向对象和面向过程的思想
	* A: 面向过程与面向对象都是我们编程中，编写程序的一种思维方式
		* a: 面向过程的程序设计方式，是遇到一件事时，思考“我该怎么做”，然后一步步实现的过程。
		* b: 面向对象的程序设计方式，是遇到一件事时，思考“我该让谁来做”，然后那个“谁”就是对象，他要怎么做这件事是他自己的事，反正最后一群对象合力能把事就好就行了。
	
### 02面向对象的思想的生活案例
	* A: 买电脑（组装机）
		* a: 面向过程：自己该怎么做
		* b: 面向对象：找人帮我们做
			
			
### 03面向对象好处
	* A: 面向对象好处
		* a: 面向对象思维方式是一种更符合人们思考习惯的思想
		* b: 面向过程思维方式中更多的体现的是执行者（自己做事情），面向对象中更多的体现是指挥者（指挥对象做事情）。
		* c: 面向对象思维方式将复杂的问题简单化。


### 04大象装进冰箱的代码案例
	* A: 需求：把大象装冰箱里
		* a: 面向过程 		
			* 自己打开冰箱门
			* 自己将大象装进去
			* 自己关闭冰箱门	
		* b: 面向对象
			* 分析发现打开、装、关闭都是冰箱的功能。即冰箱对象具	备如下功能
			* 冰箱打开
			* 冰箱存储
			* 冰箱关闭

	* B: 通过伪代码描述大象和冰箱
		* 描述大象：
			class 大象
			{
			}
		* 描述冰箱
			class冰箱
			{
				void 打开(){}
				void 存储(大象){}
				void 关闭(){}
			}

			
	* C: 使用对象：
		* 1、创建冰箱的对象
			* 冰箱 bx = new 冰箱();  
		* 2、调用冰箱的功能
			* 对象.功能()；
			* bx.打开();
			* bx.存储(new 大象());
			* bx.关闭();
	* D：总结：
		* 1、先按照名词提炼问题领域中的对象
		* 2、对对象进行描述，其实就是在明确对象中应该具备的属性和功能
		* 3、通过new的方式就可以创建该事物的具体对象
		* 4、通过该对象调用它以后的功能。



### 05定义小汽车类
	* A: 分析小汽车的属性和功能
		* 属性
			* 颜色
			* 轮胎个数
		* 功能
			* 运行	
	* B: 通过伪代码描述小汽车
		* 小汽车{
			* 颜色
			* 轮胎个数
			* 运行(){}
		* }
	* C：通过JAVA代码描述小汽车
		* public class Car {
			* String color;
			* int number;
		
			* void run() {
				* System.out.println(color + ":" + number);
			* }
		* }





### 01测试汽车类
	* A: 创见对象的格式
		* a: 类名 变量名 = new 类名();
	* B: 测试汽车类
		public class CarDemo {
			public static void main(String[] args) { 
				/*
				 测试：Car类中的run方法。
				 */
				// 1,创建Car的对象。给对象起个名字。
				Car c = new Car();// c是类类型的变量。c指向了一个具体的Car类型的对象。
				// 2,通过已有的对象调用该对象的功能。格式：对象.对象成员;
				// 3,可以该对象的属性赋值。
				c.color = "red";
				c.number = 4;
				c.run();
			}
		}
 


### 02对象的内存图
	* 见课后资料：对象的内存图.JPG


### 03类和对象的关系
	* A: 类和对象的关系
		* 类是对某一类事物的抽象描述，而对象用于表示现实中该类事物的个体
	* B: 举例
		* 可以将玩具模型看作是一个类，将一个个玩具看作对象，从玩具模型和玩具之间的关系便可以看出类与对象之间的关系


### 04成员变量和局部变量的区别
    * 区别一：定义的位置不同
        * 定义在类中的变量是成员变量
        * 定义在方法中或者{}语句里面的变量是局部变量
    * 区别二：在内存中的位置不同
        * 成员变量存储在对内存的对象中
        * 局部变量存储在栈内存的方法中
    * 区别三：声明周期不同
        * 成员变量随着对象的出现而出现在堆中，随着对象的消失而从堆中消失
        * 局部变量随着方法的运行而出现在栈中，随着方法的弹栈而消失
    * 区别四：初始化不同
        * 成员变量因为在堆内存中，所有默认的初始化值
        * 局部变量没有默认的初始化值，必须手动的给其赋值才可以使用。





### 01方法参数是基本数据类型和引用数据类型
	* A.基本类型
		class Demo
		{
			public static void main(String[] args)
			{
				int x = 4;
				show(x);
				System.out.println("x="+x);
			}
			public static void show(int x)
			{
				x = 5;
				
			}
		}	 
		基本类型作为参数传递时，其实就是将基本类型变量x空间中的值复制了一份传递给调用的方法show()，当在show()方法中x接受到了复制的值，再在show()方法中对x变量进行操作，这时只会影响到show中的x。当show方法执行完成，弹栈后，程序又回到main方法执行，main方法中的x值还是原来的值。
	* B.引用类型
		class Demo 
		{
			int x ;
			public static void main(String[] args) 
			{
		
				Demo d = new Demo();
				d.x = 5;
				show(d);
				System.out.println("x="+d.x);
			}
			public static void show(Demo d)
			{
				d.x = 6;
			}
		}	 
		当引用变量作为参数传递时，这时其实是将引用变量空间中的内存地址(引用)复制了一份传递给了show方法的d引用变量。这时会有两个引用同时指向堆中的同一个对象。当执行show方法中的d.x=6时，会根据d所持有的引用找到堆中的对象，并将其x属性的值改为6.show方法弹栈。
		由于是两个引用指向同一个对象，不管是哪一个引用改变了引用的所指向的对象的中的值，其他引用再次使用都是改变后的值。
	* C.结论
		* 对于基本类型形式参数改变不会影响到实际参数
		* 对于引用类型形式参数改变会影响到实际参数 

### 02封装的概述
	* A.面向对象三大特征
		* 封装、继承、多态
	* B.封装表现
		* 1、方法就是一个最基本封装体
		* 2、类其实也是一个封装体	
	* C.封装的好处
		* 1、提高了代码的复用性
		* 2、隐藏了实现细节，还要对外提供可以访问的方式。便于调用者的使用。这是核心之一，也可以理解为就是封装的概念
		* 3、提高了安全性	 
### 03封装的生活中的举例
	* A.封装的生活中的举例
		机箱：
		一台电脑，它是由CPU、主板、显卡、内存、硬盘、电源等部件组长，其实我们将这些部件组装在一起就可以使用电脑了，但是发现这些部件都散落在外面，很容造成不安全因素，于是，使用机箱壳子，把这些部件都装在里面，并在机箱壳上留下一些插口等，若不留插口，大家想想会是什么情况。
		总结：机箱其实就是隐藏了办卡设备的细节，对外提供了插口以及开关等访问内部细节的方式。
	* B.总结
		* 机箱其实就是隐藏了办卡设备的细节，对外提供了插口以及开关等访问内部细节的方式

### 04private关键字
	* A.private概述
		* private可以修饰成员内容包括成员方法和成员变量
		* 被private修饰的内容不能在其他类访问
	* B.使用步骤
		* 1、通过private修饰属性
	* C.完整代码 
		class Person {
			private int age;
			private String name;
		
			public void show() {
				System.out.println("age=" + age + ",name" + name);
			}
		}






### 01get和set方法
	* A.get和set方法
		* 年龄已被私有，错误的值无法赋值，可是正确的值也赋值不了，这样还是不行，那肿么办呢？按照之前所学习的封装的原理，隐藏后，还需要提供访问方式。只要对外提供可以访问的方法，让其他程序访问这些方法。同时在方法中可以对数据进行验证。
        一般对成员属性的访问动作：赋值(设置 set)，取值(获取 get)，因此对私有的变量访问的方式可以提供对应的 setXxx或者getXxx的方法。
		class Person {
			// 私有成员变量
			private int age;
			private String name;
		
			// 对外提供设置成员变量的方法
			public void setAge(int a) {
				// 由于是设置成员变量的值，这里可以加入数据的验证
				if (a < 0 || a > 130) {
					System.out.println(a + "不符合年龄的数据范围");
					return;
				}
				age = a; 
			}
		
			// 对外提供访问成员变量的方法
			public void getAge() {
				return age;
			}
		}
		* 总结
		   * 类中不需要对外提供的内容都私有化，包括属性和方法。
            * 以后再描述事物，属性都私有化，并提供setXxx getXxx方法对其进行访问
		* 注意
			* 私有仅仅是封装的体现形式而已
### 02私有化Person类带get,set
	* 标准代码
		package cn.itcast.demo05;
		
		/*
		 *   类描述人:
		 *     属性: 姓名和年龄
		 *     方法: 说话
		 *   
		 *   私有化所有的属性 (成员变量) ,必须写对应的get/set方法
		 *   凡是自定义的类,自定义成员变量,应该私有化,提供get/set
		 *   
		 *   this关键字:
		 *     区分成员变量和局部变量同名情况
		 *     方法中,方位成员变量,写this.
		 */
		public class Person {
			private String name;
			private int age;
		
			// set方法,变量name,age赋值
			public void setAge(int age) {
				this.age = age;
			}
		
			public void setName(String name) {
				this.name = name;
			}
		
			// get方法,变量name,age获取值
			public int getAge() {
				return age;
			}
		
			public String getName() {
				return name;
			}
		
			public void speak() {
				String  name = "哈哈";
				int age = 16;
				
				System.out.println("人在说话  " + this.name + "..." + this.age);
			}
		}
	* 标准测试代码
		package cn.itcast.demo05;
		
		public class PersonTest {
			public static void main(String[] args) {
				Person p = new Person();
				//调用set方法,对成员变量赋值
				p.setAge(18);
				p.setName("旺财");
				p.speak();
				
				
				//调用get方法,获取成员变量的值
		//		System.out.println(p.getName());
		//		System.out.println(p.getAge());
			}
		}


### 03this关键字_区分成员变量和局部变量的同名
	* A.什么时候用
		* 当类中存在成员变量和局部变量同名的时候为了区分，就需要使用this关键字
	* B.代码
		class Person {
			private int age;
			private String name;
			
			public void speak() {
				this.name = "小强";
				this.age = 18;
				System.out.println("name=" + this.name + ",age=" + this.age);
			}
		}
		
		class PersonDemo {
			public static void main(String[] args) {
				Person p = new Person();
				p.speak();
			}
		}

### 04this内存图
	* A.this内存图
		* 见附件：this内存图.jpg



### 01this的年龄比较
	* A.需求：在Person类中定义功能，判断两个人是否是同龄人
	* B.代码
		class Person {
			private int age;
			private String name;
			
			public int getAge() {
				return age;
			}
		
			public void setAge(int age) {
				this.age = age;
			}
		
			public String getName() {
				return name;
			}
		
			public void setName(String name) {
				this.name = name;
			}
		
			public void speak() {
				System.out.println("name=" + this.name + ",age=" + this.age);
			}
		
			// 判断是否为同龄人
			public boolean equalsAge(Person p) {
				// 使用当前调用该equalsAge方法对象的age和传递进来p的age进行比较
				// 由于无法确定具体是哪一个对象调用equalsAge方法，这里就可以使用this来代替
				/*
				 * if(this.age == p.age) { return true; } return false;
				 */
				return this.age == p.age;
			}
		}

### 02随机点名器案例重构
	* A.需求：随机点名器，即在全班同学中随机的找出一名同学，打印这名同学的个人信息
		它具备以下3个内容：
		存储所有同学姓名
		总览全班同学姓名
		随机点名其中一人，打印到控制台
	* B.代码
		import java.util.ArrayList;
		import java.util.Random;
		import java.util.Scanner;
		
		/**
		 * 思路：
		 * 第一步：存储全班同学信息
		 * 第二步：打印全班同学每一个人的信息
		 * 第三部：随机对学生点名，打印学生信息
		 */
		public class Test {
			public static void main(String[] args) {
				ArrayList<Student> list = new ArrayList<Student>(); //1.1创建一个可以存储多个同学名字的容器
				 //1.存储全班同学信息
				addStudent(list);
				 //2.打印全班同学每一个人的信息（姓名、年龄）
				printStudent(list);
				 //3.随机对学生点名，打印学生信息
				randomStudent(list);
			}
			public static void addStudent(ArrayList<Student> list) {
				//键盘输入多个同学名字存储到容器中
				Scanner sc = new Scanner(System.in);
				for (int i = 0; i < 3; i++) {
					//创建学生
					Student s = new Student();
					System.out.println("存储第"+i+"个学生姓名：");
					String name = sc.next();
					s.setName(name);
					System.out.println("存储第"+i+"个学生年龄：");
					int age = sc.nextInt();
					s.setAge(age);
					//添加学生到集合
					list.add(s);
				}
			}
			/**
			 2.打印全班同学每一个人的信息（姓名、年龄）
			 */
			public static void printStudent (ArrayList<Student> list) {
				for (int i = 0; i < list.size(); i++) {
					Student s = list.get(i);
					System.out.println("姓名："+s.getName() +",年龄："+s.getAge());
				}
			}
			/**
			 3.随机对学生点名，打印学生信息
			 */
			public static void randomStudent (ArrayList<Student> list) {
				//在班级总人数范围内，随机产生一个随机数
				int index = new Random().nextInt(list.size());
				//在容器（ArrayList集合）中，查找该随机数所对应的同学信息（姓名、年龄）
				Student s = list.get(index);
				System.out.println("被随机点名的同学："+s.getName() + "，年龄:" + s.getAge());
			}
		}

		/**
		 * 学生信息类
		 */
		public class Student {
			private String name; // 姓名
			private int age; // 年龄
		
			public String getName() {
				return name;
			}
		
			public void setName(String name) {
				this.name = name;
			}
		
			public int getAge() {
				return age;
			}
		
			public void setAge(int age) {
				this.age = age;
			}
		}	


		

### 03总结

* A.类与对象
	* 类，用于描述多个对象的共同特征，它是对象的模板。
	* 对象，用于描述现实中的个体，它是类的实例。
	* 类的定义：使用关键字class来定义java中的类
	* 格式：
			class 类名 {
				//属性
				数据类型 变量名;
				…
				//方法
				修饰符 返回值类型 方法名(参数){   }
				…
			}
			
* B.创建对象：
	* 格式：
	* 类名 对象名 = new 类名();

* C.封装（private关键字）
	* 封装，把对象的属性与方法的实现细节隐藏，仅对外提供一些公共的访问方式
	* 封装的体现：
	* 变量:使用 private 修饰，这就是变量的封装
	* 方法:也是一种封装，封装了多条代码
	* 类： 也是一种封装，封装了多个方法
* D.private关键字，私有的意思
	* 它可以用来修饰类中的成员(成员变量，成员方法)
	* private的特点：
	* private修饰的成员只能在当前类中访问，其他类中无法直接访问
* E.this关键字
	* this关键字，本类对象的引用
	* this是在方法中使用的，哪个对象调用了该方法，那么，this就代表调用该方法的对象引用
	* this什么时候存在的？当创建对象的时候，this存在的
	* this的作用：用来区别同名的成员变量与局部变量（this.成员变量）
	* public void setName(String name) {
	* 	this.name = name;
	* }


## 继承
### 01继承的概述
	 *A:继承的概念
	    *a:继承描述的是事物之间的所属关系，通过继承可以使多种事物之间形成一种关系体系
        *b:在Java中，类的继承是指在一个现有类的基础上去构建一个新的类，
            构建出来的新类被称作子类，现有类被称作父类
      *B:继承关系的子类特点  
        *a:子类会自动拥有父类所有非private修饰的属性和方法
	
### 02继承的定义格式和使用
	 * A:继承的格式
	    class 子类 extends 父类 {}
	 * B:雇员(Employee)与研发部员工(Developer)案例:
	     * cn.itcast.demo01包下:
	     * Employee.java:
			 /*
			 * 定义员工类Employee
			 */
			class Employee {
				String name; // 定义name属性
				
				public void work() {// 定义员工的工作方法
					System.out.println("尽心尽力地工作");
				}
			}
        *Developer.java:
		    /*
			 * 定义研发部员工类Developer 继承 员工类Employee
			 * 继承了父类中所有非private修饰的成员变量
			 */
			class Developer extends Employee {
				// 定义一个打印name的方法
				public void printName() {
					System.out.println("name=" + name);
				}
			}
        *测试员工类与研发部员工类:
            /*
 		     * 定义测试类
             */
			public class Example01 {
				public static void main(String[] args) {
					Developer d = new Developer(); // 创建一个研发部员工类对象
					d.name = "小明"; // 为该员工类的name属性进行赋值
					d.printName(); // 调用该员工的printName()方法
					d.work(); // 调用Developer类继承来的work()方法
				}
			}
        *通过子类对象既可以调用自身的非private修饰的成员,也可以调用父类的非private修饰的成员

### 03继承的好处
    *A:继承的好处：
        *1、继承的出现提高了代码的复用性，提高软件开发效率。
        *2、继承的出现让类与类之间产生了关系，提供了多态的前提。

### 04继承的注意事项 
	 *A:继承的注意事项 
		 *a:在Java中，类只支持单继承，不允许多继承，也就是说一个类只能有一个直接父类，例如下面这种情况是不合法的。
		     class A{} 
		     class B{}
		     class C extends A,B{}  // C类不可以同时继承A类和B类
		  假如支持多继承例如:
             class A{
             	int a=3;
                public void method(){

                }
             } 
		     class B{
		     	int a=5;
		     	public void method(){

		     	}
		     }
		     class C extends A,B{
                
		     } 
		     class Demo{
		     	public static void main(String[] args){
		     		C c=new C();
		     		System.out.println(c.a);//到底是调用A的还是B的成员变量??无法确定
		     		c.method();//到底是调用A的还是B的成员方法??无法确定
		     	}	
		     }
	   
	      *b:多个类可以继承一个父类，例如下面这种情况是允许的(就像你爹可以多个儿子,但是这些儿子都只有一个爹)
		     class A{}
		     class B extends A{}
		     class C extends A{}   // 类B和类C都可以继承类A
		 
	     *c:在Java中，多层继承是可以的，
	        即一个类的父类可以再去继承另外的父类，
	        例如C类继承自B类，而B类又可以去继承A类，这时，C类也可称作A类的子类。下面这种情况是允许的。
		     class A{}
		     class B extends A{}   // 类B继承类A，类B是类A的子类
		     class C extends B{}   // 类C继承类B，类C是类B的子类，同时也是类A的子类
	     
          *d:在Java中，子类和父类是一种相对概念，
            也就是说一个类是某个类父类的同时，也可以是另一个类的子类。
            例如上面的这种情况中，B类是A类的子类，同时又是C类的父类。



### 05继承的体系.avi 11:00
   *A:继承的体系:

						                  动物(吃)
						                    |
						           -------------------------
						           |                        |
						        猫科动物(吃,胎生)      爬行动物(吃,卵生)
						           |                            |
				 -------------------------------        -----------------      
			     |          			       |        |                |
				猫(吃,抓老鼠,胎生)   虎(吃,领地,胎生)  蛇(吃,冬眠,卵生)  鳄鱼(吃,潜水,卵生)
	    
	    
	    *a:动物体系是对每个具体事物共性的抽取,子类的共性抽取形成父类
	    *b:父类:具有所有子类的共性内容
	       子类:不但有共性还有自身特有的内容
	    *c:整个继承体系,越向上越抽象,越向下越具体




### 06继承后子类父类成员变量的特点 
	 A:继承后子类父类成员变量的特点
	   a:子类的对象调用成员变量的时候,子类自己有,使用子类,子类自己没有调用的父类
		   class Fu{
				//Fu中的成员变量。
				int num = 5;
			}
			
			class Zi extends Fu{
				//Zi中的成员变量
				int num2 = 6;
				//Zi中的成员方法
				public void show()
				{
					//访问父类中的num
					System.out.println("Fu num="+num);
					//访问子类中的num2
					System.out.println("Zi num2="+num2);
				}
			}
			
			class Demo{
				public static void main(String[] args) 
				{
					Zi z = new Zi(); //创建子类对象
					z.show(); //调用子类中的show方法
				}
			}
     b:当子父类中出现了同名成员变量
 		class Fu{
			//Fu中的成员变量。
			int num = 5;
		}
		
		class Zi extends Fu{
			//Zi中的成员变量
			int num = 6;
			void show(){   
				//子类的局部变量
				int num=7
				
				//直接访问,遵循就近查找原则
                System.out.println(num);//7
				
				//子父类中出现了同名的成员变量时
				//在子类中需要访问父类中非私有成员变量时，需要使用super关键字
				//访问父类中的num
				System.out.println("Fu num="+super.num);//5
				

				//访问子类中的num2
				System.out.println("Zi num2="+this.num);//6
			}
		}
		
		class Demo5 {
			public static void main(String[] args) 
			{
				Zi z = new Zi(); //创建子类对象
				z.show(); //调用子类中的show方法
			}
		}


### 07继承后子类父类成员方法的特性_子类重写父类方法 
	A:继承后子类父类成员方法的特性
	  a:子类的对象调用方法的时候,子类自己有,使用子类,子类自己没有调用的父类
	    class Fu{
			public void show(){
				System.out.println("Fu类中的show方法执行");
			}
		}
		class Zi extends Fu{
			public void show2(){
				System.out.println("Zi类中的show2方法执行");
			}
		}
		public  class Test{
			public static void main(String[] args) {
				Zi z = new Zi();
				z.show(); //子类中没有show方法，但是可以找到父类方法去执行
				z.show2();
			}
		}  
     
     b:为什么要有重写?
         class Fu{
         	public void method(){
         		//上千行代码
                //Fu类中的方法最先存在,那么如果项目需求变了,该方法
                //功能不能够满足我们的需求,此时我们也不会去改这个方法
                //因为项目中可能有大量的功能已经使用到该方法,如果随意修改可能使调用该方法的功能出现问题
                //所以使用重写方式基于原有功能提供更强的功能
         	}   
         }
         class Zi extends Fu{
          
         }
     c:子类中出现与父类一模一样的方法时，会出现覆盖操作，也称为override重写、复写或者覆盖
       class Fu{
			public void show(){
				System.out.println("Fu show");
			}
       }
	   
	   class Zi extends Fu{
			//子类复写了父类的show方法
			public void show(){
				System.out.println("Zi show");
			}
		}
       public  class Test{
			public static void main(String[] args) {
				Zi z = new Zi();
				z.show(); //Zi show 子类有直接使用子类
			}
		}  
       

### 08方法覆盖的需求 
    A:方法覆盖的需求 
	    a:案例:比如手机，当描述一个手机时，它具有发短信，打电话，显示来电号码功能，
	    后期由于手机需要在来电显示功能中增加显示姓名和头像，
	    这时可以重新定义一个类描述智能手机，并继承原有描述手机的类。
	    并在新定义的类中覆盖来电显示功能，在其中增加显示姓名和头像功能

	    b:分析:我们不改装(破坏)原来的手机,而是再买一个新的智能手机,不但有原有的功能,而且还有特有功能
	           例:厂商发布新手机都是基于原有手机的升级,不会拿着原有的手机在卖,新产一款 
          1:分析类的构建:
	           手机类
	            属性(成员变量):无
	            行为(成员方法):
	               发短信
	               打电话
	               来电显示:显示来电号码
	          智能手机类:
	            属性(成员变量):无
	            行为(成员方法):
	              发短信
	              打电话
	              来电显示:显示来电号码,显示姓名和头像
	          
	          手机类和智能手机类有共性内容:
	              发短信
	              打电话
	              显示来电号码
          
          2:继承关系分析:
            对于发短信和打电话功能,让智能手机直接沿用(继承)手机的就可以
            但是在智能手机中的来电显示不但实现号码,还显示姓名和头像,同样的都是来电显示功能,智能手机的来电显示比手机的功能更加强大,我们考虑使用重写
 
### 09方法覆盖的手机案例实现 
		//手机类
		class Phone{
			public void sendMessage(){
				System.out.println("发短信");
			}
			public void call(){
				System.out.println("打电话");
			}
			public void showNum(){
				System.out.println("来电显示号码");
			}
		}

		//智能手机类
		class NewPhone extends Phone{
			//覆盖父类的来电显示号码功能，并增加自己的显示姓名和图片功能
			//从现实生活角度考虑沿用原有的showNum方法名便于用户更快熟悉和接受,而不是再起个新的名字
			//用户还需要花费大量时间慢慢接受
			
			public void showNum(){
				//调用父类已经存在的功能使用super
                //如果不加super这是调用子类自身的showNum(),自己调用自己,递归
                //方法不断入栈导致内存溢出
				super.showNum();
				

				//增加自己特有显示姓名和图片功能
				System.out.println("显示来电姓名");
				System.out.println("显示头像");
			}
		}

		public class Test {
			public static void main(String[] args) {
				new NewPhone().showNum();//来电显示  显示来电姓名 显示头像
			}
		}
    
### 10方法覆盖的注意事项 
   A:方法覆盖的注意事项 
    a:权限:子类方法覆盖父类方法，必须要保证权限大于等于父类权限。
      四大权限:public>默认=protected>private
	   
	   class Fu{	
			void show(){

			}
			public void method(){

			}
	    }
	    class Zi() extends Fu{
			public void show(){//编译运行没问题

			}  
			void method(){//编译错误

		    }     
	    }
	 b:方法定义:子类方法和要重写的父类的方法:方法的方法名和参数列表都要一样。
	   关于方法的返回值:
	     如果是基本数据类型,子类的方法和重写的父类的方法返回值类型必须相同
	     如果是引用数据类型,子类的方法和重写的父类的方法返回值类型可以相同或者子类方法的返回值类型是父类方法返回值类型的子类
	     class Fu{	
			int show(){

			}
			public Fu method(){

			}
			
			public Fu method2(){

			}
			
	    }
	    class Zi() extends Fu{
			public int show(){//返回值为基本类型的重写

			}  
			public Fu method(){//子类的方法和重写的父类的方法返回值类型可以相同

		    }     
		    public Zi method2(){//子类方法的返回值类型是父类方法返回值类型的子类

		    }     
	    }
     c:重载与重写对比:
        重载:
		    权限修饰符(public private 默认):无关
		    方法名:重载的两个方法的方法名必须相同
		    形参列表:
		      形参类型的顺序不同
		      形参的个数不同
		      形参的类型不同
		      三者至少满足一个
		    返回值类型:
		      重载与返回值类型无关
		重写:
		    权限修饰符(public private 默认): 
		      子类方法的权限>=父类的方法的权限
		    方法名: 
		      子类方法和父类方法必须相同
		    形参列表: 
		       子类方法和父类方法的形参列表必须相同
		    返回值类型:
		      基本类数据类型:
		        必须相同
		      引用数据类型:
		       子类方法的返回值类型和父类方法的返回值类型相同
		       或者
		       子类方法的返回值类型是父类方法的返回值类型的 子类


### 11抽象类的产生 
      A:抽象类的产生
        a:分析事物时，发现了共性内容，就出现向上抽取。会有这样一种特殊情况，就是方法功能声明相同，但方法功能主体不同。那么这时也可以抽取，但只抽取方法声明，不抽取方法主体。那么此方法就是一个抽象方法。
### 12抽象类的定义格式 
	 A:抽象方法定义的格式：
	   a:public abstract 返回值类型 方法名(参数);
	     抽象类定义的格式：
		 abstract class 类名 {
			
		  }
	    b:抽象类示例代码：
		   /*
			 *  定义类开发工程师类
			 *    EE开发工程师 :  工作
			 *    Android开发工程师 : 工作
			 *    
			 *    根据共性进行抽取,然后形成一个父类Develop
			 *    定义方法,工作: 怎么工作,具体干什么呀
			 *    
			 *    抽象类,不能实例化对象, 不能new的
			 *    不能创建对象的原因:  如果真的让你new了, 对象.调用抽象方法,抽象方法没有主体,根本就不能运行
			 *    抽象类使用: 定义类继承抽象类,将抽象方法进行重写,创建子类的对象
			 */
			public abstract class Develop {
			   //定义方法工作方法,但是怎么工作,说不清楚了,讲不明白
				//就不说, 方法没有主体的方法,必须使用关键字abstract修饰
				//抽象的方法,必须存在于抽象的类中,类也必须用abstract修饰
				public abstract void work();
			}




### 13抽象类的使用方式
    A:抽象类的使用方式
	 /*
	 *  定义类,JavaEE的开发人员
	 *  继承抽象类Develop,重写抽象的方法
	 */
	public class JavaEE extends Develop{
		//重写父类的抽象方法
		//去掉abstract修饰符,加上方法主体
		public void work(){
			System.out.println("JavaEE工程师在开发B/S 软件");
		
		}
	}
	/*
	 *  定义Android类,继承开发人员类
	 *  重写抽象方法
	 */
	public class Android extends Develop{
	     public void work(){
	    	 System.out.println("Android工程师开发手机软件");
	     }
	}

	/*
	 *  测试抽象类
	 *    创建他的子类的对象,使用子类的对象调用方法
	 */
	public class Test {
		public static void main(String[] args) {
			 JavaEE ee = new JavaEE();
			 ee.work();//"JavaEE工程师在开发B/S 软件"
			 
			 Android and = new Android();
			 and.work();//"Android工程师开发手机软件"
		}
	}
	        

### 14抽象类特点
  A:抽象类的特点
    a:抽象类和抽象方法都需要被abstract修饰。抽象方法一定要定义在抽象类中。
    b:抽象类不可以直接创建对象，原因：调用抽象方法没有意义。
    c:只有覆盖了抽象类中所有的抽象方法后，其子类才可以创建对象。否则该子类还是一个抽象类。
    之所以继承抽象类，更多的是在思想，是面对共性类型操作会更简单。
      abstract class A{
      	public abstract void func();
      	public abstract void func2();
      }
      class A2 extends A{//A2把A中的两个抽象方法都重写掉了
      	                 //A2类不再是抽象类
      	 public void func(){}
      	 public void func2(){}
      }

      abstract class A3 extends A{//含有抽象方法的类一定是抽象类
      	 public void func(){

      	 }
      	 //public abstract void func2();//func2相当于被继承下来
      }

### 15抽象类的设计思想 4:40
    A:抽象类的设计思想
      a:抽象类的作用:继承的体系抽象类,强制子类重写抽象的方法
        抽象员工:
          规定一个方法,work工作
          EE员工,Android员工 
           
           Develop类 抽象类
           abstract work();
               |
        -------------
       |             |
      EE            Android  //是我开发的一员必须工作
      work(){}       work(){}

### 16抽象类的细节
   * A:抽象类的细节
        * a:抽象类一定是个父类？	
           - 是的，因为不断抽取而来的。
        * b:抽象类中是否可以不定义抽象方法?
           - 是可以的，那这个抽象类的存在到底有什么意义呢？
                不让该类创建对象,方法可以直接让子类去使用
           (适配器设计模式)
           
    /*
      *   抽象类,可以没有抽象方法,可以定义带有方法体的方法
      *   让子类继承后,可以直接使用
      */
             
    public  abstract class Animal {
    public void sleep(){
    System.out.println("动物睡觉");
    }
                
            }
            public class Cat extends Animal{
    
            }     
            
            public class Test {
                public static void main(String[] args) {
                    //Cat c = new Cat();
                    new Cat().sleep();//不让该类创建对象,方法可以直接让子类去使用
                }
            }
     c:抽象关键字abstract不可以和哪些关键字共存？	
 	     1:private：私有的方法子类是无法继承到的，也不存在覆盖，
                 而abstract和private一起使用修饰方法，abstract既要子类去实现这个方法,
                 而private修饰子类根本无法得到父类这个方法。互相矛盾。 
        
        /*
		 *   抽象类,可以没有抽象方法,可以定义带有方法体的方法
		 *   让子类继承后,可以直接使用
		 */
		public  abstract class Animal {
		 
		     // private abstract void show();
		     //抽象方法,需要子类重写, 如果父类方法是私有的,子类继承不了,也就没有了重写
		}
	 

	 
     2:final，暂时不关注，后面学
	 3:static，暂时不关注，后面学



### 17员工案例分析
A:员工案例分析:
  a:需求描述:
		某IT公司有多名员工，按照员工负责的工作不同，进行了部门的划分（研发部员工、维护部员工）。
		  研发部根据所需研发的内容不同，又分为JavaEE工程师、Android工程师；
		  维护部根据所需维护的内容不同，又分为网络维护工程师、硬件维护工程师。

		公司的每名员工都有他们自己的员工编号、姓名，并要做它们所负责的工作。
			工作内容
			JavaEE工程师：员工号为xxx的 xxx员工，正在研发淘宝网站
			Android工程师：员工号为xxx的 xxx员工，正在研发淘宝手机客户端软件
			网络维护工程师：员工号为xxx的 xxx员工，正在检查网络是否畅通
			硬件维护工程师：员工号为xxx的 xxx员工，正在修复打印机
  b:继承体系:
                        员工
                         |
       --------------------------------------------
       |                                          |
     研发部员工                                 维护部员工
       |                                          |
   -------------                              -----------
   |            |                             |         |
JavaEE工程师   Android工程师         网络维护工程师    硬件维护工程师
 
  c:详细描述:
	根据员工信息的描述，确定每个员工都有员工编号、姓名、要进行工作。
     则，把这些共同的属性与功能抽取到父类中（员工类），
     关于工作的内容由具体的工程师来进行指定。
	工作内容
		JavaEE工程师：员工号为xxx的 xxx员工，正在研发淘宝网站
		Android工程师：员工号为xxx的 xxx员工，正在研发淘宝手机客户端软件
		网络维护工程师：员工号为xxx的 xxx员工，正在检查网络是否畅通
		硬件维护工程师：员工号为xxx的 xxx员工，正在修复打印机
	创建JavaEE工程师对象，完成工作方法的调用


### 18员工案例Employee类的编写
   A:员工案例Employee类的编写:按照分析的继承体系来逐个实现
		 /*
		 *  定义员工类
		 *    内容,都是所有子类的共性抽取
		 *      属性: 姓名,工号
		 *      方法: 工作
		 */
	   public abstract class Employee {
			private String id;// 员工编号
			private String name; // 员工姓名

			public String getId() {
				return id;
			}
			public void setId(String id) {
				this.id = id;
			}
			public String getName() {
				return name;
			}
			public void setName(String name) {
				this.name = name;
			}
			
			//工作方法（抽象方法）
			public abstract void work(); 
	 }


### 19员工案例的子类的编写
   B:员工案例的子类的编写:
     /*
	 *  定义研发员工类
	 *    属于员工中的一种, 继承员工类 
	 *    抽象类Develop 给自己的员工定义自己有的属性
	 */
	public abstract class Develop extends Employee{

	}

	/*
	 *  描述JavaEE开发工程师类
	 *    工号,姓名 工作方法
	 *  其他的员工,也具备这些共性,抽取到父类中,自己就不需要定义了
	 *  是研发部员工的一种,继承研发部类
	 */
	public class JavaEE extends Develop{
		//重写他父类的父类的抽象方法
		public void work(){
			//调用父类的get方法,获取name,id值
			System.out.println("JavaEE的工程师开发淘宝"+ super.getName()+".."+super.getId());
		}
	}
	/*
	*定义Android工程师 继承 研发部员工类，重写工作方法
	*/
    public class Android extends Developer {
	  @Override
	   public void work() {
		System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在研发淘宝手机客户端软件");
	  }
    }
  

    /*
	 *   定义维护员工类,属于员工中的一种
	 *   继承员工类
	 *   抽象类Maintainer 给自己的员工定义自己有的属性
	 */
	public abstract class Maintainer extends Employee{

	}
    
    /*
	 *  描述的是网络维护工程师
	 *  属于维护部的员工,继承维护部类
	 */
	public class Network extends Maintainer{
		public void work(){
			System.out.println("网络工程师在检查网络是否畅通"+super.getName()+"..."+super.getId());
		}
	}
	
    /*
     *定义Hardware硬件维护工程师 继承 维护部员工类，重写工作方法
     */
	public class Hardware extends Maintainer {
		@Override
		public void work() {
			System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在修复打印机");
		}
	}

### 20总结
* 把今天的知识点总结一遍。
 
	 


## 接口
### 01接口的概念
	* A:接口的概念
	    接口是功能的集合，同样可看做是一种数据类型，是比抽象类更为抽象的”类”。
		接口只描述所应该具备的方法，并没有具体实现，具体的实现由接口的实现类(相当于接口的子类)来完成。这样将功能的定义与实现分离，优化了程序设计。
		请记住：一切事物均有功能，即一切事物均有接口。


	
### 02接口的定义
	* A: 接口的定义
			与定义类的class不同，接口定义时需要使用interface关键字。
			定义接口所在的仍为.java文件，虽然声明时使用的为interface关键字的编译后仍然会产生.class文件。这点可以让我们将接口看做是一种只包含了功能声明的特殊类。

								
	* B : 定义格式
			public interface 接口名 {
				抽象方法1;
				抽象方法2;
				抽象方法3;
			}
	* C: 定义步骤
			使用interface代替了原来的class，其他步骤与定义类相同：
			接口中的方法均为公共访问的抽象方法
			接口中无法定义普通的成员变量


	
			
### 03接口的实现类
	* A: 类与接口的关系
			类与接口的关系为实现关系，即类实现接口。实现的动作类似继承，只是关键字不同，实现使用implements。
			其他类(实现类)实现接口后，就相当于声明：”我应该具备这个接口中的功能”。实现类仍然需要重写方法以实现具体的功能。
	* B: 类实现接口的格式
			class 类 implements 接口 {
				重写接口中方法
			} 
	* C:注意事项
	 		在类实现接口后，该类就会将接口中的抽象方法继承过来，此时该类需要重写该抽象方法，完成具体的逻辑。
			接口中定义功能，当需要具有该功能时，可以让类实现该接口，只声明了应该具备该方法，是功能的声明。
			在具体实现类中重写方法，实现功能，是方法的具体实现。




### 04接口中成员变量的特点
	* A:成员变量特点
		 * a 接口中可以定义变量，但是变量必须有固定的修饰符修饰，public static final 所以接口中的变量也称之为常量，其值不能改变。后面我们会讲解static与final关键字
			

	* B:案例
			interface Demo { ///定义一个名称为Demo的接口。
				public static final int NUM = 3;// NUM的值不能改变
			}
			
		
### 05接口中成员方法的特点
	* A: 成员方法特点
		* a 接口中可以定义方法，方法也有固定的修饰符，public abstract
		* b 子类必须覆盖掉接口中所有的抽象方法后，子类才可以实例化。否则子类是一个抽象类。

	* B: 案例
			interface Demo { ///定义一个名称为Demo的接口。
				public abstract void show1();
				public abstract void show2();
			}
			
			//定义子类去覆盖接口中的方法。类与接口之间的关系是 实现。通过 关键字 implements
			class DemoImpl implements Demo { //子类实现Demo接口。
				//重写接口中的方法。
				public void show1(){}
				public void show2(){}
			}

### 06实现类还是一个抽象类
	A: 接口的实现类
	   一个类如果实现类接口,有两种操作方法:
	   第一:实现类是非抽象类,就需要重写接口中所有的抽象方法.
	   第二:实现类也声明为抽象类,那么实现类可以不重写接口中的抽象方法。


		
==============================第二节课开始====================================	

### 07类和接口的多实现	
	* A：接口的多实现
		了解了接口的特点后，那么想想为什么要定义接口，使用抽象类描述也没有问题，接口到底有啥用呢？
		接口最重要的体现：解决多继承的弊端。将多继承这种机制在java中通过多实现完成了。
		
	* B 多实现的优点
		* 怎么解决多继承的弊端呢？
		* 弊端：多继承时，当多个父类中有相同功能时，子类调用会产生不确定性。
		* 其实核心原因就是在于多继承父类中功能有主体，而导致调用运行时，不确定运行哪个主体内容。
		* 为什么多实现能解决了呢？
		* 因为接口中的功能都没有方法体，由子类来明确。

	* C :案例演示
		interface Fu2{
			void show2();
		}
		class Zi implements Fu1,Fu2 {    // 多实现。同时实现多个接口。
			public void show1(){}
			public void show2(){}
		}
		

 

### 08类在继承类的同时实现多接口
	* A: 继承的同时实现接口
		* 接口和类之间可以通过实现产生关系，同时也学习了类与类之间可以通过继承产生关系。当一个类已经继承了一个父类，它又需要扩展额外的功能，这时接口就派上用场了。
		* 子类通过继承父类扩展功能，通过继承扩展的功能都是子类应该具备的基础功能。如果子类想要继续扩展其他类中的功能呢？这时通过实现接口来完成。
		* 接口的出现避免了单继承的局限性。父类中定义的事物的基本功能。接口中定义的事物的扩展功能。
		
	* B: 代码演示
	    class Fu {
			public void show(){}
		}
		interface Inter {
			pulbic abstract void show1();
		}
		class Zi extends Fu implements Inter {
			public void show1() {
			}
		}

		接口的出现避免了单继承的局限性。父类中定义的事物的基本功能。接口中定义的事物的扩展功能。
		
### 09接口的多继承
	* A: 接口的多继承
		* 学习类的时候，知道类与类之间可以通过继承产生关系，接口和类之间可以通过实现产生关系，那么接口与接口之间会有什么关系。
		* 多个接口之间可以使用extends进行继承。
		
	* B 代码演示
		 interface Fu1{
			void show();
		}
		interface Fu2{
			void show1();
		}
		interface Fu3{
			void show2();
		}
		interface Zi extends Fu1,Fu2,Fu3{
			void show3();
		}
		
		在开发中如果多个接口中存在相同方法，这时若有个类实现了这些接口，那么就要实现接口中的方法，由于接口中的方法是抽象方法，子类实现后也不会发生调用的不确定性。

### 10接口思想
	* A:接口的思想
		* 前面学习了接口的代码体现，现在来学习接口的思想，接下里从生活中的例子进行说明。
		* 举例：我们都知道电脑上留有很多个插口，而这些插口可以插入相应的设备，这些设备为什么能插在上面呢？
		* 主要原因是这些设备在生产的时候符合了这个插口的使用规则，否则将无法插入接口中，更无法使用。发现这个插口的出现让我们使用更多的设备。
	
	* B: 接口的好处	
		* 总结：接口在开发中的它好处
		* 1、接口的出现扩展了功能。
		* 2、接口其实就是暴漏出来的规则。
		* 3、接口的出现降低了耦合性，即设备与设备之间实现了解耦。
		
		* 接口的出现方便后期使用和维护，一方是在使用接口（如电脑），一方在实现接口（插在插口上的设备）。例如：笔记本使用这个规则（接口），电脑外围设备实现这个规则（接口）。

### 11接口和抽象类的区别
	* A: 明白了接口思想和接口的用法后，接口和抽象类的区别是什么呢？接口在生活体现也基本掌握，那在程序中接口是如何体现的呢？
		通过实例进行分析和代码演示抽象类和接口的用法。
	* B: 举例：
		*	犬：
				行为：
				吼叫；
				吃饭；
		* 缉毒犬：
				行为：
				吼叫；
				吃饭；
				缉毒；
	
	* C:思考：
		* 由于犬分为很多种类，他们吼叫和吃饭的方式不一样，在描述的时候不能具体化，也就是吼叫和吃饭的行为不能明确。
		* 当描述行为时，行为的具体动作不能明确，这时，可以将这个行为写为抽象行为，那么这个类也就是抽象类。
		* 可是当缉毒犬有其他额外功能时，而这个功能并不在这个事物的体系中。这时可以让缉毒犬具备犬科自身特点的同时也有其他额外功能，可以将这个额外功能定义接口中。

	* D: 代码演示
		interface 缉毒{
			public abstract void 缉毒();
		}
		//定义犬科的这个提醒的共性功能
		abstract class 犬科{
		public abstract void 吃饭();
		public abstract void 吼叫();
		}
		// 缉毒犬属于犬科一种，让其继承犬科，获取的犬科的特性，
		//由于缉毒犬具有缉毒功能，那么它只要实现缉毒接口即可，这样即保证缉毒犬具备犬科的特性，也拥有了缉毒的功能
		class 缉毒犬 extends 犬科 implements 缉毒{
		
			public void 缉毒() {
			}
			void 吃饭() {
			}
			void 吼叫() {
			}
		}
		class 缉毒猪 implements 缉毒{
			public void 缉毒() {
			}
		}

	* E: 接口和抽象类区别总结
	 	相同点:
			都位于继承的顶端,用于被其他类实现或继承;
			都不能直接实例化对象;
			都包含抽象方法,其子类都必须覆写这些抽象方法;
		区别:
			抽象类为部分方法提供实现,避免子类重复实现这些方法,提高代码重用性;接口只能包含抽象方法;
			一个类只能继承一个直接父类(可能是抽象类),却可以实现多个接口;(接口弥补了Java的单继承)
			抽象类是这个事物中应该具备的你内容, 继承体系是一种 is..a关系
			接口是这个事物中的额外内容,继承体系是一种 like..a关系
		
		二者的选用:
			优先选用接口,尽量少用抽象类;
			需要定义子类的行为,又要为子类提供共性功能时才选用抽象类;
		


		
==============================第三节课开始====================================

### 12多态概述
	* A: 多态概述
		多态是继封装、继承之后，面向对象的第三大特性。
		现实事物经常会体现出多种形态，如学生，学生是人的一种，则一个具体的同学张三既是学生也是人，即出现两种形态。	
		Java作为面向对象的语言，同样可以描述一个事物的多种形态。如Student类继承了Person类，一个Student的对象便既是Student，又是Person。
		Java中多态的代码体现在一个子类对象(实现类对象)既可以给这个子类(实现类对象)引用变量赋值，又可以给这个子类(实现类对象)的父类(接口)变量赋值。
		如Student类可以为Person类的子类。那么一个Student对象既可以赋值给一个Student类型的引用，也可以赋值给一个Person类型的引用。
		最终多态体现为父类引用变量可以指向子类对象。
		多态的前提是必须有子父类关系或者类实现接口关系，否则无法完成多态。
		在使用多态后的父类引用变量调用方法时，会调用子类重写后的方法。


### 13多态调用的三种格式
	* A:多态的定义格式：
		* 就是父类的引用变量指向子类对象
			 父类类型  变量名 = new 子类类型();
			 变量名.方法名();
		
	* B: 普通类多态定义的格式
			父类 变量名 = new 子类();
			举例：	
				class Fu {}
				class Zi extends Fu {}
				//类的多态使用
				Fu f = new Zi();
	* C: 抽象类多态定义格式			
			抽象类 变量名 = new 抽象类子类();
			举例：	
			abstract class Fu {
			         public abstract void method();
				     }
			class Zi extends Fu {
			public void method(){
					      System.out.println(“重写父类抽象方法”);
			}
			}
			//类的多态使用
			Fu fu= new Zi();
	* D: 接口多态定义的格式
			接口 变量名 = new 接口实现类();
			如： interface Fu {
					     public abstract void method();
			}
			class Zi implements Fu {
					     public void method(){
			              System.out.println(“重写接口抽象方法”);
			}
			}
			//接口的多态使用
			Fu fu = new Zi();
	* E: 注意事项
			同一个父类的方法会被不同的子类重写。在调用方法时，调用的为各个子类重写后的方法。
			如 Person p1 = new Student();
			   Person p2 = new Teacher();
			   p1.work(); //p1会调用Student类中重写的work方法
			   p2.work(); //p2会调用Teacher类中重写的work方法
			当变量名指向不同的子类对象时，由于每个子类重写父类方法的内容不同，所以会调用不同的方法。



			 
### 14多态成员方法的特点
	* A: 掌握了多态的基本使用后，那么多态出现后类的成员有啥变化呢？前面学习继承时，我们知道子父类之间成员变量有了自己的特定变化，
		* 那么当多态出现后，成员变量在使用上有没有变化呢？
		* 多态出现后会导致子父类中的成员变量有微弱的变化


	* B: 代码演示
		class Fu {
			int num = 4;
		}
		class Zi extends Fu {
			int num = 5;
		}
		class Demo {
			public static void main(String[] args) 	{
				Fu f = new Zi();
				System.out.println(f.num);
				Zi z = new Zi();
				System.out.println(z.num);
			}
		}
	
	* C: 多态成员变量
		当子父类中出现同名的成员变量时，多态调用该变量时：
		编译时期：参考的是引用型变量所属的类中是否有被调用的成员变量。没有，编译失败。
		运行时期：也是调用引用型变量所属的类中的成员变量。
		简单记：编译和运行都参考等号的左边。编译运行看左边。
	
	* D: 多态出现后会导致子父类中的成员方法有微弱的变化。看如下代码
		class Fu {
			int num = 4;
			void show()	{
				System.out.println("Fu show num");
			}
		}
		class Zi extends Fu {
			int num = 5;
			void show()	{
				System.out.println("Zi show num");
			}
		}
		class Demo {
			public static void main(String[] args) 	{
				Fu f = new Zi();
				f.show();
			}
		}

	* E: 多态成员方法
		编译时期：参考引用变量所属的类，如果没有类中没有调用的方法，编译失败。
		运行时期：参考引用变量所指的对象所属的类，并运行对象所属类中的成员方法。
		简而言之：编译看左边，运行看右边。


### 15instanceof关键字
	* A: 作用
		 可以通过instanceof关键字来判断某个对象是否属于某种数据类型。如学生的对象属于学生类，学生的对象也属于人类

	* 格式:
		boolean  b  = 对象  instanceof  数据类型;

	* 举例:
		Person p1 = new Student(); // 前提条件，学生类已经继承了人类
		boolean flag = p1 instanceof Student; //flag结果为true
		boolean flag2 = p2 instanceof Teacher; //flag结果为false




### 16多态-向上转型
	* A: 多态的转型分为向上转型与向下转型两种：
		
	* B: 向上转型：当有子类对象赋值给一个父类引用时，便是向上转型，多态本身就是向上转型的过程。
		使用格式：
		父类类型  变量名 = new 子类类型();
		如：Person p = new Student();
	
	




==============================第四节课开始====================================




### 17多态-向下转型
	* A: 向下转型：一个已经向上转型的子类对象可以使用强制类型转换的格式，将父类引用转为子类引用，这个过程是向下转型。如果是直接创建父类对象，是无法向下转型的！
		使用格式：
		子类类型 变量名 = (子类类型) 父类类型的变量;
		如:Student stu = (Student) p;  //变量p 实际上指向Student对象
		
### 18多态的好处和弊端
	* A: 多态的好处和弊端
		* 当父类的引用指向子类对象时，就发生了向上转型，即把子类类型对象转成了父类类型。
		  向上转型的好处是隐藏了子类类型，提高了代码的扩展性。
		* 但向上转型也有弊端，只能使用父类共性的内容，而无法使用子类特有功能，功能有限制。
		
	* B: 看如下代码
		//描述动物类，并抽取共性eat方法
		abstract class Animal {
			abstract void eat();
		}
		 
		// 描述狗类，继承动物类，重写eat方法，增加lookHome方法
		class Dog extends Animal {
			void eat() {
				System.out.println("啃骨头");
			}
		
			void lookHome() {
				System.out.println("看家");
			}
		}
		
		// 描述猫类，继承动物类，重写eat方法，增加catchMouse方法
		class Cat extends Animal {
			void eat() {
				System.out.println("吃鱼");
			}
		
			void catchMouse() {
				System.out.println("抓老鼠");
			}
		}
		
		public class Test {
			public static void main(String[] args) {
				Animal a = new Dog(); //多态形式，创建一个狗对象
				a.eat(); // 调用对象中的方法，会执行狗类中的eat方法
				// a.lookHome();//使用Dog类特有的方法，需要向下转型，不能直接使用
				
				// 为了使用狗类的lookHome方法，需要向下转型
		// 向下转型过程中，可能会发生类型转换的错误，即ClassCastException异常
				// 那么，在转之前需要做健壮性判断 
				if( !a instanceof Dog){ // 判断当前对象是否是Dog类型
				 		System.out.println("类型不匹配，不能转换"); 
				 		return; 
				} 
				Dog d = (Dog) a; //向下转型
				d.lookHome();//调用狗类的lookHome方法
			}
		}


	* C 多态总结:
		什么时候使用向上转型：
			当不需要面对子类类型时，通过提高扩展性，或者使用父类的功能就能完成相应的操作，这时就可以使用向上转型。
			如：Animal a = new Dog();
			    a.eat();
		什么时候使用向下转型
			当要使用子类特有功能时，就需要使用向下转型。
				如：Dog d = (Dog) a; //向下转型
				    d.lookHome();//调用狗类的lookHome方法
				向下转型的好处：可以使用子类特有功能。
				弊端是：需要面对具体的子类对象；在向下转型时容易发生ClassCastException类型转换异常。在转换之前必须做类型判断。
			如：if( !a instanceof Dog){…}





### 19多态举例
	 * A: 毕老师和毕姥爷的故事
	 * 案例:
	  /*
		描述毕老师和毕姥爷，
		毕老师拥有讲课和看电影功能
		毕姥爷拥有讲课和钓鱼功能
	  */
		class 毕姥爷 {
			void 讲课() {
				System.out.println("政治");
			}
		
			void 钓鱼() {
				System.out.println("钓鱼");
			}
		}
		
		// 毕老师继承了毕姥爷，就有拥有了毕姥爷的讲课和钓鱼的功能，
		// 但毕老师和毕姥爷的讲课内容不一样，因此毕老师要覆盖毕姥爷的讲课功能
		class 毕老师 extends 毕姥爷 {
			void 讲课() {
				System.out.println("Java");
			}
		
			void 看电影() {
				System.out.println("看电影");
			}
		}
		
		public class Test {
			public static void main(String[] args) {
				// 多态形式
				毕姥爷 a = new 毕老师(); // 向上转型
				a.讲课(); // 这里表象是毕姥爷，其实真正讲课的仍然是毕老师，因此调用的也是毕老师的讲课功能
				a.钓鱼(); // 这里表象是毕姥爷，但对象其实是毕老师，而毕老师继承了毕姥爷，即毕老师也具有钓鱼功能
		
				// 当要调用毕老师特有的看电影功能时，就必须进行类型转换
				毕老师 b = (毕老师) a; // 向下转型
				b.看电影();
			}
		


### 20笔记本电脑案例
	 * A:案例介绍
	 	* 定义USB接口（具备开启功能、关闭功能），笔记本要使用USB设备，即笔记本在生产时需要预留可以插入USB设备的USB接口，即就是笔记本具备使用USB设备的功能，
	 	* 但具体是什么USB设备，笔记本并不关心，只要符合USB规格的设备都可以。鼠标和键盘要想能在电脑上使用，那么鼠标和键盘也必须遵守USB规范，不然鼠标和键盘的生产出来无法使用
		* 进行描述笔记本类，实现笔记本使用USB鼠标、USB键盘
			USB接口，包含开启功能、关闭功能
			笔记本类，包含运行功能、关机功能、使用USB设备功能
			鼠标类，要符合USB接口
			键盘类，要符合USB接口

	* B: 案例分析
		* 阶段一：
			使用笔记本，笔记本有运行功能，需要笔记本对象来运行这个功能
		* 阶段二：
			想使用一个鼠标，又有一个功能使用鼠标，并多了一个鼠标对象。
		* 阶段三：
			还想使用一个键盘 ，又要多一个功能和一个对象
		* 问题：每多一个功能就需要在笔记本对象中定义一个方法，不爽，程序扩展性极差。
			降低鼠标、键盘等外围设备和笔记本电脑的耦合性。




### 21笔记本电脑案例代码实现
	 * A: 代码实现
		定义鼠标、键盘，笔记本三者之间应该遵守的规则
		interface USB {
			void open();// 开启功能
		
			void close();// 关闭功能
		}
		
			鼠标实现USB规则
		class Mouse implements USB {
			public void open() {
				System.out.println("鼠标开启");
			}
		
			public void close() {
				System.out.println("鼠标关闭");
			}
		}
		
			键盘实现USB规则
		class KeyBoard implements USB {
			public void open() {
				System.out.println("键盘开启");
			}
		
			public void close() {
				System.out.println("键盘关闭");
			}
		}
		
			定义笔记本
		class NoteBook {
			// 笔记本开启运行功能
			public void run() {
				System.out.println("笔记本运行");
			}
		
			// 笔记本使用usb设备，这时当笔记本对象调用这个功能时，必须给其传递一个符合USB规则的USB设备
			public void useUSB(USB usb) {
				// 判断是否有USB设备
				if (usb != null) {
					usb.open();
					usb.close();
				}
			}
		
			public void shutDown() {
				System.out.println("笔记本关闭");
			}
		}
		
		public class Test {
			public static void main(String[] args) {
				// 创建笔记本实体对象
				NoteBook nb = new NoteBook();
				// 笔记本开启
				nb.run();
		
				// 创建鼠标实体对象
				Mouse m = new Mouse();
				// 笔记本使用鼠标
				nb.useUSB(m);
		
				// 创建键盘实体对象
				KeyBoard kb = new KeyBoard();
				// 笔记本使用键盘
				nb.useUSB(kb);
		
				// 笔记本关闭
				nb.shutDown();
			}
		}


## 构造方法

### 01构造方法引入
	* A:构造方法的引入
		    在开发中经常需要在创建对象的同时明确对象的属性值，比如员工入职公司就要明确他的姓名、年龄等属性信息。
			那么，创建对象就要明确属性值，那怎么解决呢？也就是在创建对象的时候就要做的事情，当使用new关键字创建对象时，怎么给对象的属性初始化值呢？
			这就要学习Java另外一门小技术，构造方法。
	* B: 那什么是构造方法呢？
	 		从字面上理解即为构建创造时用的方法，即就是对象创建时要执行的方法。既然是对象创建时要执行的方法，那么只要在new对象时，
			知道其执行的构造方法是什么，就可以在执行这个方法的时候给对象进行属性赋值。



	
### 02构造方法作用
	* A: 构造方法的作用:
			在new的同时给成员变量赋值,给对象属性进行初始化。
	* B: 举例:
			Perons p = new Person("张三",23); 在new 的时候给p对象的name属性和age属性进行赋值,使这个对象的属性有值。


			
### 03构造方法的定义和运行特点
	* A: 构造方法定义
			构造方法的格式：
			修饰符 构造方法名(参数列表)
			{
			}

	* B: 构造方法的体现：
			构造方法没有返回值类型。也不需要写返回值。因为它是为构建对象的，对象创建完，方法就执行结束。
			构造方法名称必须和类型保持一致。
			构造方法没有具体的返回值。
			构造方法的代码体现：

	* C: 构造方法举例
			class Person {
				// Person的成员属性age和name
				private int age;
				private String name;
			
				// Person的构造方法，拥有参数列表
				Person(int a, String nm) {
					// 接受到创建对象时传递进来的值，将值赋给成员属性
					age = a;
					name = nm;
				}
			}

	* D: 构造方法运行特点:
			在new 对象的时候自动调用执行。



### 04默认添加的构造方法
	* A: 每一class类都必须有一个构造方法，构造方法不写也有。
		 编译的时候，javac，系统会自动检查类中是否有构造方法，如果没有编译器就会自动添加一个构造方法
		 比如Person类， 编译器添加一个无参构造 public Person(){}
		
### 05构造方法的调用赋值
	* A: 理解构造方法的格式和基本功能之后，现在就要研究构造方法是怎么执行的呢？在创建对象的时候是如何初始化的呢？
		 构造方法是专门用来创建对象的，也就是在new对象时要调用构造方法。现在来看看如何调用构造方法。


	* B: 案例
			class Person {
				// Person的成员属性age和name
				private int age;
				private String name;
			
				// Person的构造方法，拥有参数列表
				Person(int a, String nm) {
					// 接受到创建对象时传递进来的值，将值赋给成员属性
					age = a;
					name = nm;
				}
			
				public void speak() {
					System.out.println("name=" + name + ",age=" + age);
				}
			}
			
			class PersonDemo {
				public static void main(String[] args) {
					// 创建Person对象，并明确对象的年龄和姓名
					Person p2 = new Person(23, "张三");
					p2.speak();
				}
			}

		上述代码演示了创建对象时构造方法的调用。即在创建对象时，会调用与参数列表对应的构造方法


### 06构造方法的内存
		A:内存加载的过程
			有一个Person类, 创建Person 对象new Person()
			1、首先会将main方法压入栈中，执行main方法中的 new Person(23,"张三"); 
			2、在堆内存中分配一片区域，用来存放创建的Person对象，这片内存区域会有属于自己的内存地址（0x88）。然后给成员变量进行默认初始化（name=null，age=0）。
			3、执行构造方法中的代码（age = a ; name = nm;）,将变量a对应的23赋值给age，将变量nm对应的”张三赋值给name，这段代码执行结束后，成员变量age和name的值已经改变。执行结束之后构造方法弹栈，Person对象创建完成。将Person对象的内存地址0x88赋值给p2。





		
==============================第二节课开始====================================	

### 07构造方法的重载			
	* A：当在描述事物时，要不要在类中写构造方法呢？这时要根据描述事物的特点来确定，当描述的事物在创建其对象时就要明确属性的值，这时就需要在定义类的时候书写带参数的构造方法。
	*    若创建对象时不需要明确具体的数据，这时可以不用书写构造方法（不书写也有默认的构造方法）。
			构造方法的细节：
			1、一个类中可以有多个构造方法，多个构造方法是以重载的形式存在的
			2、构造方法是可以被private修饰的，作用：其他程序无法创建该类的对象。
	* B: 举例
		class Person {
			private int age;
			private String name;
		
			// 私有无参数的构造方法，即外界不能通过new Person();语句创建本类对象
			private Person() {
			}
		
			// 多个构造方法是以重载的形式存在
			Person(int a) {
				age = a;
			}
		
			Person(String nm, int a) {
				name = nm;
				age = a;
			}
		}

		


### 08构造方法和一般方法区别
	* A: 目前为止，学习两种方法，分别为构造方法和一般方法，那么他们之间有什么异同呢？
		1.格式不同
		 构造方法 : 修饰符  类名(参数类型 参数 ...){
			初始化成员变量
		}
		一般方法: 需要有返回值类型
		2.作用不同
		构造方法一般用来给成员变量初始化;
		一般方法根据需求而定;
		3.调用方式不同
		构造方法创建对象时调用, 或者this() super() 语句调用
		普通方法需要对象调用或者静态方法直接调用静态方法.
		4.执行不同
		构造方法在对象创建时就执行了，而且只执行一次。
		一般方法是在对象创建后，需要使用时才被对象调用，并可以被多次调用。


		
### 09this在构造方法之间的调用
	* A: 在之前学习方法之间调用时，可以通过方法名进行调用。可是针对构造方法，无法通过构造方法名来相互调用。
		构造方法之间的调用，可以通过this关键字来完成。
		构造方法调用格式：
		this(参数列表);

	* B:调用构造方法的案例
		class Person {
			// Person的成员属性
			private int age;
			private String name;
		
			// 无参数的构造方法
			Person() {
			}
		
			// 给姓名初始化的构造方法
			Person(String nm) {
				name = nm;
			}
		
			// 给姓名和年龄初始化的构造方法
			Person(String nm, int a) {
				// 由于已经存在给姓名进行初始化的构造方法 name = nm;因此只需要调用即可
				// 调用其他构造方法，需要通过this关键字来调用
				this(nm);
				// 给年龄初始化
				age = a;
			}
		}


### 10this在构造方法调用的内存图
	* A: 被加载的代码
		class Person {
			private int age;
			private String name;

			Person() {
			}
			Person(String nm) {
				name = nm;
			}
			Person(String nm, int a) {
				this(nm);
				age = a;
			}
		}

		class PersonDemo {
			public static void main(String[] args) {
				Person p = new Person("张三", 23);
			}
		}

	
	* B: 构造方法调用的原理图
	*   图略
		1、先执行main方法，main方法压栈，执行其中的new Person(“张三”,23);
		2、堆内存中开辟空间，并为其分配内存地址0x33，，紧接着成员变量默认初始化（name=null  age = 0）；
		3、拥有两个参数的构造方法（Person（String nm , int a））压栈，在这个构造方法中有一个隐式的this，因为构造方法是给对象初始化的，那个对象调用到这个构造方法，this就指向堆中的那个对象。
		4、由于Person（String nm , int a）构造方法中使用了this(nm);构造方法Person(String nm)就会压栈，并将“张三”传递给nm。在Person（String nm , int a）构造方法中同样也有隐式的this，this的值同样也为0x33，这时会执行其中name = nm，即把“张三”赋值给成员的name。当赋值结束后Person（String nm , int a）构造方法弹栈。
		5、程序继续执行构造方法（Person（String nm , int a）中的age = a；这时会将23赋值给成员属性age。赋值结束构造方法（Person（String nm , int a）弹栈。
		6、当构造方法（Person（String nm , int a）弹栈结束后，Person对象在内存中创建完成，并将0x33赋值给main方法中的p引用变量。
		注意：
		this到底代表什么呢？this代表的是对象，具体代表哪个对象呢？哪个对象调用了this所在的方法，this就代表哪个对象。
		调用其他构造方法的语句必须定义在构造方法的第一行，原因是初始化动作要最先执行。


### 11this简易应用
	* A: 当在方法中出现了局部变量和成员变量同名的时候，那么在方法中怎么区别局部变量成员变量呢？可以在成员变量名前面加上this.来区别成员变量和局部变量
	* B: 举例1
		class Person {
			private int age;
			private String name;
		
			// 给姓名和年龄初始化的构造方法
			Person(String name, int age) {
				// 当需要访问成员变量是，只需要在成员变量前面加上this.即可
				this.name = name;
				this.age = age;
			}
		
			public void speak() {
				System.out.println("name=" + this.name + ",age=" + this.age);
			}
		}
		
		class PersonDemo {
			public static void main(String[] args) {
				Person p = new Person("张三", 23);
				p.speak();
			}
		}

	* C: 举例2
		学习完了构造方法、this的用法之后，现在做个小小的练习。
		需求：在Person类中定义功能，判断两个人是否是同龄人
		class Person {
			private int age;
			private String name;
		
			// 给姓名和年龄初始化的构造方法
			Person(String name, int age) {
				// 当需要访问成员变量是，只需要在成员变量前面加上this.即可
				this.name = name;
				this.age = age;
			}
		
			public void speak() {
				System.out.println("name=" + this.name + ",age=" + this.age);
			}
		
			// 判断是否为同龄人
			public boolean equalsAge(Person p) {
				// 使用当前调用该equalsAge方法对象的age和传递进来p的age进行比较
				// 由于无法确定具体是哪一个对象调用equalsAge方法，这里就可以使用this来代替
				/*
				 * if(this.age == p.age) { return true; } return false;
				 */
				return this.age = p.age;
			}
		}



		
==============================第三节课开始====================================


	
### 12super关键字_1
	
	* A: 子父类中构造方法的调用
		在创建子类对象时，父类的构造方法会先执行，因为子类中所有构造方法的第一行有默认的隐式super();语句。
	* B: 格式：
		调用本类中的构造方法
		this(实参列表);
		调用父类中的空参数构造方法
		super();
		调用父类中的有参数构造方法
		super(实参列表);


### 13super关键字_2
	* A:子类构造方法,有一个默认添加的构造方法
		public class Student extends Person {
			 public Student(){
			 	super();
			 }
		}
	* B :为什么子类对象创建都要访问父类中的构造方法？因为子类继承了父类的内容，所以创建对象时，必须要先看父类是如何对其内容进行初始化的，看如下程序
		public class Test {
			public static void main(String[] args) {
				new Zi();
			}
			
		}
		class Fu{
			int num ;
			Fu(){
				System.out.println("Fu构造方法"+num);
				num = 4;
			}
		}
		class Zi extends Fu{
			Zi(){
		         //super(); 调用父类空参数构造方法
				System.out.println("Zi构造方法"+num);
			}
		}

		执行结果：
　　     Fu构造方法0
　　     Zi构造方法4

		通过结果发现，子类构造方法执行时中，调用了父类构造方法，这说明，子类构造方法中有一句super()。
		那么，子类中的构造方法为什么会有一句隐式的super()呢？
		原因：子类会继承父类中的内容，所以子类在初始化时，必须先到父类中去执行父类的初始化动作。这样，才可以使用父类中的内容。
		当父类中没有空参数构造方法时，子类的构造方法必须有显示的super语句，指定要访问的父类有参数构造方法。

	 
### 14子类父类的内存图
		略: 
		具体见 day12_source/子类父类的内存图.JPG	



### 15super关键字_3
	* A: 创建子类对象的时候会必须调用父类的构造方法。
	   子类默认会调用父类的无参构造， 但如果父类没有无参构造，子类的构造方法继续调用父类的无参构造就会报错。
	   因此子类构造方法的第一行需要调用父类的构造方法，既可以调用父类的无参构造，也可以调用父类的有参构造，这样语法上就不会报错。
		


### 16super关键字_4
	* A: 构造方法第一行,写this()还是super()
	*  this() 是调用本类的构造方法,super()是调用父类的构造方法, 且两条语句不能同时存在
	*  保证子类的所有构造方法调用到父类的构造方法即可
	
	* B: 小结:
	* 无论如何,子类的所有构造方法,直接或间接必须调用到父类构造方法;
	* 子类的构造方法什么都不写,默认的构造方法第一行super()

		
### 17创建子类对象过程的细节
	* A 创建子类对象过程的细节
	* 如果子类的构造方法第一行写了this调用了本类其他构造方法，那么super调用父类的语句还有吗？
	* 这时是没有的，因为this()或者super(),只能定义在构造方法的第一行，因为初始化动作要先执行。
	* 父类构造方法中是否有隐式的super呢？
	* 也是有的。记住：只要是构造方法默认第一行都是super();
	* 父类的父类是谁呢？super调用的到底是谁的构造方法呢？
	* Java体系在设计，定义了一个所有对象的父类Object

	* 注意：
		类中的构造方法默认第一行都有隐式的super()语句，在访问父类中的空参数构造方法。所以父类的构造方法既可以给自己的对象初始化，也可以给自己的子类对象初始化。
		如果默认的隐式super()语句在父类中没有对应的构造方法，那么必须在构造方法中通过this或者super的形式明确要调用的构造方法。




==============================第四节课开始====================================

### 18super的应用
	 * A: 练习：描述学生和工人这两个类，将他们的共性name和age抽取出来存放在父类中，并提供相应的get和set方法，同时需要在创建学生和工人对象就必须明确姓名和年龄
	 * 案例:
		//定义Person类，将Student和Worker共性抽取出来
		class Person {
			private String name;
			private int age;
			public Person(String name, int age) {
				// super();
				this.name = name;
				this.age = age;
			}
			public String getName() {
				return name;
			}
			public void setName(String name) {
				this.name = name;
			}
			public int getAge() {
				return age;
			}
			public void setAge(int age) {
				this.age = age;
			}
		}
		class Student extends Person {
			// Student类的构造方法
			Student(String name, int age) {
				// 使用super关键字调用父类构造方法，进行相应的初始化动作
				super(name, age);
			}
			public void study() {// Studnet中特有的方法
				System.out.println(this.getName() + "同学在学习");
			}
		}
		class Worker extends Person {
			Worker(String name, int age) {
				// 使用super关键字调用父类构造方法，进行相应的初始化动作
				super(name, age);
			}
			public void work() {// Worker 中特有的方法
				System.out.println(this.getName() + "工人在工作");
			}
		}
		public class Test {
			public static void main(String[] args) {
				Student stu = new Student("小明",23);
		stu.study();
				
		Worker w = new Worker("小李",45);
		w.work();
			}
		}


### 19完整员工案例分析
	 * A: 项目介绍
		某IT公司有多名员工，按照员工负责的工作不同，进行了部门的划分（研发部员工、维护部员工）。研发部根据所需研发的内容不同，又分为JavaEE工程师、Android工程师；维护部根据所需维护的内容不同，又分为网络维护工程师、硬件维护工程师。
		公司的每名员工都有他们自己的员工编号、姓名，并要做它们所负责的工作。
		工作内容
		JavaEE工程师：员工号为xxx的 xxx员工，正在研发淘宝网站
		Android工程师：员工号为xxx的 xxx员工，正在研发淘宝手机客户端软件
		网络维护工程师：员工号为xxx的 xxx员工，正在检查网络是否畅通
		硬件维护工程师：员工号为xxx的 xxx员工，正在修复打印机
		请根据描述，完成员工体系中所有类的定义，并指定类之间的继承关系。进行XX工程师类的对象创建，完成工作方法的调用。

	* B: 案例分析
		根据上述部门的描述，得出如下的员工体系图
	 
		根据员工信息的描述，确定每个员工都有员工编号、姓名、要进行工作。则，把这些共同的属性与功能抽取到父类中（员工类），关于工作的内容由具体的工程师来进行指定。
		工作内容
		JavaEE工程师：员工号为xxx的 xxx员工，正在研发淘宝网站
		Android工程师：员工号为xxx的 xxx员工，正在研发淘宝手机客户端软件
		网络维护工程师：员工号为xxx的 xxx员工，正在检查网络是否畅通
		硬件维护工程师：员工号为xxx的 xxx员工，正在修复打印机
		创建JavaEE工程师对象，完成工作方法的调用



### 20案例代码实现
	 * A:定义员工类(抽象类)
		public abstract class Employee {
			private String id;// 员工编号
			private String name; // 员工姓名
			
			//空参数构造方法
			public Employee() {
				super();
			}
			//有参数构造方法
			public Employee(String id, String name) {
				super();
				this.id = id;
				this.name = name;
			}
			public String getId() {
				return id;
			}
			public void setId(String id) {
				this.id = id;
			}
			public String getName() {
				return name;
			}
			public void setName(String name) {
				this.name = name;
			}
			//工作方法（抽象方法）
			public abstract void work(); 
		}
		
		* B :	定义研发部员工类Developer 继承 员工类Employee
		public abstract class Developer extends Employee {
			//空参数构造方法
			public Developer() {
				super();
			}
			//有参数构造方法
			public Developer(String id, String name) {
				super(id, name);
			}
		}
		
		* C:	定义维护部员工类Maintainer 继承 员工类Employee
		public abstract class Maintainer extends Employee {
			//空参数构造方法
			public Maintainer() {
				super();
			}
			//有参数构造方法
			public Maintainer(String id, String name) {
				super(id, name);
			}
		}
		
		* D:	定义JavaEE工程师 继承 研发部员工类，重写工作方法
		public class JavaEE extends Developer {
			//空参数构造方法
			public JavaEE() {
				super();
			}
			//有参数构造方法
			public JavaEE(String id, String name) {
				super(id, name);
			}
		
			@Override
			public void work() {
				System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在研发淘宝网站");
			}
		}
		
		* E:	定义Android工程师 继承 研发部员工类，重写工作方法
		public class Android extends Developer {
			//空参数构造方法
			public Android() {
				super();
			}
			//有参数构造方法
			public Android(String id, String name) {
				super(id, name);
			}
		
			@Override
			public void work() {
				System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在研发淘宝手机客户端软件");
			}
		}
		
		* F:	定义Network网络维护工程师 继承 维护部员工类，重写工作方法
		public class Network extends Maintainer {
			//空参数构造方法
			public Network() {
				super();
			}
			//有参数构造方法
			public Network(String id, String name) {
				super(id, name);
			}
		
			@Override
			public void work() {
				System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在检查网络是否畅通");
			}
		}
		
		* G:	定义Hardware硬件维护工程师 继承 维护部员工类，重写工作方法
		public class Hardware extends Maintainer {
			//空参数构造方法
			public Hardware() {
				super();
			}
			//有参数构造方法
			public Hardware(String id, String name) {
				super(id, name);
			}
		
			@Override
			public void work() {
				System.out.println("员工号为 " + getId() + " 的 " + getName() + " 员工，正在修复打印机");
			}
		}
		
		* H:	在测试类中，创建JavaEE工程师对象，完成工作方法的调用
		public class Test {
			public static void main(String[] args) {
				//创建JavaEE工程师员工对象，该员工的编号000015，员工的姓名 小明
				JavaEE ee = new JavaEE("000015", "小明");
				//调用该员工的工作方法
				ee.work();
			}
		}



### 21总结
	* 把今天的知识点总结一遍。
## final static 关键字 内部类

### 01final关键字概念
	* A: 概述
			继承的出现提高了代码的复用性，并方便开发。但随之也有问题，有些类在描述完之后，不想被继承，
			或者有些类中的部分方法功能是固定的，不想让子类重写。可是当子类继承了这些特殊类之后，
			就可以对其中的方法进行重写，那怎么解决呢？
			要解决上述的这些问题，需要使用到一个关键字final，final的意思为最终，不可变。
			final是个修饰符，它可以用来修饰类，类的成员，以及局部变量。



	
### 02final修饰类义
	* A: final 修饰类
			final修饰类不可以被继承，但是可以继承其他类。
	* B: 案例
			class Yy {}
			final class Fu extends Yy{} //可以继承Yy类
			class Zi extends Fu{} //不能继承Fu类

	
			
### 03final修饰方法
	* A: final修饰方法
				final修饰的方法不可以被覆盖,但父类中没有被final修饰方法，子类覆盖后可以加final。
	* B: 案例	
	 		class Fu {
				// final修饰的方法，不可以被覆盖，但可以继承使用
				public final void method1(){}
				public void method2(){}
			}
			class Zi extends Fu {
				//重写method2方法
				public final void method2(){}
			}




### 04final修饰局部变量
	* A:修饰基本数据类型变量
		final修饰的变量称为常量，这些变量只能赋值一次
		

	* B:案例1
			final int i = 20;
			i = 30; //赋值报错，final修饰的变量只能赋值一次
			
	* C: 修饰引用数据类型
			引用类型的变量值为对象地址值，地址值不能更改，但是地址内的对象属性值可以修改
	
	* D: 修饰引用数据类型
			final Person p = new Person();
			Person p2 = new Person();
			p = p2; //final修饰的变量p，所记录的地址值不能改变
			p.name = "小明";//可以更改p对象中name属性值
			p不能为别的对象，而p对象中的name或age属性值可更改。

	
### 05final修饰成员变量
	* A: 修饰成员变量
		 修饰成员变量，需要在创建对象前赋值，否则报错。(当没有显式赋值时，多个构造方法的均需要为其赋值。)

	* B: 案例
			class Demo {
				//直接赋值
				final int m = 100;
				
				//final修饰的成员变量，需要在创建对象前赋值，否则报错。
				final int n; 
				public Demo(){
					//可以在创建对象时所调用的构造方法中，为变量n赋值
					n = 2016;
				}
			}


### 06static的概念
	* A：概念
		当在定义类的时候，类中都会有相应的属性和方法。而属性和方法都是通过创建本类对象调用的。
		当在调用对象的某个方法时，这个方法没有访问到对象的特有数据时，方法创建这个对象有些多余。
		可是不创建对象，方法又调用不了，这时就会想，那么我们能不能不创建对象，就可以调用方法呢？
		可以的，我们可以通过static关键字来实现。static它是静态修饰符，一般用来修饰类中的成员。






### 07static修饰的对象特有数据			
	* A：特点1:
			被static修饰的成员变量属于类，不属于这个类的某个对象。
			（也就是说，多个对象在访问或修改static修饰的成员变量时，其中一个对象将static成员变量值进行了修改，
			其他对象中的static成员变量值跟着改变，即多个对象共享同一个static成员变量）
	* B: 代码演示
			class Demo {
				public static int num = 100;
			}

			class Test {
				public static void main(String[] args) {
					Demo d1 = new Demo();
					Demo d2 = new Demo();
					d1.num = 200;
					System.out.println(d1.num); //结果为200
					System.out.println(d2.num); //结果为200
				}
			}

	


### 08static的内存图
	* A: 略
			参考day13_source 静态的内存图.jpg

		
### 09static注意事项_静态不能直接调用非静态
	* A: 注意事项	
			被static修饰的成员可以并且建议通过类名直接访问。
			
	* B: 访问静态成员的格式：
			类名.静态成员变量名
			类名.静态成员方法名(参数)
			对象名.静态成员变量名     		------不建议使用该方式，会出现警告
			对象名.静态成员方法名(参数) 	------不建议使用该方式，会出现警告
			
	* C: 代码演示
			class Demo {
				//静态成员变量
				public static int num = 100;
				//静态方法
				public static void method(){
					System.out.println("静态方法");
				}
			}
			class Test {
				public static void main(String[] args) {
					System.out.println(Demo.num);
					Demo.method();
				}
			}

		

### 10static静态的使用场景
	* A: 使用场景
		static可以修饰成员变量和成员方法。	
		什么时候使用static修饰成员变量？
			加static修饰成员的时候，这个成员会被类的所有对象所共享。一般我们把共性数据定义为静态的变量
		什么时候使用static修饰成员方法？
			静态的方法只能访问静态的成员，如果静态方法中引用到了静态的其他成员，那么这个方法需要声明为静态的方法。
	
### 11对象中的静态调用
	* A: 对象的静态调用
	  在多态中，非静态编译看父类，运行看子类，父类没有编译失败。
	  但多态中的静态方法,编译看父类,运行仍然看父类。因为静态和对象没有关系，属于静态绑定。

	* B: 举例
		public class Test{
			public static void main(String[] args){
				Fu f = new Zi();
				f.show();   //父类的引用和父类的方法绑定,和对象无关,不会在运行时动态的执行子类特有的方法。
			}
		}
		
### 12定义静态常量
	* A: 静态常量
		开发中，我们想在类中定义一个静态常量，通常使用public static final修饰的变量来完成定义。
		此时变量名用全部大写，多个单词使用下划线连接。
	* B: 定义格式：
		public static final 数据类型 变量名 = 值;
		
	* C: 如下演示：
		class Company {
			public static final String COMPANY_NAME = "传智播客";
			public static void method(){
				System.out.println("一个静态方法");
			}
		}

		当我们想使用类的静态成员时，不需要创建对象，直接使用类名来访问即可。
		System.out.println(Company.COMPANY_NAME); //打印传智播客
		Company.method(); // 调用一个静态方法

	* D: 注意：
		接口中的每个成员变量都默认使用public static final修饰。
		所有接口中的成员变量已是静态常量，由于接口没有构造方法，所以必须显示赋值。可以直接用接口名访问。
		interface Inter {
			public static final int COUNT = 100;
		}
			访问接口中的静态变量
		Inter.COUNT
			
			

### 13匿名对象
	* A:匿名对象的概述
		* 匿名对象是指创建对象时，只有创建对象的语句，却没有把对象地址值赋值给某个变量。
	* B:案例
		public class Person{
			public void eat(){
				System.out.println();
		}
		}

		创建一个普通对象
		Person p = new Person();
		创建一个匿名对象
		new Person();
	
	* C: 匿名对象的特点
		a:创建匿名对象直接使用，没有变量名。
			new Person().eat()  //eat方法被一个没有名字的Person对象调用了。

		b:匿名对象在没有指定其引用变量时，只能使用一次。
			new Person().eat(); 创建一个匿名对象，调用eat方法
			new Person().eat(); 想再次调用eat方法，重新创建了一个匿名对象
			
		c:匿名对象可以作为方法接收的参数、方法返回值使用
			class Demo {
				public static Person getPerson(){
					//普通方式
					//Person p = new Person();	
					//return p;
					
					//匿名对象作为方法返回值
					return new Person(); 
				}
				
				public static void method(Person p){}
			}

			class Test {
				public static void main(String[] args) {
					//调用getPerson方法，得到一个Person对象
					Person person = Demo.getPerson();
					
					//调用method方法
					Demo.method(person);
					//匿名对象作为方法接收的参数
					Demo.method(new Person());
				}
			}

			 
### 14内部类
	* A: 内部类的概述
		将类写在其他类的内部，可以写在其他类的成员位置和局部位置，这时写在其他类内部的类就称为内部类。
		其他类也称为外部类。
	* B: 什么时候使用内部类
		在描述事物时，若一个事物内部还包含其他可能包含的事物，比如在描述汽车时，汽车中还包含这发动机，
		这时发动机就可以使用内部类来描述。
		class 汽车 { //外部类
			class 发动机 { //内部类
			}
		}
	* C: 内部类的分类
		内部类分为成员内部类与局部内部类。
		我们定义内部类时，就是一个正常定义类的过程，同样包含各种修饰符、继承与实现关系等。
		在内部类中可以直接访问外部类的所有成员。



### 15成员内部类的调用格式
	* A: 格式
		成员内部类，定义在外部类中的成员位置。与类中的成员变量相似，可通过外部类对象进行访问
	* B: 定义格式
		class 外部类 { 
			修饰符 class 内部类 {
				//其他代码
			}
		}

	* C: 访问方式
		外部类名.内部类名 变量名 = new 外部类名().new 内部类名();

	* D: 成员内部类代码演示
		class Body {//外部类，身体
			 private boolean life= true; //生命状态
			 public class Heart { //内部类，心脏
				 public void jump() {
					 System.out.println("心脏噗通噗通的跳")
						System.out.println("生命状态" + life); //访问外部类成员变量
				}
			}
		}

		访问内部类
		public static void main(String[] args) {
			//创建内部类对象
			Body.Heart bh = new Body().new Heart();
			//调用内部类中的方法
			bh.jump();
		}


		


### 16成员内部类的同名变量调用
	* A: 代码实现
		public class Outer {
			int i  = 1;
			class Inner {
				int i  = 2;
				public void inner(){
					int i = 3;
					System.out.println(Outer.this.i);
				}
			}
		}

		
### 17局部内部类
	* A 局部内部类，定义在外部类方法中的局部位置。与访问方法中的局部变量相似，可通过调用方法进行访问.
	* B 定义格式
		class 外部类 { 
			修饰符 返回值类型 方法名(参数) {
				class 内部类 {
					//其他代码
				}
			}
		}
	* C 访问方式
		在外部类方法中，创建内部类对象，进行访问

	* D 局部内部类代码演示
		定义类
		class Party {//外部类，聚会
			public void puffBall(){// 吹气球方法
				class Ball {// 内部类，气球
					  public void puff(){
						System.out.println("气球膨胀了");
					  }
				}
				//创建内部类对象，调用puff方法
				new Ball().puff();
			}
		}
		访问内部类
		public static void main(String[] args) {	
			//创建外部类对象
			Party p = new Party();
			//调用外部类中的puffBall方法
			p.puffBall();
		}





### 18匿名内部类
	 * A: 概述
	 内部类是为了应对更为复杂的类间关系。查看源代码中会涉及到，而在日常业务中很难遇到，这里不做赘述。
	 最常用到的内部类就是匿名内部类，它是局部内部类的一种。
	 定义的匿名内部类有两个含义：
	 临时定义某一指定类型的子类
	 定义后即刻创建刚刚定义的这个子类的对象

	* B: 本质
	 匿名内部类的本质是一个实现了接口或继承了某个类的子类匿名对象.
	 
	* C: 案例
	public interface Smoking {
		public abstract void smoking();
		}
		/*
		 *  实现类,实现接口 重写接口抽象方法,创建实现类对象
		 *  class XXX implements Smoking{
		 *      public void smoking(){
		 *      
		 *      }
		 *  }
		 *  XXX x = new XXX();
		 *  x.smoking(); 
		 *  Smoking s = new XXX();
		 *  s.smoking();
		 *  
		 *  匿名内部类,简化问题:  定义实现类,重写方法,建立实现类对象,合为一步完成
		 */

	测试类:
	public class Test {
		public static void main(String[] args) {
			//使用匿名内部类
			/*
			 *  定义实现类,重写方法,创建实现类对象,一步搞定
			 *  格式:
			 *    new 接口或者父类(){
			 *       重写抽象方法
			 *    };
			 *    从 new开始,到分号结束
			 *    创建了接口的实现类的对象
			 */
			new Smoking(){
				public void smoking(){
					System.out.println("人在吸烟");
				}
			}.smoking();
		}
	}


### 19匿名内部类_2
	 * A: 匿名内部类案例演示
		public abstract class Animal {
			public abstract void eat();
			public abstract void sleep();
		}

	测试代码
	/*
	 *    new Animal(){
				public void eat(){
					System.out.println("在吃饭");
				} 
				public void sleep(){
					System.out.println("在睡觉");
				}
			 };
		以上代码,就是Animal的子类的对象
		多态性, 父类引用 = 子类的对象

	 */
	public class Test2 {
		public static void main(String[] args) {
			Animal a= new Animal(){
				public void eat(){
					System.out.println("在吃饭");
				} 
				public void sleep(){
					System.out.println("在睡觉");
				}
			 };
			 a.eat();
			 a.sleep();
		}
	}


### 20包的概念 
	 * A: 概念
		java的包，其实就是我们电脑系统中的文件夹，包里存放的是类文件。
		当类文件很多的时候，通常我们会采用多个包进行存放管理他们，这种方式称为分包管理。
		在项目中，我们将相同功能的类放到一个包中，方便管理。并且日常项目的分工也是以包作为边界。
		类中声明的包必须与实际class文件所在的文件夹情况相一致，即类声明在a包下，则生成的.class文件必须在a文件夹下，否则，程序运行时会找不到类。
	
	* B 声明格式
		通常使用公司网址反写，可以有多层包，包名采用全部小写字母，多层包之间用”.”连接
			类中包的声明格式： 
		package 包名.包名.包名…;
			如：黑马程序员网址itheima.com那么网址反写就为com.itheima
				传智播客 itcast.cn  那么网址反写就为 cn.itcast
			注意：声明包的语句，必须写在程序有效代码的第一行（注释不算）
		代码演示：
		package cn.itcast; //包的声明，必须在有效代码的第一行
		
		import java.util.Scanner;
		import java.util.Random;

		public class Demo {}
		
	* C: 包的访问
		在访问类时，为了能够找到该类，必须使用含有包名的类全名（包名.类名）。
		包名.包名….类名
		如： java.util.Scanner
			 java.util.Random
			cn.itcast.Demo
		带有包的类，创建对象格式：包名.类名 变量名 = new包名.类名();
			 cn.itcast.Demo d = new cn.itcast.Demo();
			前提：包的访问与访问权限密切相关，这里以一般情况来说，即类用public修饰的情况。

			类的简化访问
		当我们要使用一个类时，这个类与当前程序在同一个包中（即同一个文件夹中），或者这个类是java.lang包中的类时通常可以省略掉包名，直接使用该类。
		如：cn.itcast包中有两个类，PersonTest类，与Person类。我们在PersonTest类中，访问Person类时，由于是同一个包下，访问时可以省略包名，即直接通过类名访问 Person。
		类名 变量名 = new类名();
		Person p = new Person();

			当我们要使用的类，与当前程序不在同一个包中（即不同文件夹中），要访问的类必须用public修饰才可访问。
		package cn.itcst02;
		public class Person {}


		
### 22导入包
	  * A:导入包
		我们每次使用类时，都需要写很长的包名。很麻烦，我们可以通过import导包的方式来简化。
		可以通过导包的方式使用该类，可以避免使用全类名编写（即，包类.类名）。
		导包的格式：
		import 包名.类名;

			当程序导入指定的包后，使用类时，就可以简化了。演示如下
		//导入包前的方式
		//创建对象
		java.util.Random r1 = new java.util.Random();
		java.util.Random r2 = new java.util.Random();
		java.util.Scanner sc1 = new java.util.Scanner(System.in);
		java.util.Scanner sc2 = new java.util.Scanner(System.in);

		//导入包后的方式
		import java.util.Random;
		import java.util.Scanner;
		//创建对象
		Random r1 = new Random();
		Random r2 = new Random();
		Scanner sc1 = new Scanner(System.in);
		Scanner sc2 = new Scanner(System.in);
		import导包代码书写的位置：在声明包package后，定义所有类class前，使用导包import包名.包名.类名;

	  
### 23权限修饰符
	 * A 权限修饰符有哪些
			 在Java中提供了四种访问权限，使用不同的访问权限时，被修饰的内容会有不同的访问权限，
			 以下表来说明不同权限的访问能力：
						            public			protected	  default		private
			 同一类中	              √	               √	         √	           √
			 同一包中(子类与无关类)	  √	               √	          √	
			 不同包的子类	          √	               √		
			 不同包中的无关类	      √			
	* B: 小结
		归纳一下：在日常开发过程中，编写的类、方法、成员变量的访问
		要想仅能在本类中访问使用private修饰；
		要想本包中的类都可以访问不加修饰符即可；
		要想本包中的类与其他包中的子类可以访问使用protected修饰
		要想所有包中的所有类都可以访问使用public修饰。
		注意：如果类用public修饰，则类名必须与文件名相同。一个文件中只能有一个public修饰的类。




### 24代码块
	 * A: 概述:
		程序中用大括号括起来的代码叫代码块
	 * B: 分类
	  局部代码块  构造代码块  静态代码块  同步代码块
	 
	 * C 局部代码块:
		局部代码块是定义在方法或语句中
		特点：
			以”{}”划定的代码区域，此时只需要关注作用域的不同即可
			方法和类都是以代码块的方式划定边界的

		  class Demo{
				public static void main(String[] args)	{
					{
							 int x = 1;
							 System.out.println("普通代码块" + x);
					}
					int x = 99;
					System.out.println("代码块之外" + x);
				}
		  }
		  结果：
			普通代码块1
			代码块之外99
		  局部代码块作用:可以限定变量的声明周期.

	* D: 构造代码块
		构造代码块是定义在类中成员位置的代码块
		特点：
			优先于构造方法执行，构造代码块用于执行所有对象均需要的初始化动作
			每创建一个对象均会执行一次构造代码块。
		public class Person {
			private String name;
			private int age;
			
			 //构造代码块
			{
				System.out.println("构造代码块执行了");
			}
			Person(){
				System.out.println("Person无参数的构造函数执行");
			}
			Person(int age){
				this.age = age;
				System.out.println("Person（age）参数的构造函数执行");
			}
		}
		class PersonDemo{
			public static void main(String[] args)	{
				Person p = new Person();
				Person p1 = new Person(23);
			}
		}

	* E: 静态代码块
		静态代码块是定义在成员位置，使用static修饰的代码块。
		特点：
			它优先于主方法执行、优先于构造代码块执行，当以任意形式第一次使用到该类时执行。
			该类不管创建多少对象，静态代码块只执行一次。
			可用于给静态变量赋值，用来给类进行初始化。
			public class Person {
				private String name;
				private int age;
				 //静态代码块
				static{
					System.out.println("静态代码块执行了");
				}
			}
			
	* F: 同步代码块(多线程学习)

### 25总结
	* 把今天的知识点总结一遍。


### 01eclipse快捷键
	* A: 	Ctrl+T：查看所选中类的继承树
		例如，在下面代码中，选中Teacher类名，然后按Ctrl+T，就会显示出Teacher类的继承关系

	* B:	查看所选中方法的源代码
		Ctrl+滑动鼠标点击方法名，或者选中方法名后，按F3键查看所选中方法的源代码。

### 02java中的文档注释和制作
	* A: 在eclipse使用时，可以配合文档注释，导出对类的说明文档，从而供其	     他人阅读学习与使用。
		通过使用文档注释，将类或者方法进行注释用@简单标注基本信息。如@author 作者、@version代码版本、@param方法参数、@return方法返回值等。

			
### 03eclipse生成jar包	
### 04JAVA_HOME配置	
### 05导入jar包	
	* A: 	导入jar包：即把指定的jar包，加入到指项目中，提供给项目使用。
		导入jar包的过程是将jar包加入到项目的.classpath文件中去，让项目识别，便可以使用jar包中所有的.class文件类。
		以下是加入步骤：
		1：项目根文件夹下创建lib文件夹，用于同一管理所有的jar文件
		2：把jar文件复制到lib文件夹中
		3：右键点击jar文件，点击Build Path，选择Add to Build Path，此时查看项目根文件夹下的.classpath文件，发现新加入的jar包路径被配置到了该文件中。说明可以使用jar包中所有类了。

	注意：
		Jar包加入后，必须Add to Build Path才能使用
		Jar包加入后，加入的类也必须导包，如果加入的类其包名与现有类包名相同，则视作在同一个包下。(不常见)
				

### 07不同修饰符使用细节
	
	A: 常用来修饰类、方法、变量的修饰符如下：
		public 权限修饰符，公共访问, 类,方法,成员变量
		protected 权限修饰符，受保护访问, 方法,成员变量
		默认什么也不写 也是一种权限修饰符，默认访问, 类,方法,成员变量
		private 权限修饰符，私有访问, 方法,成员变量
		static 静态修饰符  方法,成员变量
		final 最终修饰符   类,方法,成员变量,局部变量
		abstract 抽象修饰符  类 ,方法

	B: 不能同时使用的修饰符
		同时，abstract与private不能同时使用；
		同时，abstract与static不能同时使用；
		同时，abstract与final不能同时使用。

	C: 修饰类能够使用的修饰符：
		修饰类只能使用public、默认的、final、abstract关键字
		使用最多的是 public关键字

		a:代码案例
			public class Demo {} //最常用的方式
			class Demo2{}
			public final class Demo3{}
			public abstract class Demo4{}

	D:修饰成员变量能够使用的修饰符：
		public : 公共的
		protected : 受保护的
			: 默认的
		private ：私有的
		final : 最终的
		static : 静态的
		使用最多的是 private

		a: 代码案例
			public int count = 100;
			protected int count2 = 100;
			int count3 = 100;
			private int count4 = 100; //最常用的方式
			public final int count5 = 100;
			public static int count6 = 100;


	E:修饰构造方法能够使用的修饰符：
		public : 公共的
		protected : 受保护的
			: 默认的
		private ：私有的
		使用最多的是 public

		a:代码案例
			public Demo(){} //最常用的方式
			protected Demo(){}
			Demo(){}
			private Demo(){}

			修饰成员方法能够使用的修饰符：
				public : 公共的
				protected : 受保护的
					: 默认的
				private ：私有的
				final : 最终的
				static : 静态的
				abstract : 抽象的
				使用最多的是 public
			public void method1(){}//最常用的方式
			protected void method2(){}
			void method3(){}
			private void method4(){}
			public final void method5(){}
			public static void method6(){}//最常用的方式
			public abstract void method7();//最常用的方式


### 07局部变量和成员变量解析
	* A：程序编译
			数学工具类
	public class MathTool {
		//求两个数的和的二倍
		public double sum2times(int number,int number2) {
			return (number+number2)*2;
		}
		//求两个数的积
		public double area(int number,int number2) {
			return number*number2;
		}
	}

	长方形类
	public class CFX {
		//因为长与宽，在现实事物中属于事物的一部分，所以定义成员变量
		private int chang;
		private int kuan;
		
		public CFX(int chang, int kuan) {
			this.chang = chang;
			this.kuan = kuan;
		}
		
		//求长与宽的周长
		public double zhouChang() {
			return (chang+kuan)*2;
		}
		//求长与宽的面积
		public double mianJi() {
			return chang*kuan;
		}
		public int getChang() {
			return chang;
		}
		public void setChang(int chang) {
			this.chang = chang;
		}
		public int getKuan() {
			return kuan;
		}
		public void setKuan(int kuan) {
			this.kuan = kuan;
		}
	}


### 08类作为方法的参数			
	* A：	类作为方法参数
		在编写程序中，会经常碰到调用的方法要接收的是一个类类型的情况，那么这时，要向方法中传入该类的对象。

		如下代码演示：
			class Person{
				public void show(){
					System.out.println("show方法执行了");
				}
			}
			//测试类
			public class Test {
				public static void main(String[] args) {
					//创建Person对象
					Person p = new Person();
					//调用method方法
					method(p);
				}
				
			//定义一个方法method，用来接收一个Person对象，在方法中调用Person对象的show方法
			public static void method(Person p){
				p.show();
			}


### 09抽象类作为方法参数与返回值
	* A: 	抽象类作为方法参数
		今后开发中，抽象类作为方法参数的情况也很多见。当遇到方法参数为抽象类类型时，要传入一个实现抽象类所有抽象方法的子类对象。如下代码演示：
		//抽象类
		abstract class Person{
			public abstract void show();
		}
		class Student extends Person{
			@Override
			public void show() {
				System.out.println("重写了show方法");
			}
		}
		//测试类
		public class Test {
			public static void main(String[] args) {
				//通过多态的方式，创建一个Person类型的变量，而这个对象实际是Student
				Person p = new Student();
				//调用method方法
				method(p);
			}
			
			//定义一个方法method，用来接收一个Person类型对象，在方法中调用Person对象的show方法
			public static void method(Person p){//抽象类作为参数
				//通过p变量调用show方法,这时实际调用的是Student对象中的show方法
				p.show();	
		}
		}


	* B:	抽象类作为方法返回值
		抽象类作为方法返回值的情况，也是有的，这时需要返回一个实现抽象类所有抽象方法的子类对象。如下代码演示：
		//抽象类
		abstract class Person{
			public abstract void show();
		}
		class Student extends Person{
			@Override
			public void show() {
				System.out.println("重写了show方法");
			}
		}
		//测试类
		public class Test {
			public static void main(String[] args) {
				//调用method方法，获取返回的Person对象
				Person p = method();
				//通过p变量调用show方法,这时实际调用的是Student对象中的show方法
				p.show();
			}
			
			//定义一个方法method，用来获取一个Person对象，在方法中完成Person对象的创建
			public static Person method(){
				Person p = new Student();
				return p;
			}
		}

		
### 10接口作为方法参数与返回值
	* A: 	接口作为方法参数
		接口作为方法参数的情况是很常见的，经常会碰到。当遇到方法参数为接口类型时，那么该方法要传入一个接口实现类对象。如下代码演示。
		//接口
		interface Smoke{
			public abstract void smoking();
		}
		class Student implements Smoke{
			@Override
			public void smoking() {
				System.out.println("课下吸口烟，赛过活神仙");
			}
		}
		//测试类
		public class Test {
			public static void main(String[] args) {
				//通过多态的方式，创建一个Smoke类型的变量，而这个对象实际是Student
				Smoke s = new Student();
				//调用method方法
				method(s);
			}
			
			//定义一个方法method，用来接收一个Smoke类型对象，在方法中调用Smoke对象的show方法
			public static void method(Smoke sm){//接口作为参数
				//通过sm变量调用smoking方法，这时实际调用的是Student对象中的smoking方法
				sm.smoking();
			}
		}

	* B:	接口作为方法返回值
		接口作为方法返回值的情况，在后面的学习中会碰到。当遇到方法返回值是接口类型时，那么该方法需要返回一个接口实现类对象。如下代码演示。

		//接口
		interface Smoke{
			public abstract void smoking();
		}
		class Student implements Smoke{
			@Override
			public void smoking() {
				System.out.println("课下吸口烟，赛过活神仙");
			}
		}
		//测试类
		public class Test {
			public static void main(String[] args) {
				//调用method方法，获取返回的会吸烟的对象
				Smoke s = method();
				//通过s变量调用smoking方法,这时实际调用的是Student对象中的smoking方法
				s.smoking();
			}
			
			//定义一个方法method，用来获取一个具备吸烟功能的对象，并在方法中完成吸烟者的创建
			public static Smoke method(){
				Smoke sm = new Student();
				return sm;
			}
		}

		
## 类练习
### 11星级酒店案例
	* A: 	根据“某五星级酒店，资金雄厚……都有自己的工作要做。”分析出，该题目中包含酒店，可以把它封装成类，多名员工）。

		class 员工 {
		     属性：姓名
		属性：工号
		方法：工作
		}
		class 厨师 extends 员工{}
		class 服务员 extends 员工{}
		class 经理 extends 员工 {
		     属性：奖金
		}

		员工的类型有经理、厨师、服务员，它们有共同的属性（姓名、工号、），经理额外属性（奖金）。

			根据“向酒店中，增加多名员工（其中包含1名经理，1名厨师、2名服务员）”。分析出，要创建一个酒店对象，并添加4名员工到酒店对象的员工集合中。
		酒店员工集合添加新员工： 经理对象
		酒店员工集合添加新员工： 厨师对象
		酒店员工集合添加新员工： 服务员对象
		酒店员工集合添加新员工： 服务员对象

			根据“获取酒店幸运员工”。分析出，从酒店员工集合随机得到一名员工对象。
		1. 从酒店员工集合长度范围内，随机产生一个随机数
		2. 使用该随机数作为集合的索引，返回该索引处对应的员工对象

			根据“酒店开设VIP服务，酒店的厨师与服务员可以提供VIP服务。（厨师做菜加量、服务员给顾客倒酒）”。分析出，这是要增加一个VIP的接口，接口中提供个VIP服务的方法。让厨师与服务员实现该接口。
		interface VIP服务{
		     抽象方法：服务
		}
		class 厨师 extends 员工 implements VIP服务{ 重写服务方法 }
		class 服务员 extends 员工 implements VIP服务{ 重写服务方法 }

	B:
		VIP服务
    public interface VIP {
         public abstract void server(); //服务
    }

	员工

    /*
     * 	员工：
             姓名 String
             工号 String
     */
    public abstract class YuanGong {
        // 成员变量
        private String xingMing;
        private String gongHao;
        // 构造方法
        public YuanGong() {
            super();
        }
        public YuanGong(String xingMing, String gongHao) {
            super();
            this.xingMing = xingMing;
            this.gongHao = gongHao;
        
        }
        // 抽象方法
        public abstract void work();
        
        // getters与setters
        public String getXingMing() {
            return xingMing;
        }
        public void setXingMing(String xingMing) {
            this.xingMing = xingMing;
        }
        public String getGongHao() {
            return gongHao;
        }
        public void setGongHao(String gongHao) {
            this.gongHao = gongHao;
        }
        
    }

	服务员

    /*
    * 定义员工的子类 服务员类
    */
    public class FuWuYuan extends YuanGong implements VIP {
        public FuWuYuan() {
            super();
        }
    
        public FuWuYuan(String xingMing, String gongHao) {
            super(xingMing, gongHao);
        }
        @Override
        public void work() {
            System.out.println("亲，全身心为您服务，记得给好评哦");
        }
        @Override
        public void server() {
            System.out.println("给顾客倒酒");
        }
    }

	经理

     /*
    * 经理在员工的基础上，添加了奖金成员
    */
    public class JingLi extends YuanGong {
        private double jiangJin;
    
        public JingLi() {
            super();
        }
        public JingLi(String xingMing, String gongHao, double jiangJin) {
            super(xingMing, gongHao);
            this.jiangJin = jiangJin;
        }
    
        public double getJiangJin() {
            return jiangJin;
        }
        public void setJiangJin(double jiangJin) {
            this.jiangJin = jiangJin;
        }
    
        @Override
        public void work() {
            System.out.println("哪个员工让顾客不满意，我扣谁钱");
        };
    }

	厨师

    /*
    * 定义员工的子类 厨师类
     */
     public class ChuShi extends YuanGong implements VIP{
	public ChuShi() {
		super();
	}
	public ChuShi(String xingMing, String gongHao) {
		super(xingMing, gongHao);
	}

	@Override
	public void work() {
		System.out.println("我做饭，放心吃吧，包您满意");
	}
	@Override
	public void server() {
		System.out.println("做菜加量加料");
	}
}

###  API 
    api的概述： 就是java替我们写好的一些类，他封装了一些功能，我们仅仅只需要知道如何使用即可

###  Object 
    object的概述：
       A、 object是所有的类父类
       B、 object中的所有方法，子类都能使用（接口不是object的子类）
     
###  Object 类中常用方法
     A、equals()  
        底层调用其实就是== 方法
        == 方法：
           基本数据类： 比较的是内容(值)
           引用数据类型：比较的是内存地址值
      String 的equals比较的是内容  

     B、String toString()
        问题：为什么要重写toString()方法
         
        答：打印时默认会调用toString()方法
         因为toString()方法来源于object中，object中getClass.getName()+"@" +Integer.toHexString(hasCode() ) --->打印就是内存地址值
        很多时候，我们不想看见内存地址值，想看到的是子类的特有属性值，这时就需要重写toString()方法


###  String 
     在String 中认为都是对象，String str = "...";
     所以str 是对象，""也是对象
      String 是一个常量，其本质就是private final 修饰的字符数组     

    String的构造方法:
     new String(byte [] bytes, int offset,int length);
     offset: 数据解锁起始位置
     length:需要解锁的位数
  
    substring(int start ,int end );   包含头，不包含尾。 截取一段字符
    substring(int start);             从某一位到尾
    startsWith(String str)            判断以什么开头
    endsWith(String str)                        判断以什么结尾    
    contains(String str)               判断是否包含
    indexOf（String str）      
    charAt(int index)
    equals()                           注意：要区分大小写
    equalsIgnoreCase                   不区分大小写
    getBytes（）    
    toCharArray()            
    

### StringBuilder && StringBuffer

    1、 StringBuilder 是字符串缓冲对象，底层是一个没有用final修饰的数组，并且长度默认为16,底层是一个"可变数组"

    注意：是底层自动帮我们创建新数组，数组一旦创建，是不可变的

  

------------------------------------------------------------------------------------






###  面试题
    object类有哪些方法
   
    
### 　final
    A、修饰类 ： 不能被继承
    B、修饰方法 ： 不能被重写
    C、修饰变量 ：  基本数据类型： 值不能改变
       * 引用数据类型： 地址值不能改变



###   重写和重载
     重写：子类中出现和父类方法声明一模一样的方法,重写
     重载：本类中出现方法名相同，但参数列表不同，注意：与返回值类型无关


###  封装
    封装好处：
     A、提高了代码的复用性
     B、提高了代码的安全性
     C、隐藏了对象实现的细节，仅仅对外提供方法
 
###  继承
    A、提高了代码的复用性
    B、提高了代码的可维护性
    C、是类和类之间耦合起来了，这是多态的前提
    继承的弊端：
    开发的原则：高内聚，低耦合
    内聚：完成一个功能的能力
    耦合：类和类之间的关系   继承的注意事项：
 
     1、 子类继承父类，只能继承父类中非private修饰的成员变量和方法
     2、 简单说：子类有，父类有，找子类，子类没有，父类有，找父类
         


### 01API概念

	* A:API(Application Programming Interface) 
		* 应用程序编程接口
	* B:Java API
		* 就是Java提供给我们使用的类，这些类将底层的实现封装了起来，
		* 我们不需要关心这些类是如何实现的，只需要学习这些类如何使用。
	* C: 演示查看Object类中的相关方法
	
### 02Object类概述
	* A:Object类概述
		* 类层次结构的根类
		* 所有类都直接或者间接的继承自该类
		* Object中描述的所有方法子类都可以使用
		* 所有类在创建对象的时候，最终找的父类就是Object。
	* B:构造方法
		* public Object()
		* 回想面向对象中为什么说：
			* 子类的构造方法默认访问的是父类的无参构造方法

			
### 03equals方法比较内存地址
	* A:equals方法比较内存地址
		* a: Object类中的equals方法
			* 用于比较两个对象是否相同，Object类中就是使用两个对象的内存地址在比较。
			* Object类中的equals方法内部使用的就是==比较运算符。
			
		* b: 案例代码
		
			public class Person extends Object{
				private String name;
				private int age;
				
				public Person(){}
				
				public Person(String name, int age) {
					this.name = name;
					this.age = age;
				}
				/*
				 * 将父类的equals方法写过来,重写父类的方法
				 * 但是,不改变父类方法的源代码, 方法equals 比较两个对象的内存地址
				 * 				
				 */
				public boolean equals(Object obj){					
					return this == obj;
				}		
				
				public String getName() {
					return name;
				}
				public void setName(String name) {
					this.name = name;
				}
				public int getAge() {
					return age;
				}
				public void setAge(int age) {
					this.age = age;
				}				 
			}
			//测试代码
			public class TestEquals {
				public static void main(String[] args) {
					//Person类继承Object类,继承下来了父类的方法equals
					Person p1 = new Person("李四",20);
					Person p2 = new Person("张三",20);
					
				  
					//Person对象p1,调用父类的方法equals,进行对象的比较
					boolean b = p1.equals(p1);
					System.out.println(b);
					
				}
			}
	

### 04重写equals方法
	* A: 重写equals方法
		* a: 开发中要比较两个对象是否相同，经常会根据对象中的属性值进行比较			
		* b: 在开发经常需要子类重写equals方法根据对象的属性值进行比较。	
		* c: ==号和equals方法的区别
			* ==是一个比较运算符号,既可以比较基本数据类型,也可以比较引用数据类型,基本数据类型比较的是值,引用数据类型比较的是地址值
			* equals方法是一个方法,只能比较引用数据类型,所有的对象都会继承Object类中的方法,如果没有重写Object类中的equals方法,
				equals方法和==号比较引用数据类型无区别,重写后的equals方法比较的是对象中的属性
		* d: 案例代码
			public class Person extends Object{
				private String name;
				private int age;
				
				public Person(){}
				
				public Person(String name, int age) {
					this.name = name;
					this.age = age;
				}
				/*
				 * 重写父类的方法toString()
				 * 没有必要让调用者看到内存地址
				 * 要求: 方法中,返回类中所有成员变量的值
				 */
				public String toString(){
					return name + age;
				}
				
				
				/*
				 * 将父类的equals方法写过来,重写父类的方法
				 * 但是,不改变父类方法的源代码, 方法equals 比较两个对象的内存地址
				 * 
				 * 两个对象,比较地址,没有意义
				 * 比较两个对象的成员变量,age
				 * 两个对象变量age相同,返回true,不同返回false
				 * 
				 * 重写父类的equals,自己定义自己对象的比较方式
				 */
				public boolean equals(Object obj){
					if( this == obj){
						return true;
					}
					
					//对参数obj,非null判断
					if( obj == null){
						return false;
					}
					
					if( obj instanceof Person){
						// 参数obj接受到是Person对象,才能转型
						// 对obj参数进行类型的向下转型,obj转成Person类型
						Person p = (Person)obj;
						return this.age ==  p.age;
					}
					return false;
				}				
				
				public String getName() {
					return name;
				}
				public void setName(String name) {
					this.name = name;
				}
				public int getAge() {
					return age;
				}
				public void setAge(int age) {
					this.age = age;
				}				 
			}
			//测试代码
			public class TestEquals {
				public static void main(String[] args) {
					//Person类继承Object类,继承下来了父类的方法equals
					Person p1 = new Person("李四",20);
					Person p2 = new Person("张三",20);
					
				  
					//Person对象p1,调用父类的方法equals,进行对象的比较
					boolean b = p1.equals(p1);
					System.out.println(b);
					
				}
			}			

### 05重写toString方法
	* A: 重写toString方法
		* a: 为什么要重写toString方法
			* toString方法返回该对象的字符串表示，其实该字符串内容就是对象的类型+@+内存地址值。
			* 由于toString方法返回的结果是内存地址，而在开发中，经常需要按照对象的属性得到相应的字符串表现形式，因此也需要重写它。
			* Object类中的toString的核心代码
				getClass().getName() + "@" + Integer.toHexString(hashCode()) 
			* 由于默认情况下的数据对我们来说没有意义，一般建议重写该方法。
		* b: 案例核心代码(重写Person类中的toString方法)
			/*
			 * 重写父类的方法toString()
			 * 没有必要让调用者看到内存地址
			 * 要求: 方法中,返回类中所有成员变量的值
			 */
			public String toString(){
				return name + age;
			}	
			//Eclipse中自动生成的toString
			@Override
			public String toString() {
				return "Person [name=" + name + ", age=" + age + "]";
			}
			//测试代码
			public class TestToString {
				public static void main(String[] args) {
					//调用Person类的方法toString()
					//输出语句中,写的是一个对象,默认调用对象的toString方法
					Person p = new Person("张三",20);
					String s = p.toString();
					System.out.println(p);
					System.out.println(s);
					/*
					 * System.out.println(p);
					 * System.out.println(p.toString());
					 */
					
					/*Random r = new Random();
					System.out.println(r.toString());
					
					Scanner sc = new Scanner(System.in);
					System.out.println(sc.toString());*/
				}
			}

		
### 06String类的概念和不变性
	* A: String类的概念和不变性
		* a:String类
			* API中的String类的描述，发现String 类代表字符串
			* Java 程序中的所有字符串字面值（如 "abc" ）都作为此类的实例实现。
			* 字符串是常量,在创建之后不能更改
			* 其实就是说一旦这个字符串确定了，那么就会在内存区域中就生成了这个字符串。字符串本身不能改变，但str变量中记录的地址值是可以改变的。
			* 源码分析,String类底层采用的是字符数组:
				private final char value[]
				private 修饰说明value只能在String类内部使用,而且又没有提供get方法,所以外部无法获取value数组,就无法改变数组中元素的值
				final修饰说明value是常量,一旦创建,就不能被改变,value一旦被初始化成某个数组,将永远指向这个数组,不可能再指向其它的数组了
				
		* b: 案例代码
			/*
			 *   String类特点:
			 *     一切都是对象,字符串事物 "" 也是对象
			 *     类是描述事物,String类,描述字符串对象的类
			 *     所有的 "" 都是String类的对象
			 *     
			 *     字符串是一个常量,一旦创建,不能改变
			 */
			public class StringDemo {
				public static void main(String[] args) {
					//引用变量str执行内存变化
					//定义好的字符串对象,不变
					String str = "itcast";
					System.out.println(str);
					str = "itheima";
					System.out.println(str);
					
					
				}
			}
			
### 07String类创建方式和比较
	* A: String类创建方式和比较
		* a: 创建对象的数量比较
			* String s3 = "abc";
				* 在内存中只有一个对象。这个对象在字符串常量池中
			* String s4 = new String("abc");
				* 在内存中有两个对象。一个new的对象在堆中，一个字符串本身对象，在字符串常量池中
		* b: 案例代码
			public class StringDemo2 {
				public static void main(String[] args) {
					//字符串定义方式2个, 直接=  使用String类的构造方法
					String str1 = new String("abc");
					String str2 = "abc";
					System.out.println(str1);
					System.out.println(str2);
					
					System.out.println(str1==str2);//引用数据类型,比较对象的地址 false
					System.out.println(str1.equals(str2));//true
				}
			}
						
### 08String类构造方法
	* A: String类构造方法
		* a: 常见构造方法
			* public String():空构造
			* public String(byte[] bytes):把字节数组转成字符串
			* public String(byte[] bytes,int index,int length):把字节数组的一部分转成字符串			
			* public String(String original):把字符串常量值转成字符串
		* b: 案例代码
			public class StringDemo3 {
				public static void main(String[] args) {
					function_1();
				}
				/*
				 *  定义方法,String类的构造方法
				 *  String(byte[] bytes)  传递字节数组
				 *  字节数组转成字符串
				 *  通过使用平台的默认字符集解码指定的 byte 数组，构造一个新的 String。
				 *  平台 : 机器操作系统
				 *  默认字符集: 操作系统中的默认编码表, 默认编码表GBK
				 *  将字节数组中的每个字节,查询了编码表,得到的结果
				 *  字节是负数,汉字的字节编码就是负数, 默认编码表 ,一个汉字采用2个字节表示
				 *  
				 *  String(byte[] bytes, int offset, int length) 传递字节数组
				 *  字节数组的一部分转成字符串
				 *  offset 数组的起始的索引
				 *  length 个数,转几个   , 不是结束的索引
				 */
				public static void function(){
					byte[] bytes = {97,98,99,100};
					//调用String类的构造方法,传递字节数组
					String s = new String(bytes);
					System.out.println(s);
					
					byte[] bytes1 ={65,66,67,68,69};
					//调用String构造方法,传递数组,传递2个int值
					String s1 = new String(bytes1,1,3);
					System.out.println(s1);
				}
			}


### 09String类构造方法_2
	* A: String类构造方法
		* a: 常见构造方法
			* public String(char[] value):把字符数组转成字符串
			* public String(char[] value,int index,int count):把字符数组的一部分转成字符串
	* B: 案例代码
		 /*
		  *  String类构造方法
		  *  String类的构造方法,重载形式
		  * 
		  */
		public class StringDemo3 {
			public static void main(String[] args) {
				function_1();
			}
			/*
			 * String(char[] value) 传递字符数组
			 * 将字符数组,转成字符串, 字符数组的参数,不查询编码表
			 * 
			 * String(char[] value, int offset, int count) 传递字符数组
			 * 将字符数组的一部分转成字符串
			 * offset  数组开始索引
			 * count   个数
			 */
			public static void function_1(){
				char[] ch = {'a','b','c','d','e','f'};
				//调用String构造方法,传递字符数组
				String s = new String(ch);
				System.out.println(s);
				
				String s1 = new String(ch,1,4);
				System.out.println(s1);
			}
		}




		
### 10String类的其他方法			
	* A：String类的其他方法
		* a: 方法介绍
			* int length(): 返回字符串的长度
			* String substring(int beginIndex,int endIndex): 获取字符串的一部分
			* String substring(int beginIndex): 获取字符串的一部分
			* boolean startsWith(String prefix): 判断一个字符串是不是另一个字符串的前缀,开头
			* boolean endsWith(String prefix): 判断一个字符串是不是另一个字符串的后缀,结尾
			* boolean contains (String s): 判断一个字符串中,是否包含另一个字符串
			* int indexOf(char ch):  查找一个字符,在字符串中第一次出现的索引,被查找的字符不存在,返回-1
			* byte[] getBytes(): 将字符串转成字节数组,此功能和String构造方法相反,byte数组相关的功能,查询编码表
			* char[] toCharArray(): 将字符串转成字符数组,功能和构造方法相反
			* boolean equals(Object obj): 方法传递字符串,判断字符串中的字符是否完全相同,如果完全相同返回true
			* boolean equalsIgnoreCase(String s): 传递字符串,判断字符串中的字符是否相同,忽略大小写			
			
		* b: 案例代码
		
			public class StringDemo4 {
				public static void main(String[] args) {
					function_9();
				}
				/*
				 *  boolean equals(Object obj)
				 *  方法传递字符串,判断字符串中的字符是否完全相同,如果完全相同返回true
				 *  
				 *  boolean equalsIgnoreCase(String s)
				 *  传递字符串,判断字符串中的字符是否相同,忽略大小写
				 */
				public static void function_9(){
					String str1 = "Abc";
					String str2 = "abc";
					//分别调用equals和equalsIgnoreCase
					boolean b1 = str1.equals(str2);
					boolean b2 = str1.equalsIgnoreCase(str2);
					System.out.println(b1);
					System.out.println(b2);
				}
				
				/*
				 * char[] toCharArray() 将字符串转成字符数组
				 * 功能和构造方法相反
				 */
				public static void function_8(){
					String str = "itcast";
					//调用String类的方法toCharArray()
					char[] ch = str.toCharArray();
					for(int i = 0 ; i < ch.length ; i++){
						System.out.println(ch[i]);
					}
				}
				
				/*
				 *  byte[] getBytes() 将字符串转成字节数组
				 *  此功能和String构造方法相反
				 *  byte数组相关的功能,查询编码表
				 */
				public static void function_7(){
					String str = "abc";
					//调用String类方法getBytes字符串转成字节数组
					byte[] bytes = str.getBytes();
					for(int i = 0 ; i < bytes.length ; i++){
						System.out.println(bytes[i]);
					}
				}
				
				/*
				 *  int indexOf(char ch)
				 *  查找一个字符,在字符串中第一次出现的索引
				 *  被查找的字符不存在,返回-1
				 */
				public static void function_6(){
					String str = "itcast.cn";
					//调用String类的方法indexOf
					int index = str.indexOf('x');
					System.out.println(index);
				}
				
				/*
				 *  boolean contains (String s)
				 *  判断一个字符串中,是否包含另一个字符串
				 */
				public static void function_5(){
					String str = "itcast.cn";
					//调用String类的方法contains
					boolean b =str.contains("ac");
					System.out.println(b);
				}
				
				/*
				 * boolean endsWith(String prefix)
				 * 判断一个字符串是不是另一个字符串的后缀,结尾
				 * Demo.java
				 *     .java
				 */
				public static void function_4(){
					String str = "Demo.java";
					//调用String类方法endsWith
					boolean b = str.endsWith(".java");
					System.out.println(b);
				}
				
				/*
				 * boolean startsWith(String prefix)  
				 * 判断一个字符串是不是另一个字符串的前缀,开头
				 * howareyou
				 * hOw
				 */
				  public static void function_3(){
					  String str = "howareyou";
					  //调用String类的方法startsWith
					  boolean b = str.startsWith("hOw");
					  System.out.println(b);
				  }
				
				/*
				 *  String substring(int beginIndex,int endIndex) 获取字符串的一部分
				 *  返回新的字符串
				 *  包含头,不包含尾巴
				 *  
				 *  String substring(int beginIndex)获取字符串的一部分
				 *  包含头,后面的字符全要
				 */
				public static void function_2(){
					String str = "howareyou";
					//调用String类方法substring获取字符串一部分
					str= str.substring(1, 5);
					System.out.println(str);
					
					String str2 = "HelloWorld";
					str2 = str2.substring(1);
					System.out.println(str2);
				}
				
				/*
				 *  int length() 返回字符串的长度
				 *  包含多少个字符
				 */
				public static void function(){
					String str = "cfxdf#$REFewfrt54GT";
					//调用String类方法length,获取字符串长度
					int length = str.length();
					System.out.println(length);
				}
			}
				
### 11String类练习
	* A: 获取指定字符串中，大写字母、小写字母、数字的个数
		* a: 题目分析
			* 为了统计大写字母、小写字母、数字的个数。创建3个计数的变量。
			* 为了获取到字符串中的每个字符，进行字符串的遍历，得到每个字符。
			* 对得到的字符进行判断，如果该字符为大写字母，则大写字母个数+1；如果该字符为小写字母，则小写字母个数+1；如果该字符为数字，则数字个数+1。
			* 显示大写字母、小写字母、数字的个数

		* b: 解题步骤
			* 略
		* 案例代码
			public class StringTest {
				public static void main(String[] args) {
					getCount("A%A3eBr1FFy");					
				}
				
				/*
				 * 获取指定字符串中，大写字母、小写字母、数字的个数。
				 * 思想:
				 *   1. 计数器,就是int变量,满足一个条件 ++
				 *   2. 遍历字符串, 长度方法length() + charAt() 遍历
				 *   3. 字符判断是大写,是小写,还是数字
				 */
				public static void getCount(String str){
					//定义三个变量,计数
					int upper = 0;
					int lower = 0;
					int digit = 0;
					//对字符串遍历
					for(int i = 0 ; i < str.length() ; i++){
						//String方法charAt,索引,获取字符
						char c = str.charAt(i);
						//利用编码表 65-90  97-122  48-57
						if(c >='A' && c <=90){
							upper++;
						}else if( c >= 97 && c <= 122){
							lower++;
						}else if( c >= 48 && c <='9'){
							digit++;
						}
					}
					System.out.println(upper);
					System.out.println(lower);
					System.out.println(digit);
				}
			}

### 12String类练习_2
	* A: 将字符串中，第一个字母转换成大写，其他字母转换成小写，并打印改变后的字符串。
		* a: 题目分析
			* 把字符串分为两个部分，第一部分为字符串中第一个字母，第二部分为剩下的字符串。
			* 把第一部分字符串转换成大写字母，把第二部分字符串转换成小写字母
			* 把两部分字符串连接在一起，得到一个完整的字符串
		* b: 解题步骤
			* 略
		* C: 案例代码
			public class StringTest {
				public static void main(String[] args) {
					
					System.out.println(toConvert("aBc5%4dEF"));
					
				}
				
				/*
				 *  将字符串的首字母转成大写,其他内容转成小写
				 *  思想:
				 *    获取首字母, charAt(0)  substring(0,1)
				 *    转成大写 toUpperCase()
				 *    
				 *    获取剩余字符串, substring(1)  toLowerCase()
				 */
				public static String toConvert(String str){
					//定义变量,保存首字母,和剩余字符
					String first = str.substring(0,1);
					String after = str.substring(1);
					//调用String类方法,大写,小写转换
					first = first.toUpperCase();
					after = after.toLowerCase();
					return first+after;
				}
			}



### 13String类练习_3
	* A: 查询大字符串中，出现指定小字符串的次数
		* a: 题目分析
			* 在大串中，查找小串出现的位置，出现了就次数+1
			* 在上次小串出现位置的后面继续查找，需要更改大串的内容为上次未查询到的字符串。
			* 回到第一步，继续查找小串出现的位置，直到大串中查询不到小串为止
		* b: 解题步骤
			* 略
		* C: 案例代码	
			package cn.itcast.demo02;

			public class StringTest {
				public static void main(String[] args) {		
					System.out.println(getStringCount("hellojava,nijavahaojava,javazhenbang", "java"));
				}
				/*
				 *  获取一个字符串中,另一个字符串出现的次数
				 *  思想:
				 *    1. indexOf到字符串中到第一次出现的索引
				 *    2. 找到的索引+被找字符串长度,截取字符串
				 *    3. 计数器++
				 */
				public static int getStringCount(String str, String key){
					//定义计数器
					int count = 0;
					//定义变量,保存indexOf查找后的索引的结果
					int index = 0;
					//开始循环找,条件,indexOf==-1 字符串没有了
					while(( index = str.indexOf(key) )!= -1){
						count++;
						//获取到的索引,和字符串长度求和,截取字符串
						str = str.substring(index+key.length());
					}
					return count;
				}
			}


======================================================================第三节课开始=========================================================
				
### 14StringBuffer特点可变字符数组
	* A:StringBuffer类概述
		* 通过JDK提供的API，查看StringBuffer类的说明
		* 线程安全的可变字符序列 
		* 底层采用字符数组实现,初始容量为16
	* B:StringBuffer和String的区别
		* String是一个不可变的字符序列
		* StringBuffer是一个可变的字符序列

### 15StringBuffer类的方法
	* A: StringBuffer类的方法
		* a: 方法介绍
			* StringBuffer append(), 将任意类型的数据,添加缓冲区
				*  append 返回值,写return this
				*  调用者是谁,返回值就是谁
			* delete(int start,int end): 删除缓冲区中字符
				*  开始索引包含,结尾索引不包含
			* insert(int index, 任意类型): 将任意类型数据,插入到缓冲区的指定索引上
			* replace(int start,int end, String str): 将指定的索引范围内的所有字符,替换成新的字符串
			* reverse(): 将缓冲区中的字符反转
			* String toString(): 继承Object,重写toString()
				*   将缓冲区中的所有字符,变成字符串
		* b: 案例代码
			public class StringBufferDemo {
				public static void main(String[] args) {
					function_5();
				}
				/*
				 *  StringBuffer类的方法
				 *   String toString() 继承Object,重写toString()
				 *   将缓冲区中的所有字符,变成字符串
				 */
				public static void function_5(){
					StringBuffer buffer = new StringBuffer();
					buffer.append("abcdef");
					buffer.append(12345);
					
					//将可变的字符串缓冲区对象,变成了不可变String对象
					String s = buffer.toString();
					System.out.println(s);
				}
				
				/*
				 *  StringBuffer类的方法
				 *    reverse() 将缓冲区中的字符反转
				 */
				public static void function_4(){
					StringBuffer buffer = new StringBuffer();
					buffer.append("abcdef");
					
					buffer.reverse();
					
					System.out.println(buffer);
				}
				
				/*
				 *  StringBuffer类方法
				 *    replace(int start,int end, String str)
				 *    将指定的索引范围内的所有字符,替换成新的字符串
				 */
				public static void function_3(){
					StringBuffer buffer = new StringBuffer();
					buffer.append("abcdef");
					
					buffer.replace(1, 4, "Q");
					
					System.out.println(buffer);
				}
				
				/*
				 *  StringBuffer类方法 insert
				 *    insert(int index, 任意类型)
				 *  将任意类型数据,插入到缓冲区的指定索引上
				 */
				 public static void function_2(){
					 StringBuffer buffer = new StringBuffer();
					 buffer.append("abcdef");	 
					 
					 buffer.insert(3, 9.5);
					 System.out.println(buffer);
				 }
				
				/*
				 * StringBuffer类方法
				 *   delete(int start,int end) 删除缓冲区中字符
				 *   开始索引包含,结尾索引不包含
				 */
				public static void function_1(){
					StringBuffer buffer = new StringBuffer();
					buffer.append("abcdef");
					
					buffer.delete(1,5);
					System.out.println(buffer);
				}
				
				/*
				 *  StringBuffer类方法
				 *   StringBuffer append, 将任意类型的数据,添加缓冲区
				 *   append 返回值,写return this
				 *   调用者是谁,返回值就是谁
				 */
				public static void function(){
					StringBuffer buffer = new StringBuffer();
					//调用StringBuffer方法append向缓冲区追加内容
					buffer.append(6).append(false).append('a').append(1.5);
					System.out.println(buffer);
				}
			}

		
### 16StringBuilder类
	* A:StringBuilder的概述
		* 通过查看API了解一下StringBuilder类
	* B:面试题
		* String,StringBuffer,StringBuilder的区别
			* StringBuffer和StringBuilder的区别
				* StringBuffer是jdk1.0版本的,是线程安全的,效率低
				* StringBuilder是jdk1.5版本的,是线程不安全的,效率高

			* String和StringBuffer,StringBuilder的区别
				* String是一个不可变的字符序列
				* StringBuffer,StringBuilder是可变的字符序列
	


		
### 17StringBuffer类案例拼接数组
	* A: StringBuffer类案例拼接数组
		* a: 题目分析
			* 定义StringBuffer对象
			* 遍历数组,按照格式要求拼接处新的字符串,追加到StringBuffer容器中
			* 将StringBuffer中的内容以String的形式返回
		* b: 解题步骤
			* 略
		* C: 案例代码	
			public class StringBufferTest {
				public static void main(String[] args) {
					int[] arr = {4,1,4,56,7,8,76};
					System.out.println(toString(arr));
				}
			   /*
				* int[] arr = {34,12,89,68};将一个int[]中元素转成字符串 
				* 格式 [34,12,89,68]
				* String s = "["
				* 数组遍历
				*   s+= arr[i];
				*  s+"]"
				*  StringBuffer实现,节约内存空间, String + 在缓冲区中,append方法
				*/
				public static String toString(int[] arr){
					//创建字符串缓冲区
					StringBuffer buffer = new StringBuffer();
					buffer.append("[");
					//数组遍历
					for(int i = 0 ; i < arr.length;i++){
						//判断是不是数组的最后一个元素
						if(i == arr.length-1){
							buffer.append(arr[i]).append("]");
						}else{
							buffer.append(arr[i]).append(",");
						}
					}
					return buffer.toString();
				}
			}
### 18总结
* 把今天的知识点总结一遍。


### 01正则表达式的概念和作用
	* A: 正则表达式的概念和作用
		* a: 正则表达式的概述
			* 正则表达式也是一个字符串，用来定义匹配规则，在Pattern类中有简单的规则定义。
			  可以结合字符串类的方法使用。
			* 简单记：正则表达式是具有特殊含义的字符串。
		* b: 正则表达式的作用
		* 比如注册邮箱,邮箱有用户名和密码,一般会对其限制长度,这个限制长度的事情就是正则表达式做的

		
### 02正则表达式语法规则
	* A: 正则表达式语法规则
		* a: 字符
			* x  代表的是字符x
			* \\ 代表的是反斜线字符'\'
			* \t 代表的是制表符
			* \n 代表的是换行符
			* \r 代表的是回车符
		* b: 字符类
			* [abc]    a、b 或 c（简单类）
			* [^abc]   任何字符，除了 a、b 或 c（否定）
			* [a-zA-Z] a到 z 或 A到 Z，两头的字母包括在内（范围） 
			* [0-9]    0到9的字符都包括
			* [a-zA-Z_0-9] 代表的字母或者数字或者下划线(即单词字符)
		* c: 预定义字符类
			* . 任何字符。
			* \d 数字：[0-9]
			* \w 单词字符：[a-zA-Z_0-9]如"com.itheima.tests"/finish
		* d: 边界匹配器
			* ^  代表的是行的开头
			* $  代表的是行的结尾
			* \b 代表的是单词边界
		* e: 数量词
			* X?     X，一次或一次也没有
			* X*     X，零次或多次
			* X+     X，一次或多次
			* X{n}   X，恰好 n 次 
			* X{n,}  X，至少 n 次 
			* X{n,m} X，至少 n 次，但是不超过 m 次


### 03正则表达式练习和相关的String类方法
	* A: 正则表达式练习和相关的String类方法
		* a: boolean matches(String 正则的规则)
			* "abc".matches("[a]")  
			* 匹配成功返回true
		* b: String[] split(String 正则的规则)
			* "abc".split("a")  
			* 使用规则将字符串进行切割
		* c: String replaceAll( String 正则规则,String 字符串)
			* "abc0123".repalceAll("[\\d]","#")	
			* 按照正则的规则,替换字符串
	
	
### 04正则表达式匹配练习
	* A: 正则表达式匹配练习
		* a: 案例代码
			public class RegexDemo {
				public static void main(String[] args) {
					checkTel();
				}
				
				
				/*
				 *  检查手机号码是否合法
				 *  1开头 可以是34578  0-9 位数固定11位
				 */
				public static void checkTel(){
					String telNumber = "1335128005";
					//String类的方法matches
					boolean b = telNumber.matches("1[34857][\\d]{9}");
					System.out.println(b);
				}
				
				/*
				 *  检查QQ号码是否合法
				 *  0不能开头,全数字, 位数5,10位
				 *  123456 
				 *  \\d  \\D匹配不是数字
				 */
				public static void checkQQ(){
					String QQ = "123456";
					//检查QQ号码和规则是否匹配,String类的方法matches
					boolean b = QQ.matches("[1-9][\\d]{4,9}");
					System.out.println(b);
				}
			}
	

### 05正则表达式切割练习
	* A: 正则表达式切割练习
		* a: 案例代码
			public class RegexDemo1 {
				public static void main(String[] args) {
					split_1();
					split_2();
					split_3();

				}
				
				/*
				 * String类方法split对字符串进行切割
				 * 192.168.105.27 按照 点切割字符串
				 */
				public static void split_3(){
					String ip = "192.168.105.27";
					String[] strArr = ip.split("\\.");
					System.out.println("数组的长度"+strArr.length);
					for(int i = 0 ; i < strArr.length ; i++){
						System.out.println(strArr[i]);
					}
				}
				
				/*
				 * String类方法split对字符串进行切割
				 * 18 22 40 65 按照空格切割字符串
				 */
				public static void split_2(){
					String str = "18    22     40          65";
					String[] strArr = str.split(" +");
					System.out.println("数组的长度"+strArr.length);
					for(int i = 0 ; i < strArr.length ; i++){
						System.out.println(strArr[i]);
					}
				}
				
				/*
				 *  String类方法split对字符串进行切割
				 *  12-25-36-98  按照-对字符串进行切割
				 */
				public static void split_1(){
					String str = "12-25-36-98";
					//按照-对字符串进行切割,String类方法split
					String[] strArr = str.split("-");
					System.out.println("数组的长度"+strArr.length);
					for(int i = 0 ; i < strArr.length ; i++){
						System.out.println(strArr[i]);
					}
				}
			}		

			
### 06正则表达式替换练习
	* A: 正则表达式替换练习
		* a: 案例代码
			public class RegexDemo1 {
				public static void main(String[] args) {
					replaceAll_1();
				}
				
				/*
				 * "Hello12345World6789012"将所有数字替换掉
				 * String类方法replaceAll(正则规则,替换后的新字符串)
				 */
				public static void replaceAll_1(){
					String str = "Hello12345World6789012";
					str = str.replaceAll("[\\d]+", "#");
					System.out.println(str);
				}
			}
			

### 07正则表达式邮箱地址验证
	* A: 正则表达式邮箱地址验证
		* a: 案例代码
			public class RegexDemo2 {
				public static void main(String[] args) {
					checkMail();
				}
				/*
				 *  检查邮件地址是否合法
				 *  规则:
				 *   1234567@qq.com
				 *   mym_ail@sina.com
				 *   nimail@163.com
				 *   wodemail@yahoo.com.cn    
				 *   
				 *   @: 前  数字字母_ 个数不能少于1个
				 *   @: 后  数字字母     个数不能少于1个
				 *   .: 后面 字母 
				 *     
				 */
				public static void checkMail(){
					String email ="abc123@sina.com";
					boolean b = email.matches("[a-zA-Z0-9_]+@[0-9a-z]+(\\.[a-z]+)+");
					System.out.println(b);
				}
			}
				
### 08毫秒值概念 
	* A: 毫秒值概念
		* a: 时间和日期类
			* java.util.Date
		* b: 毫秒概念
			* 1000毫秒=1秒
		* c: 毫秒的0点
			 * System.currentTimeMillis() 返回值long类型参数
			 * 获取当前日期的毫秒值   3742769374405    
			 * 时间原点; 公元1970年1月1日,午夜0:00:00 英国格林威治  毫秒值就是0
			 * 时间2088年8月8日    
			 * 时间和日期的计算，必须依赖毫秒值


### 09Date类的构造方法
	* A: Date类的构造方法
		* a: 空参构造
			* public Date()
		* b: 带参构造
			* public Date(long times)
	
		
==============================第二阶段====================================		


		
### 10Date类的get和set方法			
	* A：Date类的get和set方法
		* public long getTime()	
			* 将当前的日期对象，转为对应的毫秒值
		* public void setTime(long times);
			* 根据给定的毫秒值，生成对应的日期对象


### 11日期格式化SimpleDateFormat
	* A: 日期格式化SimpleDateFormat
		* a: 对日期进行格式化(自定义)
			* 对日期格式化的类 java.text.DateFormat 抽象类, 普通方法,也有抽象的方法
			* 实际使用是子类 java.text.SimpleDateFormat 可以使用父类普通方法,重写了抽象方法
		* b: 对日期进行格式化的步骤
			* 1: 创建SimpleDateFormat对象
				* 在类构造方法中,写入字符串的日期格式 (自己定义)
			* 2: SimpleDateFormat调用方法format对日期进行格式化
				* public String format(Date date) 传递日期对象,返回字符串
				* 日期模式:
	 			* yyyy    年份
	 			* MM      月份
				* dd      月中的天数
				* HH       0-23小时
				* mm      小时中的分钟
	 			* ss      秒
	 			* yyyy年MM月dd日 HH点mm分钟ss秒  汉字修改,: -  字母表示的每个字段不可以随便写

				
### 12字符串转成日期对象
	* A: 字符串转成日期对象
		* a: 使用步骤
			* 1: 创建SimpleDateFormat的对象
				* 构造方法中,指定日期模式
			* 2: 子类对象,调用方法 parse 传递String,返回Date
				* 注意: 时间和日期的模式yyyy-MM-dd, 必须和字符串中的时间日期匹配


### 13Calendar类_1
	* A: Calendar类_1
		* a: 日历类(抽象类)
			* java.util.Calendar
		* b: 创建对象
			* Calendar类写了静态方法 getInstance() 直接返回了子类的对象
			* 不需要直接new子类的对象,通过静态方法直接获取


### 14Calendar类_2
	* A: Calendar类_2
		* a: 成员方法
			* getTime() 把日历对象,转成Date日期对象
			* get(日历字段) 获取指定日历字段的值
		* b: 代码演示
			Calendar c = Calendar.getInstance();
			// 获取年份
			int year = c.get(Calendar.YEAR);
			// 获取月份
			int month = c.get(Calendar.MONTH) + 1;
			// 获取天数
			int day = c.get(Calendar.DAY_OF_MONTH);
			System.out.println(year + "年" + month + "月" + day + "日");
			
			
### 15Calendar类_3
	* A: Calendar类_3
		* a: 成员方法
			* set(int field,int value)  设置指定的时间
		* b: 代码演示
			/*
			 * Calendar类的set方法 设置日历 set(int field,int value) field 设置的是哪个日历字段 value
			 * 设置后的具体数值
			 * 
			 * set(int year,int month,int day) 传递3个整数的年,月,日
			 */
			public static void function_1() {
				Calendar c = Calendar.getInstance();
				// 设置,月份,设置到10月分
				// c.set(Calendar.MONTH, 9);
		
				// 设置年,月,日
				c.set(2099, 4, 1);
		
				// 获取年份
				int year = c.get(Calendar.YEAR);
				// 获取月份
				int month = c.get(Calendar.MONTH) + 1;
				// 获取天数
				int day = c.get(Calendar.DAY_OF_MONTH);
				System.out.println(year + "年" + month + "月" + day + "日");
			}
		

### 16Calendar类_4
	* A: Calendar类_4
		* a: 成员方法
			* add(int field, int value) 进行整数的偏移
			* int get(int field) 获取指定字段的值
		* b: 案例演示
			/*
			 * Calendar类方法add 日历的偏移量,
			 * 可以指定一个日历中的字段,
			 * 进行整数的偏移 add(int field, int value)
			 */
			public static void function_2() {
				Calendar c = Calendar.getInstance();
				// 让日历中的天数,向后偏移280天
				c.add(Calendar.DAY_OF_MONTH, -280);
				// 获取年份
				int year = c.get(Calendar.YEAR);
				// 获取月份
				int month = c.get(Calendar.MONTH) + 1;
				// 获取天数
				int day = c.get(Calendar.DAY_OF_MONTH);
				System.out.println(year + "年" + month + "月" + day + "日");
			}


### 17日期练习_活了多少天
	* A: 日期练习_活了多少天
		* a: 案例代码
			/*
			 *  计算活了多少天
			 *   生日  今天的日期
			 *   两个日期变成毫秒值,减法
			 */
			public static void function() throws Exception {
				System.out.println("请输入出生日期 格式 YYYY-MM-dd");
				//获取出生日期,键盘输入
				String birthdayString = new Scanner(System.in).next();
				//将字符串日期,转成Date对象
				//创建SimpleDateFormat对象,写日期模式
				SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd");
				//调用方法parse,字符串转成日期对象
				Date birthdayDate = sdf.parse(birthdayString);
				
				//获取今天的日期对象
				Date todayDate = new Date();
				
				//将两个日期转成毫秒值,Date类的方法getTime
				long birthdaySecond = birthdayDate.getTime();
				long todaySecond = todayDate.getTime();
				long secone = todaySecond-birthdaySecond;
				
				if(secone < 0){
					System.out.println("还没出生呢");
				}
				else{
				System.out.println(secone/1000/60/60/24);
				}
				
			}


### 18日期练习_闰年计算
	* A: 日期练习_闰年计算
		* a: 案例代码
			/*
			 *  闰年计算
			 *  2000 3000
			 *  高级的算法: 日历设置到指定年份的3月1日,add向前偏移1天,获取天数,29闰年
			 */
			public static void function_1(){
				Calendar c = Calendar.getInstance();
				//将日历,设置到指定年的3月1日
				c.set(2088, 2, 1);
				//日历add方法,向前偏移1天
				c.add(Calendar.DAY_OF_MONTH, -1);
				//get方法获取天数
				int day = c.get(Calendar.DAY_OF_MONTH);
				System.out.println(day);
			}


## 基本数据包装类

### 01基本数据类型对象包装类概述
	 *A:基本数据类型对象包装类概述
	   *a.基本类型包装类的产生
           在实际程序使用中，程序界面上用户输入的数据都是以字符串类型进行存储的。而程序开发中，我们需要把字符串数据，根据需求转换成指定的基本数据类型，如年龄需要转换成int类型，考试成绩需要转换成double类型等
       *b.八种基本类型对应的包装类
           char    Character
           int     Integer
           byte    Byte
           short   Short
           long    Long
           float   Float
           double  Double
           boolean Boolean

### 02Integer类parseInt方法
	   *A:Integer类parseInt方法:
	    *a:parseInt()
		    int i = Integer.parseInt("12");
		    System.out.println(i/2);//6
		 
		*b:parseInt(String s, int radix)
		    /*
		 	 * Integer类静态方法parseInt(String s, int radix)
		 	 * radix基数,进制
		 	 * "110",2 含义 前面的数字是二进制的,但是方法parseInt运行结果都是十进制
		 	 *  指定进制的字符串转换为十进制的整数
		 	 */
		 	public static void function_1(){
		 		int i = Integer.parseInt("110", 2);
		 		System.out.println(i);
		 	}
### 03Integer类int转成字符串 
    *A:Integer类int转成字符串:
       *a:使用+与字符串拼接
            int i = 3;
          	String s = i+"";
          	System.out.println(s+1);//"31"
      
       *b:toString(int ,int 进制),任意进制整数转成任意进制的字符串 (了解)
          	String s1 = Integer.toString(5,2);
          	System.out.println(s1);

### 04Integer类构造方法
	 *A:Integer类构造方法
	    /*
	     *  Integer类构造方法
	     *   Integer (String s)
	     *   将数字格式的字符串,传递到Integer类的构造方法中
	     *   创建Integer对象,包装的是一个字符串
	     *   将构造方法中的字符串,转成基本数据类型,调用方法,非静态的, intValue()
	     */
	    public static void function_3(){
	    	Integer in = new Integer("100");
	    	int i = in.intValue();
	    	System.out.println(--i);//99
	    }


### 05Integer类其他方法
   *A:Integer类其他方法
   
	     /*
		 * Integer类的3个静态方法
		 * 做进制的转换
		 * 十进制转成二进制  toBinarString(int)
		 * 十进制转成八进制  toOctalString(int)
		 * 十进制转成十六进制 toHexString(int)
		 * 三个方法,返回值都是以String形式出现
		 */
	      a:十进制转二,八,十六进制
	          public static void function_1(){
	        		System.out.println(Integer.toBinaryString(99));
	        		System.out.println(Integer.toOctalString(99));
	        		System.out.println(Integer.toHexString(999));
	          }
	      b:获取int的最大值和最小值
	      /*
	       *   Integer类的静态成员变量
	       *   MAX_VALUE
	       *   MIN_VALUE
	       */
	      public static void function(){
	      	System.out.println(Integer.MAX_VALUE);
	      	System.out.println(Integer.MIN_VALUE);
	      }
 
### 06自动装箱和自动拆箱 
  *A:自动装箱与自动拆箱:
  
    //JDK1.5新特性
	//自动装箱,拆箱的 好处: 基本类型和引用类直接运算
    //自动装箱:使用Integer.valueOf(整数值)返回一个封装了该整数值的Integer对象
    //自动拆箱:使用Integer对象.intValue()返回Integer对象中封装的整数值
	public static void function(){
		//引用类型 , 引用变量一定指向对象
		//自动装箱, 基本数据类型1, 直接变成了对象
		
		Integer in = 1; // Integer in = new Integer(1)
		//in 是引用类型,不能和基本类型运算, 自动拆箱,引用类型in,转换基本类型
		
		//in+1  ==> in.inValue()+1 = 2    
		//in = 2    自动装箱
		in = in + 1;
		
		System.out.println(in);
		
	}
      

### 07自动装箱和自动拆箱练习题 
   *A:自动装箱与自动拆箱:
   
	    Integer i = new Integer(1);
	 	Integer j = new Integer(1);
	 	System.out.println(i==j);// false 对象地址
	 	System.out.println(i.equals(j));// true  继承Object重写equals,比较的对象数据
	 	
	 	System.out.println("===================");
	 	
	 	Integer a = 500;//Integer integer=Integer.valueOf(500)
	 	                //integer=new Integer(500);
	 	Integer b = 500;
	 	System.out.println(a==b);//false
	 	System.out.println(a.equals(b));//true
	 	
	 	System.out.println("===================");
	 	
	 	
	 	//数据在byte(-128~127)范围内,JVM不会从新new对象
	 	Integer aa = 127; // Integer aa = new Integer(127)
	 	Integer bb = 127; // Integer bb = aa;
	 	System.out.println(aa==bb); //true
	 	System.out.println(aa.equals(bb));//true
       
    
### 08System类方法currentTimeMillis 
   *A:System类方法currentTimeMillis():用于计算程序的执行时间
   
        /*
      	 *  获取系统当前毫秒值
      	 *  static long currentTimeMillis()
      	 *  对程序执行时间测试
      	 */
      	public static void function(){
      		long start = System.currentTimeMillis();//当前时间x-1970年1月1日零时零分零秒
      		for(int i = 0 ; i < 10000; i++){
      			System.out.println(i);
      		}
      		long end = System.currentTimeMillis();//当前时间y-1970年1月1日零时零分零秒
      		System.out.println(end - start);//当前时间y-当前时间x 
      	}
 
### 09System类方法exit 
     *A:System类方法exit()方法
		     /*
		 	 *  退出虚拟机,所有程序全停止
		 	 *  static void exit(0)
		 	 */
		 	public static void function_1(){
		 		while(true){
		 			System.out.println("hello");
		 			System.exit(0);//该方法会在以后的finally代码块中使用(讲到再说)
		 		}
		 	}
### 10System类方法gc 
   A:System类方法gc
   
        public class Person {
        	public void finalize(){
        		System.out.println("垃圾收取了");
        	}
        }

        /*
     	 *  JVM在内存中,收取对象的垃圾
     	 *  当没有更多引用指向该对象时,会自动调用垃圾回收机制回收堆中的对象
     	 *  同时调用回收对象所属类的finalize方法()
     	 *  static void gc()
     	 */
     	public static void function_2(){
     		new Person();
     		new Person();
     		new Person();
     		new Person();
     		new Person();
     		new Person();
     		new Person();
     		new Person();
     		System.gc();
     	}

### 11System类方法getProperties 
  A:System类方法getProperties(了解)
  
     /*
      *  获取当前操作系统的属性:例如操作系统名称,
      *  static Properties getProperties() 
      */
     public static void function_3(){
     	System.out.println( System.getProperties() );
     }
      
### 12System类方法arraycopy
	 A:System类方法arraycopy：
	  /*
	   * System类方法,复制数组
	   * arraycopy(Object src, int srcPos, Object dest, int destPos, int length)
	   * Object src, 要复制的源数组
	   * int srcPos, 数组源的起始索引
	   * Object dest,复制后的目标数组
	   * int destPos,目标数组起始索引 
	   * int length, 复制几个
	   */
	  public static void function_4(){
	  	int[] src = {11,22,33,44,55,66};
	  	int[] desc = {77,88,99,0};
	  	
	  	System.arraycopy(src, 1, desc, 1, 2);//将src数组的1位置开始(包含1位置)的两个元素,拷贝到desc的1,2位置上
	  	for(int i = 0 ;  i < desc.length ; i++){
	  		System.out.println(desc[i]);
	  	}
	  }

### 13Math类的方法_1
   A:Math类中的方法
   
       /*
         * static double sqrt(double d)
         * 返回参数的平方根
         */
    public static void function_4(){
            double d = Math.sqrt(-2);
            System.out.println(d);
        }
   	
   	/*0
   	 * static double pow(double a, double b)
   	 * a的b次方
   	 */
   	public static void function_3(){
   		double d = Math.pow(2, 3);
   		System.out.println(d);
   	}
   	
   	/*
   	 * static double floor(double d)
   	 * 返回小于或者等于参数d的最大整数
   	 */
   	public static void function_2(){
   		double d = Math.floor(1.5);
   		System.out.println(d);
   	}
   	
   	/*
   	 *  static double ceil(double d)
   	 *  返回大于或者等于参数d的最小整数
   	 */
   	public static void function_1(){
   		double d = Math.ceil(5.1);
   		System.out.println(d);
   	}
   	
   	/*
   	 *  static int abs(int i)
   	 *  获取参数的绝对值
   	 */
   	 public static void function(){
   		int i = Math.abs(0);
   		System.out.println(i);
   	 }

### 14Math类的方法_2
 A:Math类的方法_2
 
     /*
       *  static double round(doubl d)
       *  获取参数的四舍五入,取整数
       */
    public static void function_6(){
  	double d = Math.round(5.4195);
  	System.out.println(d);
    }
  
      /*
       *  static double random() 返回随机数 0.0-1.0之间
       *  来源,也是Random类
       */
      public static void function_5(){
        for(int i = 0 ; i < 10 ;i++){
            double d = Math.random();
            System.out.println(d);
        }
      }

### 15Arrays工具类 
  A:Arrays工具类:
  
    public class ArraysDemo {
    	public static void main(String[] args) {
    		function_2();
    		int[] arr = {56,65,11,98,57,43,16,18,100,200};
    		int[] newArray = test(arr);
    		System.out.println(Arrays.toString(newArray));
    	}
    	/*
    	 *  定义方法,接收输入,存储的是10个人考试成绩
    	 *  将最后三个人的成绩,存储到新的数组中,返回新的数组
    	 */
    	public static int[] test(int[] arr){
    		//对数组排序
    		Arrays.sort(arr);
    		//将最后三个成绩存储到新的数组中
    		int[] result = new int[3];
    		//成绩数组的最后三个元素,复制到新数组中
    	//	System.arraycopy(arr, 0, result, 0, 3);
    		for(int i = 0 ;  i < 3 ;i++){
    			result[i] = arr[i];
    		}
    		return result;
    	}
    	
    	/*
    	 *  static String toString(数组)
    	 *  将数组变成字符串
    	 */
    	public static void function_2(){
    		int[] arr = {5,1,4,6,8,9,0};
    		String s = Arrays.toString(arr);
    		System.out.println(s);
    	}
    	
    	/*
    	 *  static int binarySearch(数组, 被查找的元素)
    	 *  数组的二分搜索法
    	 *  返回元素在数组中出现的索引
    	 *  元素不存在, 返回的是  (-插入点-1)
    	 */
    	public static void function_1(){
    		int[] arr = {1,4,7,9,11,15,18};
    	    int index =  Arrays.binarySearch(arr, 10);
    	    System.out.println(index);
    	}
    	
    	/*
    	 *  static void sort(数组)
    	 *  对数组升序排列
    	 */
    	public static void function(){
    		int[] arr = {5,1,4,6,8,9,0};
    		Arrays.sort(arr);
    		for (int i = 0; i < arr.length; i++) {
    			System.out.println(arr[i]);
    		}
    	}
    }

 
### 16数组复制练习
   *A:数组复制练习:
   
	       public static void main(String[] args) {
	    		int[] arr = {56,65,11,98,57,43,16,18,100,200};
	    		int[] newArray = test(arr);
	    		System.out.println(Arrays.toString(newArray));
	    	}
	    	/*
	    	 *  定义方法,接收输入,存储的是10个人考试成绩
	    	 *  将最后三个人的成绩,存储到新的数组中,返回新的数组
	    	 */
	    	public static int[] test(int[] arr){
	    		//对数组排序
	    		Arrays.sort(arr);
	    		//将最后三个成绩存储到新的数组中
	    		int[] result = new int[3];
	    		//成绩数组的最后三个元素,复制到新数组中
	    	    //System.arraycopy(arr, 0, result, 0, 3);
	    		for(int i = 0 ;  i < 3 ;i++){
	    			result[i] = arr[i];
	    		}
	    		return result;
	    	}

### 17BigInteger类概述和构造方法   
    //A:BigInteger类概述和构造方法
    public static void main(String[] args) {
   		function();
   	}
    /*
   	 * BigInteger类的构造方法
   	 * 传递字符串,要求数字格式,没有长度限制
   	 */
   	public static void function(){
   		BigInteger b = new BigInteger("8465846668464684562385634168451684568645684564564");
   		System.out.println(b);
   		BigInteger b1 = new BigInteger("5861694569514568465846668464684562385634168451684568645684564564");
   		System.out.println(b1);
   	}

### 18BigInteger类四则运算  
 A:BigInteger类四则运算
 
        public static void main(String[] args) {
   		function_1();
   	}
	/*
	 * BigInteger对象的四则运算
	 * 调用方法计算,计算结果也只能是BigInteger对象
	 */
	 public static void function_1(){
		 BigInteger b1 = new BigInteger("5665464516451051581613661405146");
		 BigInteger b2 = new BigInteger("965855861461465516451051581613661405146");
		 
		 //计算 b1+b2对象的和,调用方法 add
		 BigInteger bigAdd = b1.add(b2);//965855867126930032902103163227322810292
		 System.out.println(bigAdd);
		 
		 //计算b1-b2对象的差,调用方法subtract
		 BigInteger bigSub = b1.subtract(b2);
		 System.out.println(bigSub);
		 
		 //计算b1*b2对象的乘积,调用方法multiply
		 BigInteger bigMul = b1.multiply(b2);
		 System.out.println(bigMul);
		 
		 //计算b2/b1对象商,调用方法divied
		 BigInteger bigDiv = b2.divide(b1);
		 System.out.println(bigDiv);
	 }

### 19员工案例的子类的编写
 A:BigDecimal类概述 
    
    /*
     * 计算结果,未知
     * 原因: 计算机二进制中,表示浮点数不精确造成
     * 超级大型的浮点数据,提供高精度的浮点运算, BigDecimal
    System.out.println(0.09 + 0.01);//0.09999999999999999
    System.out.println(1.0 - 0.32);//0.6799999999999999
    System.out.println(1.015 * 100);//101.49999999999999
    System.out.println(1.301 / 100);//0.013009999999999999 
    */

### 20BigDecimal类实现加法减法乘法  
 A:BigDecimal类实现加法减法乘法
 
    /*
  	 *  BigDecimal实现三则运算
  	 *  + - *
  	 */
  	public static void function(){
  		BigDecimal b1 =  new BigDecimal("0.09");
  		BigDecimal b2 =  new BigDecimal("0.01");
  		//计算b1+b2的和,调用方法add
  		BigDecimal bigAdd = b1.add(b2);
  		System.out.println(bigAdd);
  		
  		BigDecimal b3 = new BigDecimal("1");
  		BigDecimal b4 = new BigDecimal("0.32");
  		//计算b3-b2的差,调用方法subtract
  		BigDecimal bigSub = b3.subtract(b4);
  		System.out.println(bigSub);
  		
  		BigDecimal b5 = new BigDecimal("1.015");
  		BigDecimal b6 = new BigDecimal("100");
  		//计算b5*b6的成绩,调用方法 multiply
  		BigDecimal bigMul = b5.multiply(b6);
  		System.out.println(bigMul);
  	}

### 21BigDecimal类实现除法
	 A:BigDecimal类实现除法
	 /*
	  * BigDecimal实现除法运算
	  * divide(BigDecimal divisor, int scale, int roundingMode) 
	  * int scale : 保留几位小数
	  * int roundingMode : 保留模式
	  * 保留模式 阅读API文档
	  *   static int ROUND_UP  向上+1
	  *   static int ROUND_DOWN 直接舍去
	  *   static int ROUND_HALF_UP  >= 0.5 向上+1
	  *   static int ROUND_HALF_DOWN   > 0.5 向上+1 ,否则直接舍去
	  */
	 public static void function_1(){
	 	BigDecimal b1 = new BigDecimal("1.0301");
	 	BigDecimal b2 = new BigDecimal("100");
	 	//计算b1/b2的商,调用方法divied
	 	BigDecimal bigDiv = b1.divide(b2,2,BigDecimal.ROUND_HALF_UP);//0.01301
	 	System.out.println(bigDiv);
	 }


## 集合
### 01集合使用的回顾
	 *A:集合使用的回顾
	   *a.ArrayList集合存储5个int类型元素
          public static void main(String[] args) {
               ArrayList<Integer> list = new ArrayList<Integer>();
            list.add(111);
            list.add(222);
            list.add(333);
            list.add(444);
            list.add(555);
            for(int i=0; i<list.size(); i++){
                   System.out.println(list.get(i));
           }
          }

      *b.ArrayList集合存储5个Person类型元素
         public static void main(String[] args) {
          ArrayList<Person> list = new ArrayList<Person>();
          list.add(new Person(“小强”));
          list.add(new Person(“老王”));
          list.add(new Person(“小虎”));
          list.add(new Person(“小泽”));
          list.add(new Person(“小红”));
          for(int i=0; i<list.size(); i++){
            Person p = list.get(i);
                  System.out.println(p);
           }
         }


### 02集合的学习目标
	   集合，集合是java中提供的一种容器，可以用来存储多个数据。
     在前面的学习中，我们知道数据多了，可以使用数组存放或者使用ArrayList集合进行存放数据。那么，集合和数组既然都是容器，它们有啥区别呢？
       数组的长度是固定的。集合的长度是可变的。
       集合中存储的元素必须是引用类型数据

### 03集合继承关系图
    A:集合继承关系图
     a:ArrayList的继承关系:
     查看ArrayList类发现它继承了抽象类AbstractList同时实现接口List，而List接口又继承了Collection接口。Collection接口为最顶层集合接口了。
     源代码：
      interface List extends Collection {
      }
      public class ArrayList extends AbstractList implements List{
      }
    
    b:集合继承体系
     这说明我们在使用ArrayList类时，该类已经把所有抽象方法进行了重写。那么，实现Collection接口的所有子类都会进行方法重写。
       Collecton接口常用的子接口有：List接口、Set接口
       List接口常用的子类有：ArrayList类、LinkedList类
       Set接口常用的子类有：HashSet类、LinkedHashSet类
     
                              Collection 接口     
                                   |
     ----------------------------------------------------------------
     |                                                              |
    List接口                                                       Set接口
     |                                                              |
 ----------------                                             -------------
 |              |                                             |            |
ArrayList类    LinkedList类                                 HashSet类     LinkedHashSet类

### 04集合Collection的方法
	A:集合Collection的方法
     /*
      *  Collection接口中的方法
      *  是集合中所有实现类必须拥有的方法
      *  使用Collection接口的实现类,程序的演示
      *  ArrayList implements List
      *  List extends Collection
      *  方法的执行,都是实现的重写
      */
     public class CollectionDemo {
      public static void main(String[] args) {
        function_2();
      }
      
      
      /*  Collection接口方法
       *  Object[] toArray() 集合中的元素,转成一个数组中的元素, 集合转成数组
       *  返回是一个存储对象的数组, 数组存储的数据类型是Object
       */
      private static void function_2() {
        Collection<String> coll = new ArrayList<String>();
        coll.add("abc");
        coll.add("itcast");
        coll.add("itheima");
        coll.add("money");
        coll.add("123");
        
        Object[] objs = coll.toArray();
        for(int i = 0 ; i < objs.length ; i++){
          System.out.println(objs[i]);
        }
      }
      /*
       * 学习Java中三种长度表现形式
       *   数组.length 属性  返回值 int
       *   字符串.length() 方法,返回值int
       *   集合.size()方法, 返回值int
       */
      
      /*
       * Collection接口方法
       * boolean contains(Object o) 判断对象是否存在于集合中,对象存在返回true
       * 方法参数是Object类型
       */
      private static void function_1() {
        Collection<String> coll = new ArrayList<String>();
        coll.add("abc");
        coll.add("itcast");
        coll.add("itheima");
        coll.add("money");
        coll.add("123");
        
        boolean b = coll.contains("itcast");
        System.out.println(b);
      }


      /*
       * Collection接口的方法
       * void clear() 清空集合中的所有元素
       * 集合容器本身依然存在
       */
      public static void function(){
        //接口多态的方式调用
        Collection<String> coll = new ArrayList<String>();
        coll.add("abc");
        coll.add("bcd");
        System.out.println(coll);
        
        coll.clear();
        
        System.out.println(coll);
        
      }
     }

### 05集合Collection的remove方法
   A:05集合Collection的remove方法
   
    /*
     * Collection接口方法
     * boolean remove(Object o)移除集合中指定的元素
     */
    private static void function_3(){
      Collection<String> coll = new ArrayList<String>();
      coll.add("abc");
      coll.add("money");
      coll.add("itcast");
      coll.add("itheima");
      coll.add("money");
      coll.add("123");  
      System.out.println(coll);
      
      boolean b = coll.remove("money");
      System.out.println(b);
      System.out.println(coll);
    }


### 06迭代器的概述

    A:迭代器概述:
        a:java中提供了很多个集合，它们在存储元素时，采用的存储方式不同。
        我们要取出这些集合中的元素，可通过一种通用的获取方式来完成。
   
    b:Collection集合元素的通用获取方式：在取元素之前先要判断集合中有没有元素，
        如果有，就把这个元素取出来，继续在判断，如果还有就再取出出来。一直把集合中的所有元素全部取出。这种取出方式专业术语称为迭代。
   
    c:每种集合的底层的数据结构不同,例如ArrayList是数组,LinkedList底层是链表,但是无论使用那种集合,我们都会有判断是否有元素
     以及取出里面的元素的动作,那么Java为我们提供一个迭代器定义了统一的判断元素和取元素的方法 

### 07迭代器的实现原理
   *A:迭代器的实现原理
   
	  /*
     *  集合中的迭代器:
     *    获取集合中元素方式
     *  接口 Iterator : 两个抽象方法
     *     boolean hasNext() 判断集合中还有没有可以被取出的元素,如果有返回true
     *     next() 取出集合中的下一个元素
     *     
     *  Iterator接口,找实现类.
     *    Collection接口定义方法 
     *       Iterator  iterator()
     *    ArrayList 重写方法 iterator(),返回了Iterator接口的实现类的对象
     *    使用ArrayList集合的对象
     *     Iterator it =array.iterator(),运行结果就是Iterator接口的实现类的对象
     *     it是接口的实现类对象,调用方法 hasNext 和 next 集合元素迭代
     */

### 08迭代器的代码实现
   *A:迭代器的代码实现
   
      public class IteratorDemo {
        public static void main(String[] args) {
          Collection<String> coll = new ArrayList<String>();
          coll.add("abc1");
          coll.add("abc2");
          coll.add("abc3");
          coll.add("abc4");
          //迭代器,对集合ArrayList中的元素进行取出
          
          //调用集合的方法iterator()获取出,Iterator接口的实现类的对象
          Iterator<String> it = coll.iterator();
          //接口实现类对象,调用方法hasNext()判断集合中是否有元素
          //boolean b = it.hasNext();
          //System.out.println(b);
          //接口的实现类对象,调用方法next()取出集合中的元素
          //String s = it.next();
          //System.out.println(s);
          
          //迭代是反复内容,使用循环实现,循环的条件,集合中没元素, hasNext()返回了false
          while(it.hasNext()){
            String s = it.next();
            System.out.println(s);
          }
          
         
          
        }
      }
### 09迭代器的执行过程
   A:迭代器的执行过程
     a:迭代器的原理:
     
       while(it.hasNext()) {
            System.out.println(it.next());
       }
       
       //cursor记录的索引值不等于集合的长度返回true,否则返回false
         public boolean hasNext() {       
           return cursor != size; //cursor初值为0
                           
         }

        //next()方法作用:
        //①返回cursor指向的当前元素 
        //②cursor++
        public Object next() {            
                 int i = cursor; 
                 cursor = i + 1;  
                 return  elementData[lastRet = i]; 
             
             }
     b:for循环迭代写法:
        for (Iterator<String> it2 = coll.iterator(); it2.hasNext();  ) {
         System.out.println(it2.next());
       } 

### 10集合迭代中的转型 
   * A:集合迭代中的转型
   
    - a:在使用集合时，我们需要注意以下几点：
         -  集合中存储其实都是对象的地址。
         - 集合中可以存储基本数值吗？
         - jdk1.5版本以后可以存储了。
         因为出现了基本类型包装类，它提供了自动装箱操作（基本类型对象），这样，集合中的元素就是基本数值的包装类对象。
    
    b:存储时提升了Object。取出时要使用元素的特有内容，必须向下转型。
         Collection coll = new ArrayList();
         coll.add("abc");
         coll.add("aabbcc");
         coll.add("shitcast");
         Iterator it = coll.iterator();
         while (it.hasNext()) {
          //由于元素被存放进集合后全部被提升为Object类型
         //当需要使用子类对象特有方法时，需要向下转型
          String str = (String) it.next();
          System.out.println(str.length());
         }
         注意：如果集合中存放的是多个对象，这时进行向下转型会发生类型转换异常。

    
    c:Iterator接口也可以使用<>来控制迭代元素的类型的。代码演示如下：
         Collection<String> coll = new ArrayList<String>();
         coll.add("abc");
         coll.add("aabbcc");
         coll.add("shitcast");
         Iterator<String> it = coll.iterator();
         while (it.hasNext()) {
          String str =  it.next(); 
         //当使用Iterator<String>控制元素类型后，就不需要强转了。获取到的元素直接就是String类型
          System.out.println(str.length());
         }
    
### 11增强for循环遍历数组
   * A:增强for循环遍历数组
      * a:格式:
     
    /*
      *  JDK1.5新特性,增强for循环
      *  JDK1.5版本后,出现新的接口 java.lang.Iterable
      *    Collection开是继承Iterable
      *    Iterable作用,实现增强for循环
      *    
      *    格式:
      *      for( 数据类型  变量名 : 数组或者集合 ){
      *         sop(变量);
      *      }
      */
     public static void function_1(){
        //for对于对象数组遍历的时候,能否调用对象的方法呢
        String[] str = {"abc","itcast","cn"};
        for(String s : str){
          System.out.println(s.length());
        }
      }
      
      /*
       *  实现for循环,遍历数组
       *  好处: 代码少了,方便对容器遍历
       *  弊端: 没有索引,不能操作容器里面的元素
       */
      public static void function(){
        int[] arr = {3,1,9,0};
        for(int i : arr){
          System.out.println(i+1);
        }
        System.out.println(arr[0]);
      }
### 12增强for循环遍历集合 
      A:增强for循环遍历集合  
        /*
         *  增强for循环遍历集合
         *  存储自定义Person类型
         */
        public static void function_2(){
          ArrayList<Person> array = new ArrayList<Person>();
          array.add(new Person("a",20));
          array.add(new Person("b",10));
          for(Person p : array){
            System.out.println(p);// System.out.println(p.toString());
          }
        }
        
### 13泛型的引入 
   A:泛型的引入
    在前面学习集合时，我们都知道集合中是可以存放任意对象的，
    只要把对象存储集合后，那么这时他们都会被提升成Object类型。
    当我们在取出每一个对象，并且进行相应的操作，这时必须采用类型转换。比如下面程序：
    public class GenericDemo {
      public static void main(String[] args) {
        List list = new ArrayList();
        list.add("abc");
        list.add("itcast");
        list.add(5);//由于集合没有做任何限定，任何类型都可以给其中存放
                    //相当于:Object obj=new Integer(5);
        
        Iterator it = list.iterator();
        while(it.hasNext()){
          //需要打印每个字符串的长度,就要把迭代出来的对象转成String类型
          String str = (String) it.next();//String str=(String)obj;
                                          //编译时期仅检查语法错误,String是Object的儿子可以向下转型
                                          //运行时期String str=(String)(new Integer(5))
                                          //String与Integer没有父子关系所以转换失败
                                          //程序在运行时发生了问题java.lang.ClassCastException
          System.out.println(str.length());
        }
      }
    }

    

### 14泛型的定义和使用
  A:泛型的定义和使用
    /*
     * JDK1.5 出现新的安全机制,保证程序的安全性
     *   泛型: 指明了集合中存储数据的类型  <数据类型>
     */

    public class GenericDemo {
      public static void main(String[] args) {
        function();
      }
      
      public static void function(){
        Collection<String> coll = new ArrayList<String>();
        coll.add("abc");
        coll.add("rtyg");
        coll.add("43rt5yhju");
    //    coll.add(1);
        
        Iterator<String> it = coll.iterator();
        while(it.hasNext()){
          String s = it.next();
          System.out.println(s.length());
        }
      }
    }

### 15Java中的伪泛型
	 A:Java中的伪泛型：
	   泛型只在编译时存在,编译后就被擦除,在编译之前我们就可以限制集合的类型,起到作用
     例如:ArrayList<String> al=new ArrayList<String>();
     编译后:ArrayList al=new ArrayList();


### 16泛型类
  A:泛型类:
    a:定义格式：
      修饰符 class 类名<代表泛型的变量> {  }
      
      例如，API中的ArrayList集合：
      class ArrayList<E>{ 
           public boolean add(E e){ }
        public E get(int index){  }
      }

    b:使用格式：
      创建对象时，确定泛型的类型
     
      例如，ArrayList<String> list = new ArrayList<String>();
      此时，变量E的值就是String类型
      class ArrayList<String>{ 
        public boolean add(String e){ }
        public String get(int index){  }
      }
     
      例如，ArrayList<Integer> list = new ArrayList<Integer>();
      此时，变量E的值就是Integer类型
      class ArrayList<Integer>{ 
           public boolean add(Integer e){ }
           public Integer get(int index){  }
      }

### 17泛型的方法
  A:泛型的方法
    a:定义格式：修饰符 <代表泛型的变量> 返回值类型 方法名(参数){  }
    b:泛型方法的使用:
     1:例如，API中的ArrayList集合中的方法：
      public <T> T[] toArray(T[] a){  } 
      //该方法，用来把集合元素存储到指定数据类型的数组中，返回已存储集合元素的数组

      使用格式：调用方法时，确定泛型的类型
    例如:
          ArrayList<String> list = new ArrayList<String>();
          String[] arr = new String[100];
          String[] result = list.toArray(arr);
       此时，变量T的值就是String类型。变量T，可以与定义集合的泛型不同
       public <String> String[] toArray(String[] a){  } 
    

      例如:
          ArrayList<String> list = new ArrayList<String>();
          Integer[] arr = new Integer[100];
          Integer [] result = list.toArray(arr);
      
      此时，变量T的值就是Integer类型。变量T，可以与定义集合的泛型不同
      public <Integer> Integer[] toArray(Integer[] a){  } 

 
### 18泛型的接口 
   A:泛型的接口:
   
     /*
      *  带有泛型的接口
      *  
      *  public interface List <E>{
      *    abstract boolean add(E e);
      *  }
      * 
      *  实现类,先实现接口,不理会泛型
      *  public class ArrayList<E> implements List<E>{
      *  }
      *  调用者 : new ArrayList<String>() 后期创建集合对象的时候,指定数据类型
      *  
      *  
      *  实现类,实现接口的同时,也指定了数据类型
      *  public class XXX implements List<String>{
      *  }
      *  new XXX()
      */
     public class GenericDemo2 {
      
     }
 
### 19泛型的好处
  *A:泛型的好处
  
   * a:将运行时期的ClassCastException，转移到了编译时期变成了编译失败。
   * b:避免了类型强转的麻烦。
    演示下列代码：
    
            
      public class GenericDemo {
         public static void main(String[] args) {
            List<String> list = new ArrayList<String>();
            list.add("abc");
            list.add("itcast");
            //list.add(5);//当集合明确类型后，存放类型不一致就会编译报错
                         //集合已经明确具体存放的元素类型，那么在使用迭代器的时候，迭代器也同样会知道具体遍历元素类型
           
            Iterator<String> it = list.iterator();
            while(it.hasNext()){
               String str = it.next();
               System.out.println(str.length()); //当使用Iterator<String>      
                                                //控制元素类型后，就不需要强转了。获取到的元素直接就是String类型
            }
         }
      }

### 20泛型的通配符   
   A:泛型的通配符
   
    /*
    *  泛型的通配符
    */
    public class GenericDemo {
    public static void main(String[] args) {
      ArrayList<String> array = new ArrayList<String>();
      
      HashSet<Integer> set = new HashSet<Integer>();
      
      array.add("123");
      array.add("456");
      
      set.add(789);
      set.add(890);
      
      iterator(array);
      iterator(set);
    }
    /*
     *  定义方法,可以同时迭代2个集合
     *  参数: 怎么实现 , 不能写ArrayList,也不能写HashSet
     *  参数: 或者共同实现的接口
     *  泛型的通配,匹配所有的数据类型  ?
     */
    public static void iterator(Collection<?> coll){
      Iterator<?> it = coll.iterator();
      while(it.hasNext()){
        //it.next()获取的对象,什么类型
        System.out.println(it.next());
      }
    }
   }
 
### 21泛型的限定 
 A:泛型的限定
 
    /*
    *  将的酒店员工,厨师,服务员,经理,分别存储到3个集合中
    *  定义方法,可以同时遍历3集合,遍历三个集合的同时,可以调用工作方法
    */
       import java.util.ArrayList;
       import java.util.Iterator;
       public class GenericTest {
        public static void main(String[] args) {
          //创建3个集合对象
          ArrayList<ChuShi> cs = new ArrayList<ChuShi>();
          ArrayList<FuWuYuan> fwy = new ArrayList<FuWuYuan>();
          ArrayList<JingLi> jl = new ArrayList<JingLi>();
          
          //每个集合存储自己的元素
          cs.add(new ChuShi("张三", "后厨001"));
          cs.add(new ChuShi("李四", "后厨002"));
          
          fwy.add(new FuWuYuan("翠花", "服务部001"));
          fwy.add(new FuWuYuan("酸菜", "服务部002"));
          
          jl.add(new JingLi("小名", "董事会001", 123456789.32));
          jl.add(new JingLi("小强", "董事会002", 123456789.33));
          
       //   ArrayList<String> arrayString = new ArrayList<String>();
          iterator(jl);
          iterator(fwy);
          iterator(cs);
        
    }
    /*
     * 定义方法,可以同时遍历3集合,遍历三个集合的同时,可以调用工作方法 work
     * ? 通配符,迭代器it.next()方法取出来的是Object类型,怎么调用work方法
     * 强制转换:  it.next()=Object o ==> Employee
     * 方法参数: 控制,可以传递Employee对象,也可以传递Employee的子类的对象
     * 泛型的限定  本案例,父类固定Employee,但是子类可以无限?
     *   ? extends Employee 限制的是父类, 上限限定, 可以传递Employee,传递他的子类对象
     *   ? super   Employee 限制的是子类, 下限限定, 可以传递Employee,传递他的父类对象
     */
    public static void iterator(ArrayList<? extends Employee> array){
      
       Iterator<? extends Employee> it = array.iterator();
       while(it.hasNext()){
         //获取出的next() 数据类型,是什么Employee
         Employee e = it.next();
         e.work();
       }
    }
    }


 
 

### 01List接口的特点
  A:List接口的特点:
   a:它是一个元素存取有序的集合。
        例如，存元素的顺序是11、22、33。那么集合中，元素的存储就是按照11、22、33的顺序完成的）。
   b:它是一个带有索引的集合，通过索引就可以精确的操作集合中的元素（与数组的索引是一个道理）。
   
     c:集合中可以有重复的元素，通过元素的equals方法，来比较是否为重复的元素。

     d:List接口的常用子类有：
      ArrayList集合
      LinkedList集合

### 02List接口的特有方法
	A:List接口的特有方法(带索引的方法)
   a:增加元素方法
   add(Object e)：向集合末尾处，添加指定的元素 
   add(int index, Object e)   向集合指定索引处，添加指定的元素，原有元素依次后移
     
     /*
       *  add(int index, E)
       *  将元素插入到列表的指定索引上
       *  带有索引的操作,防止越界问题
       *  java.lang.IndexOutOfBoundsException
       *     ArrayIndexOutOfBoundsException
       *     StringIndexOutOfBoundsException
       */
      public static void function(){
        List<String> list = new ArrayList<String>();
        list.add("abc1");
        list.add("abc2");
        list.add("abc3");
        list.add("abc4");
        System.out.println(list);
        
        list.add(1, "itcast");
        System.out.println(list);
      }

   b:删除元素删除
   remove(Object e)：将指定元素对象，从集合中删除，返回值为被删除的元素
   remove(int index)：将指定索引处的元素，从集合中删除，返回值为被删除的元素
     /*
       *  E remove(int index)
       *  移除指定索引上的元素
       *  返回被删除之前的元素
       */
      public static void function_1(){
        List<Double> list = new ArrayList<Double>();
        list.add(1.1);
        list.add(1.2);
        list.add(1.3);
        list.add(1.4);
        
        Double d = list.remove(0);
        System.out.println(d);
        System.out.println(list);
      }
   c:替换元素方法
   set(int index, Object e)：将指定索引处的元素，替换成指定的元素，返回值为替换前的元素
      /*
       *  E set(int index, E)
       *  修改指定索引上的元素
       *  返回被修改之前的元素
       */
      public static void function_2(){
        List<Integer> list = new ArrayList<Integer>();
        list.add(1);
        list.add(2);
        list.add(3);
        list.add(4);
        
        Integer i = list.set(0, 5);
        System.out.println(i);
        System.out.println(list);
      }
    d:查询元素方法
   get(int index)：获取指定索引处的元素，并返回该元素


### 03迭代器的并发修改异常
    A:迭代器的并发修改异常
     
     /*
      *  迭代器的并发修改异常 java.util.ConcurrentModificationException
      *  就是在遍历的过程中,使用了集合方法修改了集合的长度,不允许的
      */
     public class ListDemo1 {
      public static void main(String[] args) {
        List<String> list = new ArrayList<String>();
        list.add("abc1");
        list.add("abc2");
        list.add("abc3");
        list.add("abc4");
        
        //对集合使用迭代器进行获取,获取时候判断集合中是否存在 "abc3"对象
        //如果有,添加一个元素 "ABC3"
        Iterator<String> it = list.iterator();
        while(it.hasNext()){
          String s = it.next();
          //对获取出的元素s,进行判断,是不是有"abc3"
          if(s.equals("abc3")){
            list.add("ABC3");
          }
          System.out.println(s);
        }
      }
     }

     运行上述代码发生了错误 java.util.ConcurrentModificationException这是什么原因呢？
       在迭代过程中，使用了集合的方法对元素进行操作。
       导致迭代器并不知道集合中的变化，容易引发数据的不确定性。
       
     并发修改异常解决办法：
        在迭代时，不要使用集合的方法操作元素。
        或者通过ListIterator迭代器操作元素是可以的，ListIterator的出现，解决了使用Iterator迭代过程中可能会发生的错误情况。


### 04数据的存储结构
	A:数据的存储结构
     a:栈结构:后进先出/先进后出(手枪弹夹) FILO (first in last out)
     b:队列结构:先进先出/后进后出(银行排队) FIFO(first in first out)
     c:数组结构:
               查询快:通过索引快速找到元素
               增删慢:每次增删都需要开辟新的数组,将老数组中的元素拷贝到新数组中
                      开辟新数组耗费资源
     d:链表结构
               查询慢:每次都需要从链头或者链尾找起
               增删快:只需要修改元素记录的下个元素的地址值即可不需要移动大量元素




=======================第二节课开始=============================================
### 05ArrayList集合的自身特点
   A:ArrayList集合的自身特点
     底层采用的是数组结构
     ArrayList al=new ArrayList();//创建了一个长度为0的Object类型数组
     al.add("abc");//底层会创建一个长度为10的Object数组 Object[] obj=new Object[10]
                   //obj[0]="abc"
                  //如果添加的元素的超过10个,底层会开辟一个1.5*10的长度的新数组
                  //把原数组中的元素拷贝到新数组,再把最后一个元素添加到新数组中
   原数组:
     a b c d e f g h k l
   添加m:
     a b c d e f g h k l m null null null null

### 06LinkedList集合的自身特点
  A:LinkedList集合的自身特点
     底层采用链表结构,每次查询都要从链头或链尾找起,查询相对数组较慢
     但是删除直接修改元素记录的地址值即可,不要大量移动元素
     
     LinkedList的索引决定是从链头开始找还是从链尾开始找
     如果该元素小于元素长度一半,从链头开始找起,如果大于元素长度的一半,则从链尾找起

### 07LinkedList特有方法
   *A:LinkedList特有方法:获取,添加,删除
	   /*
     *  LinkedList 链表集合的特有功能
     *    自身特点: 链表底层实现,查询慢,增删快
     *  
     *  子类的特有功能,不能多态调用
     */
    public class LinkedListDemo {
      public static void main(String[] args) {
        function_3();
      }


      /*
       *  E removeFirst() 移除并返回链表的开头
       *  E removeLast() 移除并返回链表的结尾
       */
      public static void function_3(){
        LinkedList<String> link = new LinkedList<String>();
        link.add("1");
        link.add("2");
        link.add("3");
        link.add("4");
        
        String first = link.removeFirst();
        String last = link.removeLast();
        System.out.println(first);
        System.out.println(last);
      
        System.out.println(link);
      }
      
      /*
       * E getFirst() 获取链表的开头
       * E getLast() 获取链表的结尾
       */
      public static void function_2(){
        LinkedList<String> link = new LinkedList<String>();
        link.add("1");
        link.add("2");
        link.add("3");
        link.add("4");
      
        if(!link.isEmpty()){
          String first = link.getFirst();
          String last = link.getLast();
          System.out.println(first);
          System.out.println(last);
        }
      }
      
      public static void function_1(){
        LinkedList<String> link = new LinkedList<String>();
        link.addLast("a");
        link.addLast("b");
        link.addLast("c");
        link.addLast("d");
        
        link.addFirst("1");
        link.addFirst("2");
        link.addFirst("3");
        System.out.println(link);
      }
      
      /*
       *  addFirst(E) 添加到链表的开头
       *  addLast(E) 添加到链表的结尾
       */
      public static void function(){
        LinkedList<String> link = new LinkedList<String>();
        
        link.addLast("heima");
        
        link.add("abc");
        link.add("bcd");
        
        link.addFirst("itcast");
        System.out.println(link);
        
        
      }
    }

### 08Vector类的特点
    *A:Vector类的特点
       Vector集合数据存储的结构是数组结构，为JDK中最早提供的集合,它是线程同步的
       Vector中提供了一个独特的取出方式，就是枚举Enumeration，它其实就是早期的迭代器。
       此接口Enumeration的功能与 Iterator 接口的功能是类似的。
       Vector集合已被ArrayList替代。枚举Enumeration已被迭代器Iterator替代。

### 09Set接口的特点
    A:Set接口的特点
     a:它是个不包含重复元素的集合。
     b:Set集合取出元素的方式可以采用：迭代器、增强for。
     c:Set集合有多个子类，这里我们介绍其中的HashSet、LinkedHashSet这两个集合。


### 10Set集合存储和迭代
    A:Set集合存储和迭代
      /*
       *  Set接口,特点不重复元素,没索引
       *  
       *  Set接口的实现类,HashSet (哈希表)
       *  特点: 无序集合,存储和取出的顺序不同,没有索引,不存储重复元素
       *  代码的编写上,和ArrayList完全一致
       */
      public class HashSetDemo {
        public static void main(String[] args) {
          Set<String> set = new HashSet<String>();
          set.add("cn");
          set.add("heima");
          set.add("java");
          set.add("java");
          set.add("itcast");
          
          Iterator<String> it = set.iterator();
          while(it.hasNext()){
            System.out.println(it.next());
          }
          System.out.println("==============");
          
          for(String s : set){
            System.out.println(s);
          }
        }
      }


   
### 11哈希表的数据结构
    A:哈希表的数据结构:(参见图解)
       
        加载因子:表中填入的记录数/哈希表的长度
        例如:
        加载因子是0.75 代表:
          数组中的16个位置,其中存入16*0.75=12个元素

        如果在存入第十三个(>12)元素,导致存储链子过长,会降低哈希表的性能,那么此时会扩充哈希表(在哈希),底层会开辟一个长度为原长度2倍的数组,把老元素拷贝到新数组中,再把新元素添加数组中
          
        当存入元素数量>哈希表长度*加载因子,就要扩容,因此加载因子决定扩容时机

### 12字符串对象的哈希值
      A:字符串对象的哈希值
      /*
       *  对象的哈希值,普通的十进制整数
       *  父类Object,方法 public int hashCode() 计算结果int整数
       */
      public class HashDemo {
        public static void main(String[] args) {
          Person p = new Person();
          int i = p.hashCode();
          System.out.println(i);
        
          String s1 = new String("abc");
          String s2 = new String("abc");
          System.out.println(s1.hashCode());
          System.out.println(s2.hashCode());
          
          /*System.out.println("重地".hashCode());
          System.out.println("通话".hashCode());*/
        }
      }
     
      //String类重写hashCode()方法
      //字符串都会存储在底层的value数组中{'a','b','c'}
      public int hashCode() {
              int h = hash;//hash初值为0
              if (h == 0 && value.length > 0) {
                  char val[] = value;

                  for (int i = 0; i < value.length; i++) {
                      h = 31 * h + val[i];
                  }
                  hash = h;
              }
              return h;
          }

        
### 13哈希表的存储过程
   A:哈希表的存储过程
     public static void main(String[] args) {
        HashSet<String> set = new HashSet<String>();
        set.add(new String("abc"));
        set.add(new String("abc"));
        set.add(new String("bbc"));
        set.add(new String("bbc"));
        System.out.println(set); 
    }

  存取原理:
    每存入一个新的元素都要走以下三步:

    1.首先调用本类的hashCode()方法算出哈希值

    2.在容器中找是否与新元素哈希值相同的老元素,
      如果没有直接存入
      如果有转到第三步
    
    3.新元素会与该索引位置下的老元素利用equals方法一一对比
      一旦新元素.equals(老元素)返回true,停止对比,说明重复,不再存入
      如果与该索引位置下的老元素都通过equals方法对比返回false,说明没有重复,存入
 

### 14哈希表的存储自定义对象
   A:哈希表的存储自定义对象
     /*
      *  HashSet集合的自身特点:
      *    底层数据结构,哈希表
      *    存储,取出都比较快
      *    线程不安全,运行速度快
      */
     public class HashSetDemo1 {
      public static void main(String[] args) {
        
        //将Person对象中的姓名,年龄,相同数据,看作同一个对象
        //判断对象是否重复,依赖对象自己的方法 hashCode,equals
        HashSet<Person> setPerson = new HashSet<Person>();
        setPerson.add(new Person("a",11));
        setPerson.add(new Person("b",10));
        setPerson.add(new Person("b",10));
        setPerson.add(new Person("c",25));
        setPerson.add(new Person("d",19));
        setPerson.add(new Person("e",17));//每个对象的地址值都不同,调用Obejct类的hashCode方法返回不同哈希值,直接存入
        System.out.println(setPerson);
      }
     }
    
    public class Person {
      private String name;
      private int age;
      
      public String getName() {
        return name;
      }
      public void setName(String name) {
        this.name = name;
      }
      public int getAge() {
        return age;
      }
      public void setAge(int age) {
        this.age = age;
      }
      public Person(String name, int age) {
        super();
        this.name = name;
        this.age = age;
      }
      public Person(){}
      
      public String toString(){
        return name+".."+age;
      }
      


     }


      

### 15自定义对象重写hashCode和equals
	 A:自定义对象重写hashCode和equals
	  /*
          *  HashSet集合的自身特点:
          *    底层数据结构,哈希表
          *    存储,取出都比较快
          *    线程不安全,运行速度快
          */
         public class HashSetDemo1 {
          public static void main(String[] args) {
            
            //将Person对象中的姓名,年龄,相同数据,看作同一个对象
            //判断对象是否重复,依赖对象自己的方法 hashCode,equals
            HashSet<Person> setPerson = new HashSet<Person>();
            setPerson.add(new Person("a",11));
            setPerson.add(new Person("b",10));
            setPerson.add(new Person("b",10));
            setPerson.add(new Person("c",25));
            setPerson.add(new Person("d",19));
            setPerson.add(new Person("e",17));
            System.out.println(setPerson);
          }
         }
        
        public class Person {
          private String name;
          private int age;

          /*
           *  没有做重写父类,每次运行结果都是不同整数
           *  如果子类重写父类的方法,哈希值,自定义的
           *  存储到HashSet集合的依据
           *   
           *  尽可能让不同的属性值产生不同的哈希值,这样就不用再调用equals方法去比较属性
           *
           */
          public int hashCode(){
            return name.hashCode()+age*55;
          }
          //方法equals重写父类,保证和父类相同
          //public boolean equals(Object obj){}
          public boolean equals(Object obj){
            if(this == obj)
              return true;
            if(obj == null)
              return false;
            if(obj instanceof Person){
              Person p = (Person)obj;
              return name.equals(p.name) && age==p.age;
            }
            return false;
          }
          
          public String getName() {
            return name;
          }
          public void setName(String name) {
            this.name = name;
          }
          public int getAge() {
            return age;
          }
          public void setAge(int age) {
            this.age = age;
          }
          public Person(String name, int age) {
            super();
            this.name = name;
            this.age = age;
          }
          public Person(){}
          
          public String toString(){
            return name+".."+age;
          }
          


         }



### 16LinkedHashSet集合
  A:LinkedHashSet集合
    /*
     *   LinkedHashSet 基于链表的哈希表实现
     *   继承自HashSet
     *   
     *   LinkedHashSet 自身特性,具有顺序,存储和取出的顺序相同的
     *   线程不安全的集合,运行速度块
     */
    public class LinkedHashSetDemo {
      
      public static void main(String[] args) {
        LinkedHashSet<Integer> link = new LinkedHashSet<Integer>();
        link.add(123);
        link.add(44);
        link.add(33);
        link.add(33);
        link.add(66);
        link.add(11);
        System.out.println(link);
      }
    }


### 17ArrayList,HashSet判断对象是否重复的原因
  A:ArrayList,HashSet判断对象是否重复的原因
     a:ArrayList的contains方法原理:底层依赖于equals方法
       ArrayList的contains方法会使用调用方法时，
         传入的元素的equals方法依次与集合中的旧元素所比较，
         从而根据返回的布尔值判断是否有重复元素。
         此时，当ArrayList存放自定义类型时，由于自定义类型在未重写equals方法前，
         判断是否重复的依据是地址值，所以如果想根据内容判断是否为重复元素，需要重写元素的equals方法。
    
     b:HashSet的add()方法和contains方法()底层都依赖 hashCode()方法与equals方法()

      Set集合不能存放重复元素，其添加方法在添加时会判断是否有重复元素，有重复不添加，没重复则添加。
      HashSet集合由于是无序的，其判断唯一的依据是元素类型的hashCode与equals方法的返回结果。规则如下：
      先判断新元素与集合内已经有的旧元素的HashCode值
       如果不同，说明是不同元素，添加到集合。
       如果相同，再判断equals比较结果。返回true则相同元素；返回false则不同元素，添加到集合。
      所以，使用HashSet存储自定义类型，如果没有重写该类的hashCode与equals方法，则判断重复时，使用的是地址值，如果想通过内容比较元素是否相同，需要重写该元素类的hashcode与equals方法。


 
### 18hashCode和equals方法的面试题 
 A:hashCode和equals的面试题
 /*
  *   两个对象  Person  p1 p2
  *   问题: 如果两个对象的哈希值相同 p1.hashCode()==p2.hashCode()
  *        两个对象的equals一定返回true吗  p1.equals(p2) 一定是true吗
  *        正确答案:不一定
  *        
  *        如果两个对象的equals方法返回true,p1.equals(p2)==true
  *        两个对象的哈希值一定相同吗
  *        正确答案: 一定
  */  
 在 Java 应用程序执行期间，
 1.如果根据 equals(Object) 方法，两个对象是相等的，那么对这两个对象中的每个对象调用 hashCode 方法都必须生成相同的整数结果。 
 2.如果根据 equals(java.lang.Object) 方法，两个对象不相等，那么对这两个对象中的任一对象上调用 hashCode 方法不 要求一定生成不同的整数结果。 
    
    两个对象不同(对象属性值不同) equals返回false=====>两个对象调用hashCode()方法哈希值相同
    
    两个对象调用hashCode()方法哈希值不同=====>equals返回true


    两个对象不同(对象属性值不同) equals返回false=====>两个对象调用hashCode()方法哈希值不同
    
    两个对象调用hashCode()方法哈希值相同=====>equals返回true
   
   所以说两个对象哈希值无论相同还是不同,equals都可能返回true
### 并发修改异常(重点)
    描述的是：集合和迭代器同时持有同一个对象，当集合在添加，和删除集合元素时（修改呢），迭代器并不知道，所以会发生并发修改异常   
    注意：增强for也会产生并发修改异常
    如何解决： 第一： 使用普通for循环
              第二(重点):使用listIterator -->是List 特有的，其他集合不能使用  
    代码：

###  常用方法：
      a、 E set(int index, E) 修改指定索引上的元素，返回被修改之前的元素
      b、 E remove(int index) 移除指定索引上的元素，返回被删除之前的元素
      c、 add(int index, E)将元素插入到列表的指定索引上，其他元素顺移
      d、remove(int index) 删除并返回元素
             
###  数据类型：
     栈   ： 手枪的弹夹 : 手枪的压栈     ---> 喝酒   --->先进后出，后进先出
     队列 :  超市的购物，先排队，先处理   ---> 喝酒   --->先进去，先出来，后进去，后出来
     数组 :  查找快:因为底层有索引，并且是连续
            增删慢: 数组的长度的是固定的，当我们在进行增删时，会创建一个新的数组，并且将老数组中的值拷贝到新数组中
     链表：  查找慢（底层是链表，两两相连，依次往下找，直到找到为止） --->linkedList 采用二分法查找 
            增删快 :原因在于他仅仅只需要改变相邻元素的地址值
             
###   arrayList的特点
      底层是可变数组查找快:因为底层有索引，并且是连续

### 　linkedList 的特点：
       查找慢（底层是链表，两两相连，依次往下找，直到找到为止）
     Vector ： 已经被淘汰，是线程安全的，效率低，其他和arrayList 一致

###  需求：
     我想自己实现一个栈结构：-->先进后出，后进先出
    
今日内容介绍
1、Map接口
2、模拟斗地主洗牌发牌


 
 


=======================第一节课开始=============================================

### 01Map集合概述
  A:Map集合概述:
    我们通过查看Map接口描述,发现Map接口下的集合与Collection接口下的集合，它们存储数据的形式不同
    	a:Collection中的集合，元素是孤立存在的（理解为单身），向集合中存储元素采用一个个元素的方式存储。
    	
        b:Map中的集合，元素是成对存在的(理解为夫妻)。每个元素由键与值两部分组成，通过键可以找对所对应的值。
     
    	Collection中的集合称为单列集合，Map中的集合称为双列集合。
    	需要注意的是，Map中的集合不能包含重复的键，值可以重复；每个键只能对应一个值。
    Map
     |--HashMap
     |--LinkedHashMap

### 02Map接口中的常用方法 
  A:Map接口中的常用方法 
       /*
        *  Map接口中的常用方法
        *    使用Map接口的实现类 HashMap
        */
       public class MapDemo {
       	public static void main(String[] args) {
       		function_2();
       	}
       	/*
       	 *  移除集合中的键值对,返回被移除之前的值
       	 *  V remove(K)
       	 */
       	public static void function_2(){
       		Map<Integer,String> map = new HashMap<Integer, String>();
       		map.put(1, "a");
       		map.put(2, "b");
       		map.put(3, "c");
       		System.out.println(map);
       		
       		String value = map.remove(33);
       		System.out.println(value);
       		System.out.println(map);
       	}
       	
       	/*
       	 * 通过键对象,获取值对象
       	 * V get(K)
       	 * 如果集合中没有这个键,返回null
       	 */
       	public static void function_1(){
       		//创建集合对象,作为键的对象整数,值的对象存储字符串
       		Map<Integer,String> map = new HashMap<Integer, String>();
       		map.put(1, "a");
       		map.put(2, "b");
       		map.put(3, "c");
       		System.out.println(map);
       		
       		String value = map.get(4);
       		System.out.println(value);
       	}
       	
       	/*
       	 *  将键值对存储到集合中
       	 *  V put(K,V) K 作为键的对象, V作为值的对象
       	 *  存储的是重复的键,将原有的值,覆盖
       	 *  返回值一般情况下返回null,
       	 *  存储重复键的时候,返回被覆盖之前的值
       	 */
       	public static void function(){
       		//创建集合对象,HashMap,存储对象,键是字符串,值是整数
       		Map<String, Integer> map = new HashMap<String, Integer>();
       		map.put("a", 1);
       		
       		map.put("b", 2);
       		
       		map.put("c", 3);
       		
       		System.out.println(map);
       	}
       }



### 03Map集合遍历方式keySet方法
  A:Map集合遍历方式keySet方法
     1.获取Map集合中所有的键，由于键是唯一的，所以返回一个Set集合存储所有的键
     2.遍历键的Set集合，得到每一个键
     3.根据键利用get(key)去Map找所对应的值
     /*
      *  Map集合的遍历
      *    利用键获取值
      *    Map接口中定义方法keySet
      *    所有的键,存储到Set集合
      */
     public class MapDemo1 {
     	public static void main(String[] args) {
     		/*
     		 *  1. 调用map集合的方法keySet,所有的键存储到Set集合中
     		 *  2. 遍历Set集合,获取出Set集合中的所有元素 (Map中的键)
     		 *  3. 调用map集合方法get,通过键获取到值
     		 */
     		Map<String,Integer> map = new HashMap<String,Integer>();
     		map.put("a", 11);
     		map.put("b", 12);
     		map.put("c", 13);
     		map.put("d", 14);
     		
     		//1. 调用map集合的方法keySet,所有的键存储到Set集合中
     		Set<String> set = map.keySet();
     		//2. 遍历Set集合,获取出Set集合中的所有元素 (Map中的键)
     		Iterator<String> it = set.iterator();
     		while(it.hasNext()){
     			//it.next返回是Set集合元素,也就是Map中的键
     			//3. 调用map集合方法get,通过键获取到值
     			String key = it.next();
     			Integer value = map.get(key);
     			System.out.println(key+"...."+value);
     		}
     		
     		System.out.println("=======================");
     		

     		for(String key : map.keySet()){
     			Integer value = map.get(key);
     			System.out.println(key+"...."+value);
     		}
     	}
     }
    

### 04Map集合Entry对象
   A:Map集合Entry对象
     interface Map{
     	interface Entry{//Entry是Map的一个内部接口
     		           //由Map的子类的内部类实现

     	}
     }
     class HashMap{
     	static class Entry<K,V> implements Map.Entry<K,V> {//Entry对象指的就是该类的对象
            final K key;
                  V value;
     	}
     }
     在Map类设计时，提供了一个嵌套接口：Entry。
     Entry将键值对的对应关系封装成了对象。
     即键值对对象，这样我们在遍历Map集合时，就可以从每一个键值对（Entry）对象中获取对应的键与对应的值。
       a:Entry是Map接口中提供的一个静态内部嵌套接口。
       b:相关方法
     	 getKey()方法：获取Entry对象中的键
       getValue()方法：获取Entry对象中的值
       entrySet()方法：用于返回Map集合中所有的键值对(Entry)对象，以Set集合形式返回。

### 05Map集合遍历方式entrySet方法 
   A:Map集合遍历方式entrySet方法
    *
     *  Map集合获取方式
     *  entrySet方法,键值对映射关系(结婚证)获取
     *  实现步骤:
     *    1. 调用map集合方法entrySet()将集合中的映射关系对象,存储到Set集合
     *        Set<Entry <K,V> >
     *    2. 迭代Set集合
     *    3. 获取出的Set集合的元素,是映射关系对象
     *    4. 通过映射关系对象方法 getKet, getValue获取键值对
     *    
     *    创建内部类对象 外部类.内部类 = new 
     */
    public class MapDemo2 {
    	public static void main(String[] args) {
    		Map<Integer,String> map = new HashMap<Integer, String>();
    		map.put(1, "abc");
    		map.put(2, "bcd");
    		map.put(3, "cde");
    		//1. 调用map集合方法entrySet()将集合中的映射关系对象,存储到Set集合
    		Set<Map.Entry <Integer,String> >  set = map.entrySet();
    		//2. 迭代Set集合
    		Iterator<Map.Entry <Integer,String> > it = set.iterator();
    		while(it.hasNext()){
    			//  3. 获取出的Set集合的元素,是映射关系对象
    			// it.next 获取的是什么对象,也是Map.Entry对象
    			Map.Entry<Integer, String> entry = it.next();
    			//4. 通过映射关系对象方法 getKet, getValue获取键值对
    			Integer key = entry.getKey();
    			String value = entry.getValue();
    			System.out.println(key+"...."+value);
    		}
    		
    		 
    	}
    }



=======================第二节课开始============================================
### 06Map集合遍历方式增强for循环
   A:Map集合遍历方式增强for循环
     A:Map集合遍历方式entrySet方法
      *
       *  Map集合获取方式
       *  entrySet方法,键值对映射关系(结婚证)获取
       *  实现步骤:
       *    1. 调用map集合方法entrySet()将集合中的映射关系对象,存储到Set集合
       *        Set<Entry <K,V> >
       *    2. 迭代Set集合
       *    3. 获取出的Set集合的元素,是映射关系对象
       *    4. 通过映射关系对象方法 getKet, getValue获取键值对
       *    
       *    创建内部类对象 外部类.内部类 = new 
       */
      public class MapDemo2 {
      	public static void main(String[] args) {
      		Map<Integer,String> map = new HashMap<Integer, String>();
      		map.put(1, "abc");
      		map.put(2, "bcd");
      		map.put(3, "cde");
      		//1. 调用map集合方法entrySet()将集合中的映射关系对象,存储到Set集合
      		Set<Map.Entry <Integer,String> >  set = map.entrySet();
      		//2. 迭代Set集合
      		Iterator<Map.Entry <Integer,String> > it = set.iterator();
      		while(it.hasNext()){
      			//  3. 获取出的Set集合的元素,是映射关系对象
      			// it.next 获取的是什么对象,也是Map.Entry对象
      			Map.Entry<Integer, String> entry = it.next();
      			//4. 通过映射关系对象方法 getKet, getValue获取键值对
      			Integer key = entry.getKey();
      			String value = entry.getValue();
      			System.out.println(key+"...."+value);
      		}
      		
      		System.out.println("=========================");
      		for(Map.Entry<Integer, String> entry : map.entrySet()){
      			System.out.println(entry.getKey()+"..."+entry.getValue());
      		}
      	}
      }
      
      注意：Map集合不能直接使用迭代器或者foreach进行遍历。但是转成Set之后就可以使用了。
### 07HashMap集合存储和遍历
  A:HashMap集合存储和遍历
     /*
      *  使用HashMap集合,存储自定义的对象
      *  自定义对象,作为键,出现,作为值出现
      */
     public class HashMapDemo {
     	public static void main(String[] args) {
     		function_1();
     	}
     	/*
     	 * HashMap 存储自定义对象Person,作为键出现
     	 * 键的对象,是Person类型,值是字符串
     	 * 保证键的唯一性,存储到键的对象,重写hashCode equals
     	 */
     	public static void function_1(){
     		HashMap<Person, String> map = new HashMap<Person, String>();
     		map.put(new Person("a",20), "里约热内卢");
     		map.put(new Person("b",18), "索马里");
     		map.put(new Person("b",18), "索马里");
     		map.put(new Person("c",19), "百慕大");
     		for(Person key : map.keySet()){
     			String value = map.get(key);
     			System.out.println(key+"..."+value);
     		}
     		System.out.println("===================");
     		for(Map.Entry<Person, String> entry : map.entrySet()){
     			System.out.println(entry.getKey()+"..."+entry.getValue());
     		}
     	}
     	
     	/*
     	 * HashMap 存储自定义的对象Person,作为值出现
     	 * 键的对象,是字符串,可以保证唯一性
     	 */
     	public static void function(){
     		HashMap<String, Person> map = new HashMap<String, Person>();
     		map.put("beijing", new Person("a",20));
     		map.put("tianjin", new Person("b",18));
     		map.put("shanghai", new Person("c",19));
     		for(String key : map.keySet()){
     			Person value = map.get(key);
     			System.out.println(key+"..."+value);
     		}
     		System.out.println("=================");
     		for(Map.Entry<String, Person> entry : map.entrySet()){
     			String key = entry.getKey();
     			Person value = entry.getValue();
     			System.out.println(key+"..."+value);
     		}
     	}
     }


### 08LinkedHashMap的特点
   *A:LinkedHashMap的特点
	  
	  /*
	   *  LinkedHashMap继承HashMap
	   *  保证迭代的顺序
	   */
	  public class LinkedHashMapDemo {
	  	public static void main(String[] args) {
	  		LinkedHashMap<String, String> link = new LinkedHashMap<String, String>();
	  		link.put("1", "a");
	  		link.put("13", "a");
	  		link.put("15", "a");
	  		link.put("17", "a");
	  		System.out.println(link);
	  	}
	  }


### 09Hashtable的特点
   *A:Hashtable的特点
	   /*
	    *  Map接口实现类 Hashtable
	    *  底层数据结果哈希表,特点和HashMap是一样的
	    *  Hashtable 线程安全集合,运行速度慢
	    *  HashMap 线程不安全的集合,运行速度快
	    *  
	    *  Hashtable命运和Vector是一样的,从JDK1.2开始,被更先进的HashMap取代
	    *  
	    *  HashMap 允许存储null值,null键
	    *  Hashtable 不允许存储null值,null键
	    *  
	    *  Hashtable他的孩子,子类 Properties 依然活跃在开发舞台
	    */
	   public class HashtableDemo {
	   	public static void main(String[] args) {	
	   		Map<String,String> map = new Hashtable<String,String>();
	   		map.put(null, null);
	   		System.out.println(map);
	   	}
	   }


### 10静态导入
   *A:静态导入:如果本类中有和静态导入的同名方法会优先使用本类的
               如果还想使用静态导入的,依然需要类名来调用
	   /*
	    * JDK1.5新特性,静态导入
	    * 减少开发的代码量
	    * 标准的写法,导入包的时候才能使用
	    * 
	    * import static java.lang.System.out;最末尾,必须是一个静态成员
	    */
	   import static java.lang.System.out;
	   import static java.util.Arrays.sort;


	   public class StaticImportDemo {
	   	public static void main(String[] args) {
	   		out.println("hello");
	   		
	   		int[] arr = {1,4,2};
	   		sort(arr);
	   	}
	   }

### 11方法的可变参数
   *A:方法的可变参数
     /*
      *  JDK1.5新的特性,方法的可变参数
      *  前提: 方法参数数据类型确定,参数的个数任意
      *  可变参数语法: 数据类型...变量名
      *  可变参数,本质就是一个数组
      */
     public class VarArgumentsDemo {
     	public static void main(String[] args) {
     		//调用一个带有可变参数的方法,传递参数,可以任意
     	//	getSum();
     		int sum = getSum(5,34,3,56,7,8,0);
     		System.out.println(sum);
 
     	}
     
     	/*
     	 * 定义方法,计算10个整数和
     	 * 方法的可变参数实现
     	 */
     	public static int getSum(int...a){
     		int sum = 0 ;
     		for(int i : a){
     			sum = sum + i;
     		}
     		return sum;
     	}
     	
     	/*
     	 * 定义方法,计算3个整数和
     	 */
     	/*public static int getSum(int a,int b ,int c){
     		return a+b+c;
     	}*/
     	
     	/*
     	 * 定义方法,计算2个整数和
     	 */
     	/*public static int getSum(int a,int b){
     		return a+b;
     	}*/
     }



### 12可变参数的注意事项
   *A:可变参数的注意事项    
	   /*
	    * 可变参数的注意事项
	    * 1. 一个方法中,可变参数只能有一个
	    * 2. 可变参数,必须写在参数列表的最后一位
	    */
	    public static void function(Object...o){
	   	 
	    }
=======================第三节课开始=============================================
### 13Collections工具类
   A:Collections工具类
      /*
       *  集合操作的工具类
       *    Collections
       */
      public class CollectionsDemo {
      	public static void main(String[] args) {
      		function_2();
      	}
      	/*
      	 * Collections.shuffle方法
      	 * 对List集合中的元素,进行随机排列
      	 */
      	public static void function_2(){
      		List<Integer> list = new ArrayList<Integer>();
      		list.add(1);
      		list.add(5);
      		list.add(9);
      		list.add(11);
      		list.add(8);
      		list.add(10);
      		list.add(15);
      		list.add(20);	
      		System.out.println(list);
      		
      		//调用工具类方法shuffle对集合随机排列
      		Collections.shuffle(list);
      		System.out.println(list);
      	}
      	
      	/*
      	 * Collections.binarySearch静态方法
      	 * 对List集合进行二分搜索,方法参数,传递List集合,传递被查找的元素
      	 */
      	public static void function_1(){
      		List<Integer> list = new ArrayList<Integer>();
      		list.add(1);
      		list.add(5);
      		list.add(8);
      		list.add(10);
      		list.add(15);
      		list.add(20);
      		//调用工具类静态方法binarySearch
      		int index = Collections.binarySearch(list, 16);
      		System.out.println(index);
      	}
      	
      	/*
      	 *  Collections.sort静态方法
      	 *  对于List集合,进行升序排列
      	 */
      	public static void function(){
      		//创建List集合
      		List<String> list = new ArrayList<String>();
      		list.add("ewrew");
      		list.add("qwesd");
      		list.add("Qwesd");
      		list.add("bv");
      		list.add("wer");
      		System.out.println(list);
      		//调用集合工具类的方法sort
      		Collections.sort(list);
      		System.out.println(list);
      	}
      }


### 14集合的嵌套
   A:集合的嵌套
    /*
     *  Map集合的嵌套,Map中存储的还是Map集合
     *  要求:
     *    传智播客  
     *      Java基础班
     *        001  张三
     *        002  李四
     *      
     *      Java就业班
     *        001  王五
     *        002  赵六
     *  对以上数据进行对象的存储
     *   001 张三  键值对
     *   Java基础班: 存储学号和姓名的键值对
     *   Java就业班:
     *   传智播客: 存储的是班级
     *   
     *   基础班Map   <学号,姓名>
     *   传智播客Map  <班级名字, 基础班Map>
     */
    public class MapMapDemo {
    	public static void main(String[] args) {
    		//定义基础班集合
    		HashMap<String, String> javase = new HashMap<String, String>();
    		//定义就业班集合
    		HashMap<String, String> javaee = new HashMap<String, String>();
    		//向班级集合中,存储学生信息
    		javase.put("001", "张三");
    		javase.put("002", "李四");
    		
    		javaee.put("001", "王五");
    		javaee.put("002", "赵六");
    		//定义传智播客集合容器,键是班级名字,值是两个班级容器
    		HashMap<String, HashMap<String,String>> czbk =
    				new HashMap<String, HashMap<String,String>>();
    		czbk.put("基础班", javase);
    		czbk.put("就业班", javaee);
    		
    		 keySet(czbk);
    		 
    	}



   
### 15集合的嵌套keySet遍历
   A:集合的嵌套keySet遍历
	   /*
	    *  Map集合的嵌套,Map中存储的还是Map集合
	    *  要求:
	    *    传智播客  
	    *      Java基础班
	    *        001  张三
	    *        002  李四
	    *      
	    *      Java就业班
	    *        001  王五
	    *        002  赵六
	    *  对以上数据进行对象的存储
	    *   001 张三  键值对
	    *   Java基础班: 存储学号和姓名的键值对
	    *   Java就业班:
	    *   传智播客: 存储的是班级
	    *   
	    *   基础班Map   <学号,姓名>
	    *   传智播客Map  <班级名字, 基础班Map>
	    */
	   public class MapMapDemo {
	   	public static void main(String[] args) {
	   		//定义基础班集合
	   		HashMap<String, String> javase = new HashMap<String, String>();
	   		//定义就业班集合
	   		HashMap<String, String> javaee = new HashMap<String, String>();
	   		//向班级集合中,存储学生信息
	   		javase.put("001", "张三");
	   		javase.put("002", "李四");
	   		
	   		javaee.put("001", "王五");
	   		javaee.put("002", "赵六");
	   		//定义传智播客集合容器,键是班级名字,值是两个班级容器
	   		HashMap<String, HashMap<String,String>> czbk =
	   				new HashMap<String, HashMap<String,String>>();
	   		czbk.put("基础班", javase);
	   		czbk.put("就业班", javaee);
	   		
	   		 keySet(czbk);
	   		 
	   	}
	   	
	   	 
	   	
	   	public static void keySet(HashMap<String,HashMap<String,String>> czbk){
	   		//调用czbk集合方法keySet将键存储到Set集合
	   		Set<String> classNameSet = czbk.keySet();
	   		//迭代Set集合
	   		Iterator<String> classNameIt = classNameSet.iterator();
	   		while(classNameIt.hasNext()){
	   			//classNameIt.next获取出来的是Set集合元素,czbk集合的键
	   			String classNameKey = classNameIt.next();
	   			//czbk集合的方法get获取值,值是一个HashMap集合
	   			HashMap<String,String> classMap = czbk.get(classNameKey);
	   			//调用classMap集合方法keySet,键存储到Set集合
	   			Set<String> studentNum = classMap.keySet();
	   			Iterator<String> studentIt = studentNum.iterator();
	   	   
	        	   while(studentIt.hasNext()){
	   				//studentIt.next获取出来的是classMap的键,学号
	   				String numKey = studentIt.next();
	   				//调用classMap集合中的get方法获取值
	   				String nameValue = classMap.get(numKey);
	   				System.out.println(classNameKey+".."+numKey+".."+nameValue);
	   			}
	   		}
	   		
	   		System.out.println("==================================");
	   	    for(String className: czbk.keySet()){
	   	       HashMap<String, String> hashMap = czbk.get(className);	
	   	       for(String numKey : hashMap.keySet()){
	   	    	   String nameValue = hashMap.get(numKey);
	   	    	   System.out.println(className+".."+numKey+".."+nameValue);
	   	       }
	   	    }
	   	}

	   } 
      


### 16集合的嵌套entrySet遍历
    A:集合的嵌套entrySet遍历
    /*
     *  Map集合的嵌套,Map中存储的还是Map集合
     *  要求:
     *    传智播客  
     *      Java基础班
     *        001  张三
     *        002  李四
     *      
     *      Java就业班
     *        001  王五
     *        002  赵六
     *  对以上数据进行对象的存储
     *   001 张三  键值对
     *   Java基础班: 存储学号和姓名的键值对
     *   Java就业班:
     *   传智播客: 存储的是班级
     *   
     *   基础班Map   <学号,姓名>
     *   传智播客Map  <班级名字, 基础班Map>
     */
    public class MapMapDemo {
    	public static void main(String[] args) {
    		//定义基础班集合
    		HashMap<String, String> javase = new HashMap<String, String>();
    		//定义就业班集合
    		HashMap<String, String> javaee = new HashMap<String, String>();
    		//向班级集合中,存储学生信息
    		javase.put("001", "张三");
    		javase.put("002", "李四");
    		
    		javaee.put("001", "王五");
    		javaee.put("002", "赵六");
    		//定义传智播客集合容器,键是班级名字,值是两个班级容器
    		HashMap<String, HashMap<String,String>> czbk =
    				new HashMap<String, HashMap<String,String>>();
    		czbk.put("基础班", javase);
    		czbk.put("就业班", javaee);
    		
    		entrySet(czbk);
    	}
    	
    	public static void entrySet(HashMap<String,HashMap<String,String>> czbk){
    		//调用czbk集合方法entrySet方法,将czbk集合的键值对关系对象,存储到Set集合
    		Set<Map.Entry<String, HashMap<String,String>>> 
    		                         classNameSet = czbk.entrySet();
    		//迭代器迭代Set集合
    		Iterator<Map.Entry<String, HashMap<String,String>>> classNameIt = classNameSet.iterator();
    		while(classNameIt.hasNext()){
    			//classNameIt.next方法,取出的是czbk集合的键值对关系对象
    			Map.Entry<String, HashMap<String,String>> classNameEntry =  classNameIt.next();
    			//classNameEntry方法 getKey,getValue
    			String classNameKey = classNameEntry.getKey();
    			//获取值,值是一个Map集合
    			HashMap<String,String> classMap = classNameEntry.getValue();
    			//调用班级集合classMap方法entrySet,键值对关系对象存储Set集合
    			Set<Map.Entry<String, String>> studentSet = classMap.entrySet();
    			//迭代Set集合
    			Iterator<Map.Entry<String, String>> studentIt = studentSet.iterator();
    			while(studentIt.hasNext()){
    				//studentIt方法next获取出的是班级集合的键值对关系对象
    				Map.Entry<String, String> studentEntry = studentIt.next();
    				//studentEntry方法 getKey getValue
    				String numKey = studentEntry.getKey();
    				String nameValue = studentEntry.getValue();
    				System.out.println(classNameKey+".."+numKey+".."+nameValue);
    			}
    		}
    	     System.out.println("==================================");
    		
    		for (Map.Entry<String, HashMap<String, String>> me : czbk.entrySet()) {
    			String classNameKey = me.getKey();
    			HashMap<String, String> numNameMapValue = me.getValue();
    			for (Map.Entry<String, String> nameMapEntry : numNameMapValue.entrySet()) {
    				String numKey = nameMapEntry.getKey();
    				String nameValue = nameMapEntry.getValue();
    				System.out.println(classNameKey + ".." + numKey + ".." + nameValue);
    			}
    		}
    	}
    	
    
    }


=======================第四节课开始=============================================
        
### 17斗地主的功能分析
   A:斗地主的功能分析
	   a:具体规则：
		   	1. 组装54张扑克牌
		    2. 将54张牌顺序打乱
		   	3. 三个玩家参与游戏，三人交替摸牌，每人17张牌，最后三张留作底牌。
		   	4. 查看三人各自手中的牌（按照牌的大小排序）、底牌
       b:分析:
	      1.准备牌：
	       完成数字与纸牌的映射关系：
	       使用双列Map(HashMap)集合，完成一个数字与字符串纸牌的对应关系(相当于一个字典)。
	      2.洗牌：
	       通过数字完成洗牌发牌
	      3.发牌：
	       将每个人以及底牌设计为ArrayList<String>,将最后3张牌直接存放于底牌，剩余牌通过对3取模依次发牌。
	       存放的过程中要求数字大小与斗地主规则的大小对应。
	       将代表不同纸牌的数字分配给不同的玩家与底牌。
	      4.看牌：
	       通过Map集合找到对应字符展示。
	       通过查询纸牌与数字的对应关系，由数字转成纸牌字符串再进行展示。

### 18斗地主的准备牌
   A:斗地主的准备牌
     /*
      *  实现模拟斗地主的功能
      *   1. 组合牌
      *   2. 洗牌
      *   3. 发牌
      *   4. 看牌
      */
     public class DouDiZhu {
     	public static void main(String[] args) {
     		//1. 组合牌
     		//创建Map集合,键是编号,值是牌
     		HashMap<Integer,String> pooker = new HashMap<Integer, String>();
     		//创建List集合,存储编号
     		ArrayList<Integer> pookerNumber = new ArrayList<Integer>();
     		//定义出13个点数的数组
     		String[] numbers = {"2","A","K","Q","J","10","9","8","7","6","5","4","3"};
     		//定义4个花色数组
     		String[] colors = {"♠","♥","♣","♦"};
     		//定义整数变量,作为键出现
     		int index = 2;
     		//遍历数组,花色+点数的组合,存储到Map集合
     		for(String number : numbers){
     			for(String color : colors){
     				pooker.put(index, color+number);
     				pookerNumber.add(index);
     				index++;
     			}
     		}
     		//存储大王,和小王,索引是从0~54,对应大王,小王,...3(牌的顺序从大到小)
     		pooker.put(0, "大王");
     		pookerNumber.add(0);
     		pooker.put(1, "小王");
     		pookerNumber.add(1);
     	 
     }


### 19斗地主的洗牌
    A:斗地主的洗牌
	  /*
	   *  实现模拟斗地主的功能
	   *   1. 组合牌
	   *   2. 洗牌
	   *   3. 发牌
	   *   4. 看牌
	   */
	  public class DouDiZhu {
	  	public static void main(String[] args) {
	  		//1. 组合牌
	  		//创建Map集合,键是编号,值是牌
	  		HashMap<Integer,String> pooker = new HashMap<Integer, String>();
	  		//创建List集合,存储编号
	  		ArrayList<Integer> pookerNumber = new ArrayList<Integer>();
	  		//定义出13个点数的数组
	  		String[] numbers = {"2","A","K","Q","J","10","9","8","7","6","5","4","3"};
	  		//定义4个花色数组
	  		String[] colors = {"♠","♥","♣","♦"};
	  		//定义整数变量,作为键出现
	  		int index = 2;
	  		//遍历数组,花色+点数的组合,存储到Map集合
	  		for(String number : numbers){
	  			for(String color : colors){
	  				pooker.put(index, color+number);
	  				pookerNumber.add(index);
	  				index++;
	  			}
	  		}
	  		//存储大王,和小王
	  		pooker.put(0, "大王");
	  		pookerNumber.add(0);
	  		pooker.put(1, "小王");
	  		pookerNumber.add(1);
	  		
	  		//洗牌,将牌的编号打乱
	  		Collections.shuffle(pookerNumber);
	  		
	  	 
	  	}
	  	 
	  }
   

### 20斗地主的发牌
  A:斗地主的发牌
    /*
     *  实现模拟斗地主的功能
     *   1. 组合牌
     *   2. 洗牌
     *   3. 发牌
     *   4. 看牌
     */
    public class DouDiZhu {
    	public static void main(String[] args) {
    		//1. 组合牌
    		//创建Map集合,键是编号,值是牌
    		HashMap<Integer,String> pooker = new HashMap<Integer, String>();
    		//创建List集合,存储编号
    		ArrayList<Integer> pookerNumber = new ArrayList<Integer>();
    		//定义出13个点数的数组
    		String[] numbers = {"2","A","K","Q","J","10","9","8","7","6","5","4","3"};
    		//定义4个花色数组
    		String[] colors = {"♠","♥","♣","♦"};
    		//定义整数变量,作为键出现
    		int index = 2;
    		//遍历数组,花色+点数的组合,存储到Map集合
    		for(String number : numbers){
    			for(String color : colors){
    				pooker.put(index, color+number);
    				pookerNumber.add(index);
    				index++;
    			}
    		}
    		//存储大王,和小王
    		pooker.put(0, "大王");
    		pookerNumber.add(0);
    		pooker.put(1, "小王");
    		pookerNumber.add(1);
    		
    		//洗牌,将牌的编号打乱
    		Collections.shuffle(pookerNumber);
    		
    		//发牌功能,将牌编号,发给玩家集合,底牌集合
    		ArrayList<Integer> player1 = new ArrayList<Integer>();
    		ArrayList<Integer> player2 = new ArrayList<Integer>();
    		ArrayList<Integer> player3 = new ArrayList<Integer>();
    		ArrayList<Integer> bottom = new ArrayList<Integer>();
    		
    		//发牌采用的是集合索引%3
    		for(int i = 0 ; i < pookerNumber.size() ; i++){
    			//先将底牌做好
    			if(i < 3){
    				//存到底牌去
    				bottom.add( pookerNumber.get(i));
    			   //对索引%3判断
    			}else if(i % 3 == 0){
    				//索引上的编号,发给玩家1
    				player1.add( pookerNumber.get(i) );
    			}else if( i % 3 == 1){
    				//索引上的编号,发给玩家2
    				player2.add( pookerNumber.get(i) );
    			}else if( i % 3 == 2){
    				//索引上的编号,发给玩家3
    				player3.add( pookerNumber.get(i) );
    			}
    		}
    		 
    	}
    	 
    }

### 21斗地主的看牌
  A:斗地主的看牌
     /*
      *  实现模拟斗地主的功能
      *   1. 组合牌
      *   2. 洗牌
      *   3. 发牌
      *   4. 看牌
      */
     public class DouDiZhu {
     	public static void main(String[] args) {
     		//1. 组合牌
     		//创建Map集合,键是编号,值是牌
     		HashMap<Integer,String> pooker = new HashMap<Integer, String>();
     		//创建List集合,存储编号
     		ArrayList<Integer> pookerNumber = new ArrayList<Integer>();
     		//定义出13个点数的数组
     		String[] numbers = {"2","A","K","Q","J","10","9","8","7","6","5","4","3"};
     		//定义4个花色数组
     		String[] colors = {"♠","♥","♣","♦"};
     		//定义整数变量,作为键出现
     		int index = 2;
     		//遍历数组,花色+点数的组合,存储到Map集合
     		for(String number : numbers){
     			for(String color : colors){
     				pooker.put(index, color+number);
     				pookerNumber.add(index);
     				index++;
     			}
     		}
     		//存储大王,和小王
     		pooker.put(0, "大王");
     		pookerNumber.add(0);
     		pooker.put(1, "小王");
     		pookerNumber.add(1);
     		
     		//洗牌,将牌的编号打乱
     		Collections.shuffle(pookerNumber);
     		
     		//发牌功能,将牌编号,发给玩家集合,底牌集合
     		ArrayList<Integer> player1 = new ArrayList<Integer>();
     		ArrayList<Integer> player2 = new ArrayList<Integer>();
     		ArrayList<Integer> player3 = new ArrayList<Integer>();
     		ArrayList<Integer> bottom = new ArrayList<Integer>();
     		
     		//发牌采用的是集合索引%3
     		for(int i = 0 ; i < pookerNumber.size() ; i++){
     			//先将底牌做好
     			if(i < 3){
     				//存到底牌去
     				bottom.add( pookerNumber.get(i));
     			   //对索引%3判断
     			}else if(i % 3 == 0){
     				//索引上的编号,发给玩家1
     				player1.add( pookerNumber.get(i) );
     			}else if( i % 3 == 1){
     				//索引上的编号,发给玩家2
     				player2.add( pookerNumber.get(i) );
     			}else if( i % 3 == 2){
     				//索引上的编号,发给玩家3
     				player3.add( pookerNumber.get(i) );
     			}
     		}
     		//对玩家手中的编号排序
     		Collections.sort(player1);
     		Collections.sort(player2);
     		Collections.sort(player3);
     		//看牌,将玩家手中的编号,到Map集合中查找,根据键找值
     		//定义方法实现
     		look("刘德华",player1,pooker);
     		look("张曼玉",player2,pooker);
     		look("林青霞",player3,pooker);
     		look("底牌",bottom,pooker);
     	}
     	public static void look(String name,ArrayList<Integer> player,HashMap<Integer,String> pooker){
     		//遍历ArrayList集合,获取元素,作为键,到集合Map中找值
     		System.out.print(name+" ");
     		for(Integer key : player){
     			String value = pooker.get(key);
     			System.out.print(value+" ");
     		}
     		System.out.println();
     	}
     }
今日内容介绍
1、异常概述和继承体系
2、异常原因以及处理方式
3、运行时期异常
4、方法重写的异常处理
5、Throwable类常见方法
6、自定义异常



第一节课 异常的继续体系和异常处理(46:21)
### 01异常的概述.avi(01:43)
### 02异常的继续体系和错误的区别.avi(07:56)
### 03异常对象的产生原因和处理方式.avi(13:25)
### 04方法内部抛出对象throw关键字.avi(13:38)
### 05方法声明异常关键字throws.avi(09:37)


第二节课 异常处理方式讲解(42:37)
### 06(异常)try...catch异常处理.avi(19:50)
### 07(异常)多catch处理.avi(02:46)
### 08(异常)多catch处理细节.avi(10:44)
### 09(异常)finally代码块.avi(04:21)
### 10(异常)调用抛出异常方法try和throws处理方式.avi(04:54)


第三节课 运行时期异常和方法重写的异常处理(39:45)
### 11(异常)运行时期异常的特点.avi(11:00)
### 12(异常)运行异常的案例.avi(08:53)
### 13(异常)方法重写时候异常的处理.avi(11:6)
### 14(异常)Throwable类方法.avi(08:45)


第四节课 自定义异常与总结(13:32)
### 15(异常)自定义异常.avi(13:32)



============上面的内容,方便我们只做ppt,word教案以及书写下面的简要的笔记=================






=======================第一节课开始=============================================


### 01异常的概述
	* A: 异常的概述
		* a:什么是异常
			* Java代码在运行时期发生的问题就是异常。
		* b:异常类
			* 在Java中，把异常信息封装成了一个类。
			* 当出现了问题时，就会创建异常类对象并抛出异常相关的信息（如异常出现的位置、原因等）。
		* c：我们见过的异常：数组角标越界异常ArrayIndexOutOfBoundsException,空指针异常NullPointerException
		
### 02异常的继续体系和错误的区别
	* A: 异常的继承体系
		Throwable: 它是所有错误与异常的超类（祖宗类）
			|- Error 错误
			|- Exception 编译期异常,进行编译JAVA程序时出现的问题
				|- RuntimeException 运行期异常, JAVA程序运行过程中出现的问题
	* B：异常与错误的区别
		* a：异常
			* 指程序在编译、运行期间发生了某种异常(XxxException)，我们可以对异常进行具体的处理。
			* 若不处理异常，程序将会结束运行。
			* 案例演示：
				public static void main(String[] args) {
					int[] arr = new int[3];
					System.out.println(arr[0]);
					System.out.println(arr[3]);
					// 该句运行时发生了数组索引越界异常ArrayIndexOutOfBoundsException，
					// 由于没有处理异常，导致程序无法继续执行，程序结束。
					System.out.println("over"); // 由于上面代码发生了异常，此句代码不会执行
				}
				
		* b：错误
			* 指程序在运行期间发生了某种错误(XxxError)，Error错误通常没有具体的处理方式，程序将会结束运行。
			* Error错误的发生往往都是系统级别的问题，都是jvm所在系统发生的，并反馈给jvm的。
			* 我们无法针对处理，只能修正代码。
			* 案例演示：
				public static void main(String[] args) {
					int[] arr = new int[1024*1024*100];
					//该句运行时发生了内存溢出错误OutOfMemoryError，开辟了过大的数组空间，
					//导致JVM在分配数组空间时超出了JVM内存空间，直接发生错误。
				}
			
### 03异常对象的产生原因和处理方式
	* A: 异常对象的产生原因
		* 案例代码：
			* 工具类
			class ArrayTools{
				//对给定的数组通过给定的角标获取元素。
				public static int getElement(int[] arr,int index)	{
					int element = arr[index];
					return element;
				}
			}
			* 测试类
			class ExceptionDemo2 {
				public static void main(String[] args) 	{
					int[] arr = {34,12,67};
					int num = ArrayTools.getElement(arr,4)
					System.out.println("num="+num);
					System.out.println("over");
				}
			}
		* 原因分析：
			* a: 由于没找到4索引，导致运行时发生了异常。这个异常JVM认识：ArrayIndexOutOfBoundsException。
				这个异常Java本身有描述：异常的名称、异常的内容、异常的产生位置。
				java将这些信息直接封装到异常对象中。new ArrayIndexOutOfBoundsException(4);
			* b：throw new ArrayIndexOutOfBoundsException(4);产生异常对象。JVM将产生的异常抛给调用者main()方法。
			* c：main()方法接收到了数组索引越界异常对象。
				由于main()方法并没有进行处理异常，main()方法就会继续把异常抛给调用者JVM。
				当JVM收到异常后，将异常对象中的名称、异常内容、位置都显示在就控制台上。同时让程序立刻终止。
	* B：异常的处理方式
		* a：JVM的默认处理方式
			* 把异常的名称,原因,位置等信息输出在控制台，同时会结束程序。
			* 一旦有异常发生，其后来的代码不能继续执行。
		* b：解决程序中异常的手动方式
			* a)：编写处理代码 try...catch...finally
			* b)：抛出 throws

### 04方法内部抛出对象throw关键字
	在java中，提供了一个throw关键字，它用来抛出一个指定的异常对象。
	* A: 什么时候使用throw关键字？
		* 当调用方法使用接受到的参数时，首先需要先对参数数据进行合法的判断，
		  数据若不合法，就应该告诉调用者，传递合法的数据进来。
		  这时需要使用抛出异常的方式来告诉调用者。
	* B: 使用throw关键字具体操作
		* a: 创建一个异常对象。封装一些提示信息(信息可以自己编写)。
		* b: 通过关键字throw将这个异常对象告知给调用者。throw 异常对象；
		throw 用在方法内，用来抛出一个异常对象，将这个异常对象传递到调用者处，并结束当前方法的执行。
	* C: throw关键字使用格式
		* throw new 异常类名(参数);
		* 例如：
			throw new NullPointerException("要访问的arr数组不存在");
			throw new ArrayIndexOutOfBoundsException("该索引在数组中不存在，已超出范围");
	* D：案例演示
		* throw的使用

### 05方法声明异常关键字throws
	* A: 声明
		* 将问题标识出来，报告给调用者。如果方法内通过throw抛出了编译时异常，而没有捕获处理（稍后讲解该方式），那么必须通过throws进行声明，让调用者去处理。
	* B: 声明异常格式
		* 修饰符 返回值类型 方法名(参数) throws 异常类名1,异常类名2… {   }
	* C：注意事项：
		* throws用于进行异常类的声明，若该方法可能有多种异常情况产生，那么在throws后面可以写多个异常类，用逗号隔开。
	* D：代码演示：
		* 多个异常的处理
		
		
		
==============================第二节课开始====================================		


				

### 06try...catch异常处理
	* A: 捕获
		* Java中对异常有针对性的语句进行捕获，可以对出现的异常进行指定方式的处理
	* B: 捕获异常格式
		try {
			//需要被检测的语句。
		}
		catch(异常类 变量) { //参数。
			//异常的处理语句。
		}
		finally {
			//一定会被执行的语句。
		}
	* C: 格式说明
		* a: try
			* 该代码块中编写可能产生异常的代码。
		* b: catch
			* 用来进行某种异常的捕获，实现对捕获到的异常进行处理。
		* c: finally：
			* 有一些特定的代码无论异常是否发生，都需要执行。
			* 另外，因为异常会引发程序跳转，导致有些语句执行不到。
			* 而finally就是解决这个问题的，在finally代码块中存放的代码都是一定会被执行的。
		* d：try...catch...处理掉异常后，程序可以继续执行
	* D：案例演示
		* 捕获异常格式

### 07多catch处理
	* A：一个try 多个catch组合 
		* 对代码进行异常检测，并对检测的异常传递给catch处理。对每种异常信息进行不同的捕获处理。
	* B：多catch处理的格式
		void show(){ //不用throws 
			try{
				throw new Exception();//产生异常，直接捕获处理
			}catch(XxxException e){
				//处理方式	
			}catch(YyyException e){
				//处理方式	
			}catch(ZzzException e){
				//处理方式	
			}
		}
		注意事项：在捕获异常处理中，变量也是有作用域的，如可以定义多个catch中异常变量名为e。

### 08多catch处理细节			
	* A：细节：多个catch小括号中，写的是异常类的类名，有没有顺序的概念？
		* 有顺序关系。
	* B：平级异常：
		* 抛出的异常类之间,没有继承关系,没有顺序
			NullPointerException extends RuntimeException
			NoSuchElementException extends RuntimeException
			ArrayIndexOutOfBoundsException extends IndexOutOfBoundsException extends RuntimeException
	* C：上下级关系的异常
		* 越高级的父类,越写在下面
			NullPointerException extends RuntimeException extends Exception

### 09finally代码块
	* A: finally的特点
		* 被finally控制的语句体一定会执行
	* B：finally的作用
		* finally,无论程序是否有异常出现,程序必须执行释放资源在
		  如：IO流操作和数据库操作中会见到
		
### 10调用抛出异常方法try和throws处理方式
	* A: 在实际开发中使用哪种异常处理方式呢？
		* 能自己处理的尽量自己处理。(建议用try...catch)
		
		
==============================第三节课开始====================================
		
### 11运行时期异常的特点
	* A: 运行时期异常的概述: 
		* RuntimeException和他的所有子类异常,都属于运行时期异常。
			NullPointerException,ArrayIndexOutOfBoundsException等都属于运行时期异常.
	* B：运行时期异常的特点
		* a：方法中抛出运行时期异常,方法定义中无需throws声明,调用者也无需处理此异常。
		* b：运行时期异常一旦发生,需要程序人员修改源代码。
		设计原因:
			运行异常,不能发生,但是如果发生了,程序人员停止程序修改源代码
			运行异常: 一旦发生,不要处理,请你修改源代码,运行异常一旦发生,后面的代码没有执行的意义

### 12运行异常的案例
	* A: 计算圆的面积案例
		定义方法,计算圆形的面积
		传递参数0,或者负数,计算的时候没有问题
		但是,违反了真实情况
		参数小于=0, 停止程序,不要在计算了
	* B：数组索引越界案例
		使用数组中不存在的索引
		public class RuntimeExceptionDemo {
			public static void main(String[] args) {
					double d = getArea(1);
					System.out.println(d);
			}
			
			/*
			 *  定义方法,计算圆形的面积
			 *  传递参数0,或者负数,计算的时候没有问题
			 *  但是,违反了真实情况
			 *  参数小于=0, 停止程序,不要在计算了
			 */
			public static double getArea(double r){
				if(r <= 0)
					throw new RuntimeException("圆形不存在");
				return r*r*Math.PI;
			}
			
			public static void function(){
				int[] arr = {1,2,3};
				//对数组的5索引进行判断,如果5索引大于100,请将5索引上的数据/2,否则除以3
				//索引根本就没有
				if(arr[5] > 100){
					arr[5] = arr[5]/2;
				}else{
					arr[5] = arr[5]/3;
				}
		}

### 13方法重写时候异常的处理
	* A：方法重写时候异常的处理
		* a：子类覆盖父类方法时，如果父类的方法声明异常，子类只能声明父类异常或者该异常的子类，或者不声明。
			例如：
			class Fu {
				public void method () throws RuntimeException {
				}
			}
			class Zi extends Fu {
				public void method() throws RuntimeException { }  //抛出父类一样的异常
				//public void method() throws NullPointerException{ } //抛出父类子异常
			}
		* b：当父类方法声明多个异常时，子类覆盖时只能声明多个异常的子集。
			例如：
			class Fu {
				public void method () throws NullPointerException, ClassCastException{
				}
			}
			class Zi extends Fu {
				public void method()throws NullPointerException, ClassCastException { }  		
				public void method() throws NullPointerException{ } //抛出父类异常中的一部分
				public void method() throws ClassCastException { } //抛出父类异常中的一部分
			}
		* c：当被覆盖的方法没有异常声明时，子类覆盖时无法声明异常的。
			例如：
			class Fu {
				public void method (){
				}
			}
			class Zi extends Fu {
				public void method() throws Exception { }//错误的方式
			}
	* B：问题：父类中会存在下列这种情况，接口也有这种情况。
				接口中没有声明异常，而实现的子类覆盖方法时发生了异常，怎么办？
		 回答：无法进行throws声明，只能catch的捕获。
				万一问题处理不了呢？catch中继续throw抛出，但是只能将异常转换成RuntimeException子类抛出。
				
### 14Throwable类方法
	* A: 常见方法
		* a：getMessage()方法
			返回该异常的详细信息字符串，即异常提示信息
		* b：toString()方法
			返回该异常的名称与详细信息字符串
		* c：printStackTrace()方法
			在控制台输出该异常的名称与详细信息字符串、异常出现的代码位置
	* B：案例演示
		异常的常用方法代码演示
			try {
				Person p= null;
				if (p==null) {
					throw new NullPointerException(“出现空指针异常了，请检查对象是否为null”);
				}
			} catch (NullPointerException e) {
				String message = e.getMesage();
				System.out.println(message ); 
				
				String result = e.toString();
				System.out.println(result);	
				
				e.printStackTrace(); 
			}
			
			
			
======================第四节课开始=========



### 15自定义异常
	* A: 自定义异常的定义
		* a：通过阅读源码，发现规律：
			每个异常中都调用了父类的构造方法，把异常描述信息传递给了父类，让父类帮我们进行异常信息的封装。
		* b：格式：
			Class 异常名 extends Exception{ //或继承RuntimeException
				public 异常名(){
				}
				public 异常名(String s){ 
					super(s); 
				}
			}	
		
		* c：自定义异常继承Exception演示
		* d：自定义异常继承RuntimeException演示
	* B：自定义异常的练习
		在Person类的有参数构造方法中，进行年龄范围的判断，
		若年龄为负数或大于200岁，则抛出NoAgeException异常，异常提示信息“年龄数值非法”。
		要求：在测试类中，调用有参数构造方法，完成Person对象创建，并进行异常的处理。

	* C：关于构造方法抛出异常总结
		构造函数到底抛出这个NoAgeException是继承Exception呢？还是继承RuntimeException呢？
		* a：继承Exception，必须要throws声明，一声明就告知调用者进行捕获，一旦问题处理了调用者的程序会继续执行。
		* b：继承RuntimeExcpetion,不需要throws声明的，这时调用是不需要编写捕获代码的，因为调用根本就不知道有问题。
			一旦发生NoAgeException，调用者程序会停掉，并有jvm将信息显示到屏幕，让调用者看到问题，修正代码。
		
		
### 16总结
* 把今天的知识点总结一遍。
今日内容介绍
1、File
2、递归

=======================第一节课开始=============================================


### 01IO技术概述.avi（02:49）
	* A:IO技术概述
		* a: Output
			* 把内存中的数据存储到持久化设备上这个动作称为输出（写）Output操作
		* b: Input
			* 把持久设备上的数据读取到内存中的这个动作称为输入（读）Input操作
		* c: IO操作
			* 把上面的这种输入和输出动作称为IO操作
	
### 02File类的概述和作用
	* A:File类的概述和作用
		* a: File的概念
			* File类是文件和目录路径名的抽象表示形式
			* Java中把文件或者目录（文件夹）都封装成File对象
			* 我们要去操作硬盘上的文件，或者文件夹只要找到File这个类即可
			
### 03File类静态的成员变量
	* A:File类静态的成员变量
		* a: pathSeparator
			* 与系统有关的路径分隔符，为了方便，它被表示为一个字符串
		* b: separator
			* 与系统有关的默认名称分隔符，为了方便，它被表示为一个字符串
			
		* c: 案例代码
		
			/*
			 *  java.io.File
			 *    将操作系统中的,文件,目录(文件夹),路径,封装成File对象
			 *    提供方法,操作系统中的内容
			 *    File与系统无关的类
			 *    文件 file
			 *    目录 directory
			 *    路径 path
			 */
			public class FileDemo {
				public static void main(String[] args) {
					//File类静态成员变量
					//与系统有关的路径分隔符
					String separator = File.pathSeparator;
					System.out.println(separator);// 是一个分号,目录的分割(window中环境变量配置各个路径用分号分割，表示一个完整的路径结束)  Linux中是冒号 :
					
					//与系统有关的默认名称分隔符
					separator = File.separator;
					System.out.println(separator);// 向右 \  目录名称分割  Linux / 
				}
			}

	

### 04File类构造方法_1
	* A: File类构造方法_1
		* a: File(String pathname)
			* 通过将给定路径名字符串转换为一个File对象,之后可以使用File中的方法
			* windows中的路径或文件名不区分大小写
		* d: 案例代码
			public class FileDemo1 {
				public static void main(String[] args) {
					function();
				}
				/*
				 *  File(String pathname)
				 *  传递路径名: 可以写到文件夹,可以写到一个文件
				 *  c:\\abc   c:\\abc\\Demo.java
				 *  将路径封装File类型对象
				 */
				public static void function(){
					File file = new File("d:\\eclipse");
					System.out.println(file);
				}
			}

### 05相对路径和绝对路径
	* A: 相对路径和绝对路径
		* a: 绝对路径
			* 绝对路径是一个固定的路径,从盘符开始
		* b: 相对路径
			* 相对路径相对于某个位置,在eclipse下是指当前项目下	
		* c: 路径
				绝对路径
					在系统中具有唯一性
					c:\\windows\\system32
				相对路径
					表示路径之间的关系
					D:\\develop\\Java\\jdk1.7.0_72\\bin
					D:\\develop\\Java\\jre7
					路径之间关系
						Java 父目录是D:\\develop
						Java 子目录是：jdk1.7.0_72
					父路径是 唯一性
					子目录是可以多个


			
### 06File类的构造方法_2
	* A: File类的构造方法_2
		* a:File(String parent, String child) 
			* 根据 parent 路径名字符串和 child 路径名字符串创建一个新 File 对象
							
		* b: File(File parent, String child)
		
		* c: 案例代码
		public class FileDemo1 {
			public static void main(String[] args) {
				function_2();
			}
			/*
			 *  File(File parent,String child)
			 *  传递路径,传递File类型父路径,字符串子路径
			 *  好处: 父路径是File类型,父路径可以直接调用File类方法
			 */
			public static void function_2(){
				File parent = new File("d:");
				File file = new File(parent,"eclipse");
				System.out.println(file);
			}
			
			/*
			 *  File(String parent,String child)
			 *  传递路径,传递字符串父路径,字符串子路径
			 *  好处: 单独操作父路径和子路径
			 */
			public static void function_1(){
				File file = new File("d:","eclipse");
				System.out.println(file);
			}
		}

			
### 07File类创建文件功能
	* A: File类创建文件功能
		* a: public boolean createNewFile()
			* 创建文件 如果存在这样的文件，就不创建了
				
		* b: 案例代码
			public class FileDemo2 {
				public static void main(String[] args)throws IOException {
					function();
				}						
				/*
				 *  File创建文件的功能
				 *  boolean createNewFile()
				 *  创建的文件路径和文件名,在File构造方法中给出
				 *  文件已经存在了,不在创建
				 */
				public static void function()throws IOException{
					File file = new File("c:\\a.txt");
					boolean b = file.createNewFile();
					System.out.println(b);
				}
			}

						
### 08File类创建目录功能
	* A: File类创建目录功能
		* a: 创建目录
			* public boolean mkdir():创建文件夹 如果存在这样的文件夹，就不创建了
			* public boolean mkdirs():创建文件夹,如果父文件夹不存在，会帮你创建出来
		* b: 案例代码
			public class FileDemo2 {
				public static void main(String[] args)throws IOException {
					function_1();
				}
				/*
				 *  File创建文件夹功能
				 *  boolean mkdirs() 创建多层文件夹
				 *  创建的路径也在File构造方法中给出
				 *  文件夹已经存在了,不在创建
				 */
				public static void function_1(){
					File file = new File("c:\\abc");
					boolean b = file.mkdirs();
					System.out.println(b);
				}				
			}



### 09File类删除功能
	* A: File类删除功能
		* a: 删除功能
			* public boolean delete():删除文件或者文件夹
	* B: 案例代码
		public class FileDemo2 {
			public static void main(String[] args)throws IOException {
				function_2();
			}
			/*
			 *  File类的删除功能
			 *  boolean delete()
			 *  删除的文件或者是文件夹,在File构造方法中给出
			 *  删除成功返回true,删除失败返回false
			 *  删除方法,不走回收站,直接从硬盘中删除
			 *  删除有风险,运行需谨慎
			 */
			public static void function_2(){
				File file = new File("c:\\a.txt");
				boolean b = file.delete();
				System.out.println(b);
			}			
		}
		
### 10File类获取功能			
	* A：File类获取功能
		* a: 方法介绍
			* String getName(): 返回路径中表示的文件或者文件夹名
				* 获取路径中的最后部分的名字
			* long length(): 返回路径中表示的文件的字节数
			* String getAbsolutePath(): 获取绝对路径,返回String对象
			* File   getAbsoluteFile() : 获取绝对路径,返回File对象
				* eclipse环境中,写一个相对路径,绝对位置工程根目录
			* String getParent(): 获取父路径,返回String对象
			* File getParentFile(): 获取父路径,返回File对象
					
		* b: 案例代码
		
			public class FileDemo3 {
				public static void main(String[] args) {
					function_3();
				}
				/*
				 * File类的获取功能
				 * String getParent() 返回String对象
				 * File getParentFile()返回File对象
				 * 获取父路径
				 */
				public static void function_3(){
					File file = new File("d:\\eclipse\\eclipse.exe");
					File parent = file.getParentFile();
					System.out.println(parent);
				}
				
				/*
				 * File类获取功能
				 * String getAbsolutePath() 返回String对象
				 * File   getAbsoluteFile() 返回File对象
				 * 获取绝对路径
				 * eclipse环境中,写的是一个相对路径,绝对位置工程根目录
				 */
				public static void function_2(){
					File file = new File("src");
					File absolute = file.getAbsoluteFile();
					System.out.println(absolute);
				}
				
				/*
				 * File类获取功能
				 * long length()
				 * 返回路径中表示的文件的字节数
				 */
				public static void function_1(){
					File file = new File("d:\\eclipse\\eclipse.exe");
					long length = file.length();
					System.out.println(length);
				}
				
				/*
				 *  File类的获取功能
				 *  String getName()
				 *  返回路径中表示的文件或者文件夹名
				 *  获取路径中的最后部分的名字
				 */
				public static void function(){
					File file = new File("d:\\eclipse\\eclipse.exe");
					String name = file.getName();
					System.out.println(name);
					
					/*String path = file.getPath();
					System.out.println(path);*/
			//		System.out.println(file);
				}
			}

				
### 11File类判断功能
	* A: File类判断功能
		* a: 方法介绍
			* boolean exists(): 判断File构造方法中封装路径是否存在
				* 存在返回true,不存在返回false
			* boolean isDirectory(): 判断File构造方法中封装的路径是不是文件夹
				* 如果是文件夹,返回true,不是文件返回false
			* boolean isFile(): 判断File构造方法中封装的路径是不是文件
				* 如果是文件,返回true,不是文件返回false
	
		* b: 案例代码
			public class FileDemo4 {
				public static void main(String[] args) {
					function_1();
				}
				/*
				 *  File判断功能
				 *  boolean isDirectory()
				 *  判断File构造方法中封装的路径是不是文件夹
				 *  如果是文件夹,返回true,不是文件返回false
				 *  
				 *  boolean isFile()
				 *  判断File构造方法中封装的路径是不是文件
				 */
				public static void function_1(){
					File file = new File("d:\\eclipse\\eclipse.exe");
					if(file.exists()){
						boolean b = file.isDirectory();
						System.out.println(b);
					}
				}
				
				/*
				 *  File判断功能
				 *  boolean exists()
				 *  判断File构造方法中封装路径是否存在
				 *  存在返回true,不存在返回false
				 */
				public static void function(){
					File file = new File("src");
					boolean b = file.exists();
					System.out.println(b);
				}
			}


### 12File类list获取功能
	* A: File类list获取功能
		* a: 方法介绍
			* String[] list()：获取到File构造方法中封装的路径中的文件和文件夹名 (遍历一个目录)
				* 返回只有名字
			* File[] listFiles()：获取到,File构造方法中封装的路径中的文件和文件夹名 (遍历一个目录)
				* 返回的是目录或者文件的全路径
			* static File[] listRoots(): 列出可用的文件系统根 
		
		* b: 案例代码
			public class FileDemo {
				public static void main(String[] args) {
					function_2();
				}
				public static void function_2(){
					//获取系统中的所有根目录
					File[] fileArr = File.listRoots();
					for(File f : fileArr){
						System.out.println(f);
					}
				}
				
				/*
				 *  File类的获取功能
				 *  File[] listFiles()
				 *  获取到,File构造方法中封装的路径中的文件和文件夹名 (遍历一个目录)
				 *  返回的是目录或者文件的全路径
				 */
				public static void function_1(){
					File file = new File("d:\\eclipse");
					File[] fileArr = file.listFiles();
					for(File f : fileArr){
						System.out.println(f);
					}
				}
				
				/*
				 *  File类的获取功能
				 *  String[] list()
				 *  获取到,File构造方法中封装的路径中的文件和文件夹名 (遍历一个目录)
				 *  返回只有名字
				 */
				public static void function(){
					File file = new File("c:");
					String[] strArr = file.list();
					System.out.println(strArr.length);
					for(String str : strArr){
						System.out.println(str);
					}
				}
			}

### 13文件过滤器
	* A: 文件过滤器
		* a: 作用
			* 过滤一个目录下的指定扩展名的文件，或者包含某些关键字的文件夹
			
		* b: 方法介绍
			* public String[] list(FilenameFilter filter)
			* public File[] listFiles(FileFilter filter)
			
		* C: 案例代码	
			/*
			 *  自定义过滤器
			 *  实现FileFilter接口,重写抽象方法
			 */
			public class MyFilter implements FileFilter{
				public boolean accept(File pathname)  {
					/*
					 * pathname 接受到的也是文件的全路径
					 * c:\\demo\\1.txt
					 * 对路径进行判断,如果是java文件,返回true,不是java文件,返回false
					 * 文件的后缀结尾是.java
					 */
					//String name = pathname.getName();
					return pathname.getName().endsWith(".java");
					
				}
			}
			
			/*
			 *  File类的获取,文件获取过滤器
			 *  遍历目录的时候,可以根据需要,只获取满足条件的文件
			 *  遍历目录方法 listFiles()重载形式
			 *  listFiles(FileFilter filter)接口类型
			 *  传递FileFilter接口的实现类
			 *  自定义FileFilter接口实现类,重写抽象方法,
			 *  接口实现类对象传递到遍历方法listFiles
			 */
			public class FileDemo1 {
				public static void main(String[] args) {
					File file = new File("c:\\demo");
					File[] fileArr = file.listFiles(new MyFilter());
					for(File f : fileArr){
						System.out.println(f);
					}
				}
			}
				
### 14文件过滤器_原理分析
	* A:文件过滤器_原理分析
		* listFiles()遍历目录的同时，获取到了文件名全路径，调用过滤器的方法accept，将获取到的路径传递给accept方法的参数pathname
		* accept方法接收了参数pathname，参数是listFiles传递来的
		* 在accept方法中，进行判断，如果这个路径是Java文件，返回true，走着返回false
		* 一旦方法返回了true
		* listFiles将路径保存到File数组中
	
### 15递归遍历全目录
	* A: 递归遍历全目录
		* a: 案例代码
			/*
			 *  对一个目录的下的所有内容,进行完全的遍历
			 *  编程技巧,方法的递归调用,自己调用自己
			 */
			public class FileDemo {
				public static void main(String[] args) {
					File dir = new File("d:\\eclipse");
					getAllDir(dir);
				}
				/*
				 *  定义方法,实现目录的全遍历
				 */
				public static void getAllDir(File dir){
					System.out.println(dir);
					//调用方法listFiles()对目录,dir进行遍历
					File[] fileArr = dir.listFiles();
					for(File f : fileArr){
						//判断变量f表示的路径是不是文件夹
						if(f.isDirectory()){
							//是一个目录,就要去遍历这个目录
							//本方法,getAllDir,就是给个目录去遍历
							//继续调用getAllDir,传递他目录
							getAllDir(f);
						}else{
							System.out.println(f);
						}
					}
				}
			}


		
### 16递归概念和注意事项
	* A:递归概念和注意事项
		* a: 递归概念
			* 递归，指在当前方法内调用自己的这种现象
			* 递归分为两种，直接递归和间接递归
			* 直接递归称为方法自身调用自己。间接递归可以A方法调用B方法，B方法调用C方法，C方法调用A方法
		* b: 注意事项
			* 递归一定要有出口, 必须可以让程序停下
			* 递归次数不能过多
			* 构造方法,禁止递归
		
### 17递归求和计算
	* A: 递归求和计算
		* a: 题目分析
			* 1+2+3+...+(n-1)+n:求1到n的和
			* 总结规律：1到n的和等于1到(n-1)的和再加n
			* getSum(n-1)+ n
			* 递归出口：getSum(1) return 1;
		
		* b: 案例代码	
			/*
			 *  方法的递归调用
			 *    方法自己调用自己
			 *  适合于,方法中运算的主体不变,但是运行的时候,参与运行的方法参数会变化
			 *  注意:
			 *     递归一定要有出口, 必须可以让程序停下
			 *     递归次数不能过多
			 *     构造方法,禁止递归
			 */
			public class DiGuiDemo {
				public static void main(String[] args) {
					int sum = getSum(3);
					System.out.println(sum);
				}

						
				/*
				 *  计算 1+2+3+100和 = 5050
				 *  计算规律:
				 *    n+(n-1)+(n-2)
				 *    100+(100-1)+(99-1)+...1
				 */
				public static int getSum(int n){
					if( n == 1)
						return 1;
					return n + getSum(n-1);
				}
				
			}
			
### 18递归求阶乘
	* A: 递归求和计算
		* a: 题目分析
			* 5!=5*4*3*2*1
			*   =5*4!
			* 4!=4*3!
			* 3!=3*2!
			* 2!=2*1!
			* 1!=1
			* n!=n*(n-1)!
			* 递归出口：n*getJieCheng(n-1):  getJieCheng(1) return 1;
		* b: 案例代码
			/*
			 *  方法的递归调用
			 *    方法自己调用自己
			 *  适合于,方法中运算的主体不变,但是运行的时候,参与运行的方法参数会变化
			 *  注意:
			 *     递归一定要有出口, 必须可以让程序停下
			 *     递归次数不能过多
			 *     构造方法,禁止递归
			 */
			public class DiGuiDemo {
				public static void main(String[] args) {					
					System.out.println(getJieCheng(5));
					
				}
								
				/* 
				 *  计算阶乘 5!
				 *   5*4*3*2*1
				 */
				public static int getJieCheng(int n){
					if ( n == 1)
						return 1;
					return n * getJieCheng(n-1);
				}								
			}
### 19递归计算斐波那契数列
	* A: 递归计算斐波那契数列
		* a：题目分析
			* 1 1 2 3 5 8 13 21
			* 从第三项开始，后面的每一项都等于前面两项的和，第一项和第二项的值为1，作为程序的出口
		* b: 案例代码
			/*
			 *  方法的递归调用
			 *    方法自己调用自己
			 *  适合于,方法中运算的主体不变,但是运行的时候,参与运行的方法参数会变化
			 *  注意:
			 *     递归一定要有出口, 必须可以让程序停下
			 *     递归次数不能过多
			 *     构造方法,禁止递归
			 */
			public class DiGuiDemo {
				public static void main(String[] args) {					
					System.out.println(getFBNQ(12));
				}
				/*
				 *  方法递归,计算斐波那契数列
				 *  
				 */
				public static int getFBNQ(int month){
					if( month == 1)
						return 1;
					if( month == 2)
						return 1;
					return getFBNQ(month-1)+getFBNQ(month-2);
				}
			}
### 20遍历目录下的所有java文件
	* A: 遍历目录下的所有java文件
		* a: 案例代码
			public class MyJavaFilter implements FileFilter {
				public boolean accept(File pathname) {
					//判断获取的是目录,直接返回true
					if(pathname.isDirectory())
						return true;
					return pathname.getName().toLowerCase().endsWith(".java");
				}

			}
			/*
			 *  遍历目录,获取目录下的所有.java文件
			 *  遍历多级目录,方法递归实现
			 *  遍历的过程中,使用过滤器
			 */
			public class FileDemo1 {
				public static void main(String[] args) {
					getAllJava(new File("c:\\demo"));
			//		new File("c:\\demo").delete();
				}
				/*
				 * 定义方法,实现遍历指定目录
				 * 获取目录中所有的.java文件
				 */
				public static void getAllJava(File dir){
					//调用File对象方法listFiles()获取,加入过滤器
					File[] fileArr = dir.listFiles(new MyJavaFilter());
					for(File f : fileArr){
						//对f路径,判断是不是文件夹
						if(f.isDirectory()){
							//递归进入文件夹遍历
							getAllJava(f);
						}else{
							System.out.println(f);
						}
					}
				}
			}
			
### 21总结
	* 把今天的知识点总结一遍。
今日内容介绍
1、字节流
2、字符流


=======================第一节课开始=============================================


### 01输入和输出

	* A:输入和输出
		* a: 参照物
			* 到底是输入还是输出，都是以Java程序为参照
		* b: Output
			* 把内存中的数据存储到持久化设备上这个动作称为输出（写）Output操作
			* 程序到文件称为输出
		* c: Input
			* 把持久设备上的数据读取到内存中的这个动作称为输入（读）Input操作
			* 文件到程序称为输入
		* d: IO操作
			* 把上面的这种输入和输出动作称为IO操作
	
### 02字节输出流OutputStream
	* A: 字节输出流OutputStream
		* a.概念
			* IO流用来处理设备之间的数据传输
			* Java对数据的操作是通过流的方式
			* Java用于操作流的类都在IO包中
			* 流按流向分为两种：输入流，输出流。
			* 流按操作类型分为两种：
				* 字节流 : 字节流可以操作任何数据,因为在计算机中任何数据都是以字节的形式存储的
				* 字符流 : 字符流只能操作纯字符数据，比较方便。
		* b.IO流常用父类
			* 字节流的抽象父类：
				* InputStream 
				* OutputStream
			* 字符流的抽象父类：
				* Reader 
				* Writer		
		* c.IO程序书写
			* 使用前，导入IO包中的类
			* 使用时，进行IO异常处理
			* 使用后，释放资源
		* d: 方法介绍
			*  void close(): 关闭此输出流并释放与此流有关的所有系统资源。
			*  void write(byte[] b)： 将 b.length 个字节从指定的 byte 数组写入此输出流
			*  void write(byte[] b, int off, int len) ：将指定 byte 数组中从偏移量 off 开始的 len 个字节写入此输出流。
			* abstract  void write(int b) ： 将指定的字节写入此输出流。
 
				
			
### 03字节输出流FileOutputStream写字节
	* A: 字节输出流FileOutputStream写字节
		* a: FileOutputStream
			* 写入数据文件,学习父类方法,使用子类对象
		* b: FileOutputStream构造方法
			* 作用：绑定输出的输出目的
			* FileOutputStream(File file) 
				* 创建一个向指定 File 对象表示的文件中写入数据的文件输出流。
			* FileOutputStream(File file, boolean append) 
				* 创建一个向指定 File 对象表示的文件中写入数据的文件输出流，以追加的方式写入。
			* FileOutputStream(String name) 
				* 创建一个向具有指定名称的文件中写入数据的输出文件流。
			* FileOutputStream(String name, boolean append) 
				* 创建一个向具有指定 name 的文件中写入数据的输出文件流，以追加的方式写入。
		* c: 流对象使用步骤
			*  1. 创建流子类的对象,绑定数据目的
			*  2. 调用流对象的方法write写
			*  3. close释放资源
		* d: 注意事项
			* 流对象的构造方法,可以创建文件,如果文件存在,直接覆盖
			
		* e: 案例代码
		
			/*
			 *   FileOutputStream
			 *   写入数据文件,学习父类方法,使用子类对象
			 *   
			 *   子类中的构造方法: 作用:绑定输出的输出目的
			 *     参数:
			 *       File    封装文件
			 *       String  字符串的文件名
			 *   
			 *   流对象使用步骤
			 *     1. 创建流子类的对象,绑定数据目的
			 *     2. 调用流对象的方法write写
			 *     3. close释放资源
			 *     
			 *    流对象的构造方法,可以创建文件,如果文件存在,直接覆盖
			 */
			public class FileOutputStreamDemo {
				public static void main(String[] args)throws IOException {
					FileOutputStream fos = new FileOutputStream("c:\\a.txt");
					//流对象的方法write写数据
					//写1个字节
					fos.write(97);
					//关闭资源
					fos.close();
					
				}
			}


	

### 04字节输出流FileOutputStream写字节数组
	* A: 字节输出流FileOutputStream写字节数组
		* a: 方法介绍
			*  void write(byte[] b)： 将 b.length 个字节从指定的 byte 数组写入此输出流
			*  void write(byte[] b, int off, int len) ：将指定 byte 数组中从偏移量 off 开始的 len 个字节写入此输出流。
		* b: 案例代码
			/*
			 *   FileOutputStream
			 *   写入数据文件,学习父类方法,使用子类对象
			 *   
			 *   子类中的构造方法: 作用:绑定输出的输出目的
			 *     参数:
			 *       File    封装文件
			 *       String  字符串的文件名
			 *   
			 *   流对象使用步骤
			 *     1. 创建流子类的对象,绑定数据目的
			 *     2. 调用流对象的方法write写
			 *     3. close释放资源
			 *     
			 *    流对象的构造方法,可以创建文件,如果文件存在,直接覆盖
			 */
			public class FileOutputStreamDemo {
				public static void main(String[] args)throws IOException {
					FileOutputStream fos = new FileOutputStream("c:\\a.txt");
					//流对象的方法write写数据
					//写字节数组
					byte[] bytes = {65,66,67,68};
					fos.write(bytes);
					
					//写字节数组的一部分,开始索引,写几个
					fos.write(bytes, 1, 2);
					
					//写入字节数组的简便方式
					//写字符串
					fos.write("hello".getBytes());

					//关闭资源
					fos.close();
					
				}
			}


### 05文件的续写和换行符号
	* A: 文件的续写和换行符号
		* a: 文件的续写
			*  FileOutputStream构造方法, 的第二个参数中,加入true
		* b: 换行符号
			* 在文件中,写入换行,符号换行  \r\n
			* \r\n 可以写在上一行的末尾, 也可以写在下一行的开头
		* c: 案例代码
				/*
				 *  FileOutputStream 文件的续写和换行问题
				 *  续写: FileOutputStream构造方法, 的第二个参数中,加入true
				 *  在文件中,写入换行,符号换行  \r\n
				 *  \r\n 可以写在上一行的末尾, 也可以写在下一行的开头
				 */
				public class FileOutputStreamDemo1 {
					public static void main(String[] args)throws IOException {
						File file = new File("c:\\b.txt");
						FileOutputStream fos = new FileOutputStream(file,true);
						fos.write("hello\r\n".getBytes());
						fos.write("world".getBytes());
						fos.close();
					}
				}


			
### 06IO中的异常处理
	* A: IO中的异常处理
		* a:IO流的异常处理
			* try catch finally
							
		* b: 细节
			* 1. 保证流对象变量,作用域足够
			* 2. catch里面,怎么处理异常
				* 输出异常的信息,目的看到哪里出现了问题
				* 停下程序,从新尝试
			* 3. 如果流对象建立失败了,需要关闭资源吗
				* new 对象的时候,失败了,没有占用系统资源
				* 释放资源的时候,对流对象判断null
				* 变量不是null,对象建立成功,需要关闭资源
		
		* c: 案例代码
			public class FileOutputStreamDemo3 {
				public static void main(String[] args) {
					//try 外面声明变量,try 里面建立对象
					FileOutputStream fos = null;
					try{
						fos = new FileOutputStream("s:\\a.txt");
						fos.write(100);
					}catch(IOException ex){
						System.out.println(ex);
						throw new RuntimeException("文件写入失败,重试");
					}finally{
						try{
							if(fos!=null)
							  fos.close();
						}catch(IOException ex){
							throw new RuntimeException("关闭资源失败");
						}
					}
				}
			}


			
### 07字节输入流InputStream
	* A: 字节输入流InputStream
		* a: 方法介绍
			* abstract  int read() ：
				* 从输入流中读取数据的下一个字节。
			* int read(byte[] b)  
				* 从输入流中读取一定数量的字节，并将其存储在缓冲区数组 b 中。
			* int read(byte[] b, int off, int len) 
				* 将输入流中最多 len 个数据字节读入 byte 数组。
			* void close() 
				* 关闭此输入流并释放与该流关联的所有系统资源。
				
				
		* b: 案例代码
			/*
			 *   字节输入流
			 *     java.io.InputStream 所有字节输入流的超类
			 *   作用: 读取任意文件,每次只读取1个字节
			 *   读取的方法  read
			 *     int  read() 读取1个字节
			 *     int  read(byte[] b) 读取一定量的字节,存储到数组中
			 */
			public class InputStreamDemo {

			}

						
### 08字节输入流FileInputStream读取字节
	* A: 字节输入流FileInputStream读取字节
		* a: 方法介绍
			* abstract  int read() ：
				* 从输入流中读取数据的下一个字节，返回-1表示文件结束
			* int read(byte[] b)  
				* 从输入流中读取一定数量的字节，并将其存储在缓冲区数组 b 中。
				* 读入缓冲区的字节总数，如果因为已经到达文件末尾而没有更多的数据，则返回 -1。
			* int read(byte[] b, int off, int len) 
				* 将输入流中最多 len 个数据字节读入 byte 数组。
			* void close() 
				* 关闭此输入流并释放与该流关联的所有系统资源。
		* b: 案例代码
			/*
			 *  FileInputStream读取文件
			 *  
			 *  构造方法: 为这个流对象绑定数据源
			 *  
			 *    参数: 
			 *      File 类型对象
			 *      String 对象
			 *   输入流读取文件的步骤
			 *     1. 创建字节输入流的子类对象
			 *     2. 调用读取方法read读取
			 *     3. 关闭资源
			 *     
			 *     read()方法,
			 *       read()执行一次,就会自动读取下一个字节
			 *       返回值,返回的是读取到的字节, 读取到结尾返回-1
			 */
			public class FileInputStreamDemo {
				public static void main(String[] args) throws IOException{
					FileInputStream fis = new FileInputStream("c:\\a.txt");
					//读取一个字节,调用方法read 返回int
					//使用循环方式,读取文件,  循环结束的条件  read()方法返回-1
					int len = 0;//接受read方法的返回值
				
					while( (len = fis.read()) != -1){
						System.out.print((char)len);
					}
					//关闭资源
					fis.close();
				}
			}

			/*
			 * int i = fis.read();
					System.out.println(i);
					
					i = fis.read();
					System.out.println(i);
					
					i = fis.read();
					System.out.println(i);
					
					i = fis.read();
					System.out.println(i);
			 */



### 09字节输入流FileInputStream读取字节数组
	* A: 字节输入流FileInputStream读取字节数组
		* a: 方法介绍
			* int read(byte[] b)  
				* 从输入流中读取一定数量的字节，并将其存储在缓冲区数组 b 中。
				* 读入缓冲区的字节总数，如果因为已经到达文件末尾而没有更多的数据，则返回 -1。
			* int read(byte[] b, int off, int len) 
				* 将输入流中最多 len 个数据字节读入 byte 数组。
		* b: 案例代码
			/*
			 *  FileInputStream读取文件
			 *   读取方法  int read(byte[] b) 读取字节数组
			 *   数组作用: 缓冲的作用, 提高效率
			 *   read返回的int,表示什么含义 读取到多少个有效的字节数
			 */
			public class FileInputStreamDemo1 {
				public static void main(String[] args) throws IOException {
					FileInputStream fis = new FileInputStream("c:\\a.txt");
					// 创建字节数组
					byte[] b = new byte[2];

					int len = fis.read(b);
					System.out.println(new String(b));// ab
					System.out.println(len);// 2

					len = fis.read(b);
					System.out.println(new String(b));// cd
					System.out.println(len);// 2

					len = fis.read(b);
					System.out.println(new String(b));// ed
					System.out.println(len);// 1

					len = fis.read(b);
					System.out.println(new String(b));// ed
					System.out.println(len);// -1

					fis.close();
				}
			}
		
### 10字节输入流FileInputStream读取字节数组的实现原理		
	* A：字节输入流FileInputStream读取字节数组的实现原理
		* a: 原理
			* 参见day23_source文件夹中的"读取数组的原理.jpg"
		
					
		* b: 案例代码
		
			public class FileInputStreamDemo1 {
				public static void main(String[] args) throws IOException {
					FileInputStream fis = new FileInputStream("c:\\a.txt");
					//创建字节数组
					byte[] b = new byte[1024];
					
					int len = 0 ;
					while( (len = fis.read(b)) !=-1){
						System.out.print(new String(b,0,len));
					}
					fis.close();
				}
			}

				
### 11文件复制原理
	* A: 文件复制原理
		* a: 见day23_source/文件复制原理.jpg



### 12字节流复制文件读取单个字节
	* A: 字节流复制文件读取单个字节
		* a: 案例代码
			/*
			 *  将数据源 c:\\a.txt
			 *  复制到 d:\\a.txt  数据目的
			 *  字节输入流,绑定数据源
			 *  字节输出流,绑定数据目的
			 *  
			 *  输入,读取1个字节
			 *  输出,写1个字节
			 */
			public class Copy {
				public static void main(String[] args) {
					//定义两个流的对象变量
					FileInputStream fis = null;
					FileOutputStream fos = null;
					try{
						//建立两个流的对象,绑定数据源和数据目的
						fis = new FileInputStream("c:\\t.zip");
						fos = new FileOutputStream("d:\\t.zip");
						//字节输入流,读取1个字节,输出流写1个字节
						int len = 0 ;
						while((len = fis.read())!=-1){
							fos.write(len);
						}
					}catch(IOException ex){
						System.out.println(ex);
						throw new RuntimeException("文件复制失败");
					}finally{
						try{
							if(fos!=null)
								fos.close();
						}catch(IOException ex){
							throw new RuntimeException("释放资源失败");
						}finally{
							try{
								if(fis!=null)
									fis.close();
							}catch(IOException ex){
								throw new RuntimeException("释放资源失败");
							}
						}
					}
				}
			}


### 13字节流复制文件读取字节数组
	* A: 字节流复制文件读取字节数组
		* a: 案例代码
			/*
			 *  字节流复制文件
			 *   采用数组缓冲提高效率
			 *   字节数组
			 *   FileInputStream 读取字节数组
			 *   FileOutputStream 写字节数组
			 */
			public class Copy_1 {
				public static void main(String[] args) {
					long s = System.currentTimeMillis();
					FileInputStream fis = null;
					FileOutputStream fos = null;
					try{
						fis = new FileInputStream("c:\\t.zip");
						fos = new FileOutputStream("d:\\t.zip");
						//定义字节数组,缓冲
						byte[] bytes = new byte[1024*10];
						//读取数组,写入数组
						int len = 0 ; 
						while((len = fis.read(bytes))!=-1){
							fos.write(bytes, 0, len);
						}
					}catch(IOException ex){
						System.out.println(ex);
						throw new RuntimeException("文件复制失败");
					}finally{
						try{
							if(fos!=null)
								fos.close();
						}catch(IOException ex){
							throw new RuntimeException("释放资源失败");
						}finally{
							try{
								if(fis!=null)
									fis.close();
							}catch(IOException ex){
								throw new RuntimeException("释放资源失败");
							}
						}
					}
					long e = System.currentTimeMillis();
					System.out.println(e-s);
				}
			}
				
### 14编码表
	* A: 编码表
		* a: 定义：
			* 生活中字符和计算机二进制的对应关系表,就是编码表
		* b: 分类
			* 1、ascii： 一个字节中的7位就可以表示。对应的字节都是正数。0-xxxxxxx
			* 2、iso-8859-1:拉丁码表 latin，用了一个字节用的8位。1-xxxxxxx  负数。
			* 3、GB2312:简体中文码表。包含6000-7000中文和符号。用两个字节表示。两个字节第一个字节是负数,第二个字节可能是正数
				* GBK:目前最常用的中文码表，2万的中文和符号。用两个字节表示，其中的一部分文字，第一个字节开头是1，第二字节开头是0
				* GB18030：最新的中文码表，目前还没有正式使用。
			* 4、unicode：国际标准码表:无论是什么文字，都用两个字节存储。
				* Java中的char类型用的就是这个码表。char c = 'a';占两个字节。
				* Java中的字符串是按照系统默认码表来解析的。简体中文版 字符串默认的码表是GBK。
			* 5、UTF-8:基于unicode，一个字节就可以存储数据，不要用两个字节存储，而且这个码表更加的标准化，在每一个字节头加入了编码信息(后期到api中查找)。
			* 6、能识别中文的码表：GBK、UTF-8；正因为识别中文码表不唯一，涉及到了编码解码问题。
				* 对于我们开发而言；常见的编码 GBK  UTF-8  ISO-8859-1
				* 文字--->(数字) ：编码。 “abc”.getBytes()  byte[]
				* (数字)--->文字  : 解码。 byte[] b={97,98,99}  new String(b) 
	
### 15字符输出流写文本FileWriter类
	* A: 字符输出流写文本FileWriter类
		* a: 方法介绍
			*  void write(int c)
				*  写入单个字符
			* void write(String str)  
				* 写入字符串
			* void write(String str, int off, int len) 
				* 写入字符串的某一部分
			* void write(char[] cbuf)  
				* 写入字符数组
			* abstract  void write(char[] cbuf, int off, int len)  
				*  写入字符数组的某一部分
		* b: 案例代码
			/*
			 *   字符输出流
			 *     java.io.Writer 所有字符输出流的超类
			 *   写文件,写文本文件
			 *   
			 *   写的方法 write
			 *     write(int c) 写1个字符
			 *     write(char[] c)写字符数组
			 *     write(char[] c,int,int)字符数组一部分,开始索引,写几个
			 *     write(String s) 写入字符串
			 *     
			 *   Writer类的子类对象 FileWriter
			 *   
			 *   构造方法:  写入的数据目的
			 *     File 类型对象
			 *     String 文件名
			 *     
			 *   字符输出流写数据的时候,必须要运行一个功能,刷新功能
			 *   flush()
			 */
			public class WriterDemo {
				public static void main(String[] args) throws IOException{
					FileWriter fw = new FileWriter("c:\\1.txt");
					
					//写1个字符
					fw.write(100);
					fw.flush();
					
					//写1个字符数组
					char[] c = {'a','b','c','d','e'};
					fw.write(c);
					fw.flush();
					
					//写字符数组一部分
					fw.write(c, 2, 2);
					fw.flush();
					
					//写如字符串
					fw.write("hello");
					fw.flush();
					
					fw.close();
				}
			}

		
### 16字符输入流读取文本FileReader类
	* A: 字符输入流读取文本FileReader类
		* a: 方法介绍
			*  int read() 
				* 读取单个字符
			* int read(char[] cbuf) 
				* 将字符读入数组
			* abstract  int read(char[] cbuf, int off, int len)  
				* 将字符读入数组的某一部分。
		* b: 案例代码
			/*
			 *  字符输入流读取文本文件,所有字符输入流的超类
			 *    java.io.Reader
			 *  专门读取文本文件
			 *  
			 *  读取的方法 : read()
			 *   int read() 读取1个字符
			 *   int read(char[] c) 读取字符数组
			 *   
			 *   Reader类是抽象类,找到子类对象 FileReader
			 *   
			 *   构造方法: 绑定数据源
			 *     参数:
			 *        File  类型对象
			 *        String文件名
			 */
			public class ReaderDemo {
				public static void main(String[] args) throws IOException{
					FileReader fr = new FileReader("c:\\1.txt");
					/*int len = 0 ;
					while((len = fr.read())!=-1){
						System.out.print((char)len);
					}*/
					char[] ch = new char[1024];
					int len = 0 ;
					while((len = fr.read(ch))!=-1){
						System.out.print(new String(ch,0,len));
					}
					
					fr.close();
				}
			}

		
### 17flush方法和close方法区别
	* A: flush方法和close方法区别
		*a: flush()方法
			* 用来刷新缓冲区的,刷新后可以再次写出,只有字符流才需要刷新
		*b: close()方法
			* 用来关闭流释放资源的的,如果是带缓冲区的流对象的close()方法,不但会关闭流,还会再关闭流之前刷新缓冲区,关闭后不能再写出 
			
### 18字符流复制文本文件
	* A: 字符流复制文本文件
		* a: 案例代码
			/*
			 *  字符流复制文本文件,必须文本文件
			 *  字符流查询本机默认的编码表,简体中文GBK
			 *  FileReader读取数据源
			 *  FileWriter写入到数据目的
			 */
			public class Copy_2 {
				public static void main(String[] args) {
					FileReader fr = null;
					FileWriter fw = null;
					try{
						fr = new FileReader("c:\\1.txt");
						fw = new FileWriter("d:\\1.txt");
						char[] cbuf = new char[1024];
						int len = 0 ;
						while(( len = fr.read(cbuf))!=-1){
							fw.write(cbuf, 0, len);
							fw.flush();
						}
						
					}catch(IOException ex){
						System.out.println(ex);
						throw new RuntimeException("复制失败");
					}finally{
						try{
							if(fw!=null)
								fw.close();
						}catch(IOException ex){
							throw new RuntimeException("释放资源失败");
						}finally{
							try{
								if(fr!=null)
									fr.close();
							}catch(IOException ex){
								throw new RuntimeException("释放资源失败");
							}
						}
					}
				}
			}

### 19总结
	* 把今天的知识点总结一遍。
今日内容介绍
1、转换流
2、缓冲流

=======================第一节课开始=============================================


### 01转换流概述
	* A: 转换流概述
		* a: 转换流概述
			* OutputStreamWriter 是字符流通向字节流的桥梁：可使用指定的字符编码表，将要写入流中的字符编码成字节
			* 将字符串按照指定的编码表转成字节，在使用字节流将这些字节写出去
		
	
### 02转换流_字符转字节的过程
	* A: 转换流_字符转字节的过程
		* a.图解
			* 详见day24_source/转换流.JPG图片

			
### 03OutputStreamWriter写文本文件
	* A: OutputStreamWriter写文本文件
		* a: OutputStreamWriter
			* java.io.OutputStreamWriter 继承Writer类
			* 就是一个字符输出流，写文本文件
			* write()字符，字符数组，字符串    
			* 字符通向字节的桥梁，将字符流转字节流
			* OutputStreamWriter 使用方式
				* 构造方法：
					* OutputStreamWriter(OuputStream out)接收所有的字节输出流
					* 字节输出流：  FileOutputStream       
					* OutputStreamWriter(OutputStream out, String charsetName)
					* String charsetName 传递编码表名字 GBK  UTF-8 
			* OutputStreamWriter 有个子类，  FileWriter
		* b: 案例代码
		
				public class OutputStreamWriterDemo {
					public static void main(String[] args)throws IOException {
				//		writeGBK();
						writeUTF();
					}
					/*
					 * 转换流对象OutputStreamWriter写文本
					 * 采用UTF-8编码表写入
					 */
					public static void writeUTF()throws IOException{
						//创建字节输出流，绑定文件
						FileOutputStream fos = new FileOutputStream("c:\\utf.txt");
						//创建转换流对象，构造方法保证字节输出流，并指定编码表是UTF-8
						OutputStreamWriter osw = new OutputStreamWriter(fos,"UTF-8");
						osw.write("你好");
						osw.close();
					}
					
					/*
					 * 转换流对象 OutputStreamWriter写文本
					 * 文本采用GBK的形式写入
					 */
					public static void writeGBK()throws IOException{
						//创建字节输出流，绑定数据文件
						FileOutputStream fos = new FileOutputStream("c:\\gbk.txt");
						//创建转换流对象，构造方法，绑定字节输出流，使用GBK编码表
						OutputStreamWriter osw = new OutputStreamWriter(fos);
						//转换流写数据
						osw.write("你好");
						
						osw.close();
					}
				}

### 04转换流_字节转字符流过程
	* A: 转换流_字节转字符流过程
		* a: InputStreamReader			
			* java.io.InputStreamReader 继承 Reader
			* 字符输入流，读取文本文件
			* 字节流向字符的敲了，将字节流转字符流
			* 读取的方法:
				* read() 读取1个字符，读取字符数组
			* 技巧
				* OuputStreamWriter写了文件
				* InputStreamReader读取文件
			* OutputStreamWriter(OutputStream out)所有字节输出流
			* InputStreamReader(InputStream in) 接收所有的字节输入流
			* 可以传递的字节输入流： FileInputStream
			* InputStreamReader(InputStream in,String charsetName) 传递编码表的名字
		* b: 图解
			* 详见day24_source/转换流.JPG图片


### 05InputSteamReader读取文本文件
	* A: InputSteamReader读取文本文件
		* a: 案例代码
			public class InputStreamReaderDemo {
				public static void main(String[] args) throws IOException {
			//		readGBK();
					readUTF();
				}
				/*
				 *  转换流,InputSteamReader读取文本
				 *  采用UTF-8编码表,读取文件utf
				 */
				public static void readUTF()throws IOException{
					//创建自己输入流,传递文本文件
					FileInputStream fis = new FileInputStream("c:\\utf.txt");
					//创建转换流对象,构造方法中,包装字节输入流,同时写编码表名
					InputStreamReader isr = new InputStreamReader(fis,"UTF-8");
					char[] ch = new char[1024];
					int len = isr.read(ch);
					System.out.println(new String(ch,0,len));
					isr.close();
				}
				/*
				 *  转换流,InputSteamReader读取文本
				 *  采用系统默认编码表,读取GBK文件
				 */
				public static void readGBK()throws IOException{
					//创建自己输入流,传递文本文件
					FileInputStream fis = new FileInputStream("c:\\gbk.txt");
					//创建转换流对象,构造方法,包装字节输入流
					InputStreamReader isr = new InputStreamReader(fis);
					char[] ch = new char[1024];
					int len = isr.read(ch);
					System.out.println(new String(ch,0,len));
					
					isr.close();
				}
			}


			
### 06转换流子类父类的区别
	* A: 转换流子类父类的区别
		* a: 继承关系
			OutputStreamWriter:
				|--FileWriter:
			InputStreamReader:
				|--FileReader;
		* b: 区别
			* OutputStreamWriter和InputStreamReader是字符和字节的桥梁：也可以称之为字符转换流。字符转换流原理：字节流+编码表。
			* FileWriter和FileReader：作为子类，仅作为操作字符文件的便捷类存在。
				当操作的字符文件，使用的是默认编码表时可以不用父类，而直接用子类就完成操作了，简化了代码。
			* 以下三句话功能相同
				* InputStreamReader isr = new InputStreamReader(new FileInputStream("a.txt"));//默认字符集。
				* InputStreamReader isr = new InputStreamReader(new FileInputStream("a.txt"),"GBK");//指定GBK字符集。
				* FileReader fr = new FileReader("a.txt");
			
### 07缓冲流概述
	* A: 缓冲流概述
		* a: 概述
			* 可提高IO流的读写速度
			* 分为字节缓冲流与字符缓冲流 
				

						
### 08字节输出流缓冲流BufferedOutputStream
	* A: 字节输出流缓冲流BufferedOutputStream
		* a: BufferedOutputStream
			* 字节输出流的缓冲流
			* java.io.BufferedOuputStream 作用: 提高原有输出流的写入效率
			* BufferedOuputStream 继承 OutputStream
			* 方法,写入 write 字节,字节数组			 
			* 构造方法:
				* BufferedOuputStream(OuputStream out)
				* 可以传递任意的字节输出流, 传递的是哪个字节流,就对哪个字节流提高效率  
 
		* b: 案例代码
			public class BufferedOutputStreamDemo {
				public static void main(String[] args)throws IOException {
					//创建字节输出流,绑定文件
					//FileOutputStream fos = new FileOutputStream("c:\\buffer.txt");
					//创建字节输出流缓冲流的对象,构造方法中,传递字节输出流
					BufferedOutputStream bos = new
							BufferedOutputStream(new FileOutputStream("c:\\buffer.txt"));
					
					bos.write(55);
					
					byte[] bytes = "HelloWorld".getBytes();
					
					bos.write(bytes);
					
					bos.write(bytes, 3, 2);
					
					bos.close();
				}
			}



### 09字节输入流缓冲流BufferedInputStream
	* A: 字节输入流缓冲流BufferedInputStream
		* a: BufferedInputStream
			* 字节输入流的缓冲流
			* 继承InputStream,标准的字节输入流
			* 读取方法  read() 单个字节,字节数组			  
			* 构造方法:
				* BufferedInputStream(InputStream in)
				* 可以传递任意的字节输入流,传递是谁,就提高谁的效率
				* 可以传递的字节输入流 FileInputStream
		* b: 案例代码
			public class BufferedInputStreamDemo {
				public static void main(String[] args) throws IOException{
					//创建字节输入流的缓冲流对象,构造方法中包装字节输入流,包装文件
					BufferedInputStream bis = new 
							BufferedInputStream(new FileInputStream("c:\\buffer.txt"));
					byte[] bytes = new byte[10];
					int len = 0 ;
					while((len = bis.read(bytes))!=-1){
						System.out.print(new String(bytes,0,len));
					}
					bis.close();
				}
			}

		
### 10四种文件复制方式的效率比较		
	* A：四种文件复制方式的效率比较
		* a: 四中复制方式
			* 字节流读写单个字节                    125250 毫秒
			* 字节流读写字节数组                    193    毫秒  OK
			* 字节流缓冲区流读写单个字节    		1210   毫秒
			* 字节流缓冲区流读写字节数组            73     毫秒  OK		
					
		* b: 案例代码
		
			public class Copy {
				public static void main(String[] args)throws IOException {
					long s = System.currentTimeMillis();
					copy_4(new File("c:\\q.exe"), new File("d:\\q.exe"));
					long e = System.currentTimeMillis();
					System.out.println(e-s);
				}
				/*
				 * 方法,实现文件复制
				 *  4. 字节流缓冲区流读写字节数组
				 */
				public static void copy_4(File src,File desc)throws IOException{
					BufferedInputStream bis = new BufferedInputStream(new FileInputStream(src));
					BufferedOutputStream bos = new BufferedOutputStream(new FileOutputStream(desc));
					int len = 0 ;
					byte[] bytes = new byte[1024];
					while((len = bis.read(bytes))!=-1){
						bos.write(bytes,0,len);
					}
					bos.close();
					bis.close();
				}
				/*
				 * 方法,实现文件复制
				 *  3. 字节流缓冲区流读写单个字节
				 */
				public static void copy_3(File src,File desc)throws IOException{
					BufferedInputStream bis = new BufferedInputStream(new FileInputStream(src));
					BufferedOutputStream bos = new BufferedOutputStream(new FileOutputStream(desc));
					int len = 0 ;
					while((len = bis.read())!=-1){
						bos.write(len);
					}
					bos.close();
					bis.close();
				}
				
				/*
				 * 方法,实现文件复制
				 *  2. 字节流读写字节数组
				 */
				public static void copy_2(File src,File desc)throws IOException{
					FileInputStream fis = new FileInputStream(src);
					FileOutputStream fos = new FileOutputStream(desc);
					int len = 0 ;
					byte[] bytes = new byte[1024];
					while((len = fis.read(bytes))!=-1){
						fos.write(bytes,0,len);
					}
					fos.close();
					fis.close();
				}
				
				/*
				 * 方法,实现文件复制
				 *  1. 字节流读写单个字节
				 */
				public static void copy_1(File src,File desc)throws IOException{
					FileInputStream fis = new FileInputStream(src);
					FileOutputStream fos = new FileOutputStream(desc);
					int len = 0 ;
					while((len = fis.read())!=-1){
						fos.write(len);
					}
					fos.close();
					fis.close();
				}
			}

				
### 11字符输出流缓冲流BufferedWriter
	* A: 字符输出流缓冲流BufferedWriter
		* a: BufferedWriter
			* 字符输出流缓冲区流
			* java.io.BufferedWriter 继承 Writer
			* 写入方法 write () 单个字符,字符数组,字符串
  
			* 构造方法:
				* BufferedWriter(Writer w)传递任意字符输出流
				* 传递谁,就高效谁
				* 能传递的字符输出流 FileWriter, OutputStreamWriter
		* b: 案例代码
			public class BufferedWrierDemo {
				public static void main(String[] args) throws IOException{
					//创建字符输出流,封装文件
					FileWriter fw = new FileWriter("c:\\buffer.txt");
					BufferedWriter bfw = new BufferedWriter(fw);
					
					bfw.write(100);
					bfw.flush();
					bfw.write("你好".toCharArray());
					bfw.flush();
					
					
					bfw.write("你好");
					
					bfw.flush();
					
					
					bfw.write("我好好");
					
					bfw.flush();

					bfw.write("大家都好");
					bfw.flush();
					
					bfw.close();
					
				}
			}



### 12字符输出流缓冲流BufferedWriter特有方法newLine
	* A: 字符输出流缓冲流BufferedWriter特有方法newLine
		* a: 方法介绍
			* void  newLine() 写换行
				
			* newLine()文本中换行, \r\n也是文本换行
			* 方法具有平台无关性
			* Windows  \r\n
			* Linux    \n
				 
			* newLine()运行结果,和操作系统是相互关系
			* JVM: 安装的是Windows版本,newLine()写的就是\r\n
			* 安装的是Linux版本,newLine()写的就是\n
			/*
			 *  将数据源 c:\\a.txt
			 *  复制到 d:\\a.txt  数据目的
			 *  字节输入流,绑定数据源
			 *  字节输出流,绑定数据目的
			 *  
			 *  输入,读取1个字节
			 *  输出,写1个字节
			 */
		* b: 案例代码
			public class BufferedWrierDemo {
				public static void main(String[] args) throws IOException{
					//创建字符输出流,封装文件
					FileWriter fw = new FileWriter("c:\\buffer.txt");
					BufferedWriter bfw = new BufferedWriter(fw);
					
					bfw.write(100);
					bfw.flush();
					bfw.write("你好".toCharArray());
					bfw.flush();
					
					bfw.write("你好");
					bfw.newLine();
					bfw.flush();
					
					
					bfw.write("我好好");
					bfw.newLine();
					bfw.flush();

					bfw.write("大家都好");
					bfw.flush();
					
					bfw.close();
					
				}
			}
	


### 13字符输入流缓冲流BufferedReader
	* A: 字符输入流缓冲流BufferedReader
		* a: 概述
			* 从字符输入流中读取文本，缓冲各个字符，从而实现字符、数组和行的高效读取
			* public String readLine() 读取一个文本行，包含该行内容的字符串，不包含任何行终止符，如果已到达流末尾，则返回 null
				
### 14字符输入流缓冲流BufferedReader读取文本行
	* A: 字符输入流缓冲流BufferedReader读取文本行
		* a: BufferedReader
			* 字符输入流缓冲流
			* java.io.BufferedReader 继承 Reader
			* 读取功能 read() 单个字符,字符数组
			* 构造方法:
				* BufferedReader(Reader r)
				* 可以任意的字符输入流
				   FileReader  InputStreamReader       
			* BufferedReader自己的功能
				* String readLine() 读取文本行 \r\n   
					* 方法读取到流末尾,返回null
		* b: 小特点
			 * 获取内容的方法一般都有返回值
			 * int 没有返回的都是负数
			 * 引用类型 找不到返回null
			 * boolean 找不到返回false
			
		* c: 案例代码
			public class BufferedReaderDemo {
				public static void main(String[] args) throws IOException {
					int lineNumber = 0;
					//创建字符输入流缓冲流对象,构造方法传递字符输入流,包装数据源文件
					BufferedReader bfr = new BufferedReader(new FileReader("c:\\a.txt"));
					//调用缓冲流的方法 readLine()读取文本行
					//循环读取文本行, 结束条件 readLine()返回null
					String line = null;
					while((line = bfr.readLine())!=null){
						lineNumber++;
						System.out.println(lineNumber+"  "+line);
					}
					bfr.close();
				}
			}

			/*
			 * String line = bfr.readLine();
					System.out.println(line);
					
					line = bfr.readLine();
					System.out.println(line);
					
					line = bfr.readLine();
					System.out.println(line);
					
					line = bfr.readLine();
					System.out.println(line);
					
					line = bfr.readLine();
					System.out.println(line);
			 */
			 
### 15字符流缓冲区流复制文本文件
	* A: 字符流缓冲区流复制文本文件
		* a: 案例代码
			/*
			 *  使用缓冲区流对象,复制文本文件
			 *  数据源  BufferedReader+FileReader 读取
			 *  数据目的 BufferedWriter+FileWriter 写入
			 *  读取文本行, 读一行,写一行,写换行
			 */
			public class Copy_1 {
				public static void main(String[] args) throws IOException{
					BufferedReader bfr = new BufferedReader(new FileReader("c:\\w.log"));	
					BufferedWriter bfw = new BufferedWriter(new FileWriter("d:\\w.log"));
					//读取文本行, 读一行,写一行,写换行
					String line = null;
					while((line = bfr.readLine())!=null){
						bfw.write(line);
						bfw.newLine();
						bfw.flush();
					}
					bfw.close();
					bfr.close();
				}
			}

			
### 16IO流对象的操作规律
	* A: IO流对象的操作规律
		* a: 明确一：要操作的数据是数据源还是数据目的。
			* 源：InputStream    Reader
			* 目的：OutputStream Writer
			* 先根据需求明确要读，还是要写。

		* b: 明确二：要操作的数据是字节还是文本呢？
			* 源：
				* 字节：InputStream
				* 文本：Reader
			* 目的：
				* 字节：OutputStream
				* 文本：Writer
		* c: 明确三：明确数据所在的具体设备。
			* 源设备：
				* 硬盘：文件  File开头。
				* 内存：数组，字符串。
				* 键盘：System.in;
				* 网络：Socket
			* 目的设备：
				* 硬盘：文件  File开头。
				* 内存：数组，字符串。
				* 屏幕：System.out
				* 网络：Socket
				* 完全可以明确具体要使用哪个流对象。
		* d: 明确四：是否需要额外功能呢？
			* 额外功能：
				* 转换吗？转换流。InputStreamReader OutputStreamWriter
				* 高效吗？缓冲区对象。BufferedXXX
				* 已经明确到了具体的体系上。
### 17总结
	* 把今天的知识点总结一遍。
今日内容介绍
1、Properties集合
2、序列化流与反序列化流
3、打印流
4、commons-IO


### 01Properties集合的特点
	* A: Properties集合的特点
		* a: Properties类介绍
			* Properties 类表示了一个持久的属性集。Properties 可保存在流中或从流中加载。属性列表中每个键及其对应值都是一个字符串
		* b: 特点
			* Hashtable的子类，map集合中的方法都可以用。
			* 该集合没有泛型。键值都是字符串。
			* 它是一个可以持久化的属性集。键值可以存储到集合中，也可以存储到持久化的设备(硬盘、U盘、光盘)上。键值的来源也可以是持久化的设备。
			* 有和流技术相结合的方法。
		* c: 方法介绍
			* load(InputStream inputStream)  把指定流所对应的文件中的数据，读取出来，保存到Propertie集合中
			* load(Reader reader) 按简单的面向行的格式从输入字符流中读取属性列表（键和元素对）
			* store(OutputStream outputStream,String commonts) 把集合中的数据，保存到指定的流所对应的文件中，参数commonts代表对描述信息
			* stroe(Writer writer,String comments) 以适合使用 load(Reader) 方法的格式，将此 Properties 表中的属性列表（键和元素对）写入输出字符
			

		
	
### 02Properties集合存储键值对
	* A: Properties集合存储键值对		
		* a: 方法介绍
			*  集合对象Properties类,继承Hashtable,实现Map接口
			*  可以和IO对象结合使用,实现数据的持久存储
			* 使用Properties集合,存储键值对
			* setProperty等同与Map接口中的put
			* setProperty(String key, String value)
			* 通过键获取值, getProperty(String key)
		* b: 案例代码
			public class PropertiesDemo {
				public static void main(String[] args)throws IOException {
					function_2();
				}
				/*
				 * 使用Properties集合,存储键值对
				 * setProperty等同与Map接口中的put
				 * setProperty(String key, String value)
				 * 通过键获取值, getProperty(String key)
				 */
				public static void function(){
					Properties pro = new Properties();
					pro.setProperty("a", "1");
					pro.setProperty("b", "2");
					pro.setProperty("c", "3");
					System.out.println(pro);
					
					String value = pro.getProperty("c");
					System.out.println(value);
					
					//方法stringPropertyNames,将集合中的键存储到Set集合,类似于Map接口的方法keySet
					Set<String> set = pro.stringPropertyNames();
					for(String key : set){
						System.out.println(key+"..."+pro.getProperty(key));
					}
				}
			}

			
### 03Properties集合的方法load
	* A: Properties集合的方法load
		* a: 方法介绍
			* Properties集合特有方法 load
			* load(InputStream in)
			* load(Reader r)
			* 传递任意的字节或者字符输入流
			* 流对象读取文件中的键值对,保存到集合
			
		* b: 案例代码		
				public class PropertiesDemo {
					public static void main(String[] args)throws IOException {
						function_1();
					}									
					/*
					 * Properties集合特有方法 load
					 * load(InputStream in)
					 * load(Reader r)
					 * 传递任意的字节或者字符输入流
					 * 流对象读取文件中的键值对,保存到集合
					 */
					public static void function_1()throws IOException{
						Properties pro = new Properties();
						FileReader fr = new FileReader("c:\\pro.properties");
						//调用集合的方法load,传递字符输入流
						pro.load(fr);
						fr.close();
						System.out.println(pro);
					}					
				}

### 04Properties集合的方法store
	* A: Properties集合的方法store
		* a: 方法介绍			
			* Properties集合的特有方法store
			* store(OutputStream out)
			* store(Writer w)
			* 接收所有的字节或者字符的输出流,将集合中的键值对,写回文件中保存
		* b: 案例代码
			public class PropertiesDemo {
				public static void main(String[] args)throws IOException {
					function_2();
				}
				/*
				 * Properties集合的特有方法store
				 * store(OutputStream out)
				 * store(Writer w)
				 * 接收所有的字节或者字符的输出流,将集合中的键值对,写回文件中保存
				 */
				public static void function_2()throws IOException{
					Properties pro = new Properties();
					pro.setProperty("name", "zhangsan");
					pro.setProperty("age", "31");
					pro.setProperty("email", "123456789@163.com");
					FileWriter fw = new FileWriter("c:\\pro.properties");
					//键值对,存回文件,使用集合的方法store传递字符输出流
					pro.store(fw, "");
					fw.close();
				}				
			}


### 05对象的序列化与反序列化
	* A: 对象的序列化与反序列化
		* a: 基本概念
			* 对象的序列化
				* 对象中的数据，以流的形式，写入到文件中保存过程称为写出对象，对象的序列化
				* ObjectOutputStream将对象写道文件中，实现序列化
			* 对象的反序列化
				* 在文件中，以流的形式，将对象读出来，读取对象，对象的反序列化
				* ObjectInputStream 将文件对象读取出来
					
### 06ObjectOutputStream流写对象
	* A: ObjectOutputStream流写对象
		* a: 简单介绍
			 *  IO流对象,实现对象Person序列化,和反序列化
			 *  ObjectOutputStream 写对象,实现序列化
			 *  ObjectInputStream 读取对象,实现反序列化

		* b: 案例代码
			public class Person implements Serializable{
				public String name;
				public int age;
				public Person(String name, int age) {
					super();
					this.name = name;
					this.age = age;
				}
				public Person(){}
				
				public String getName() {
					return name;
				}
				public void setName(String name) {
					this.name = name;
				}
				public int getAge() {
					return age;
				}
				public void setAge(int age) {
					this.age = age;
				}
				@Override
				public String toString() {
					return "Person [name=" + name + ", age=" + age + "]";
				}				
			}
			
			public class ObjectStreamDemo {
				public static void main(String[] args)throws IOException, ClassNotFoundException {
			//		writeObject();
					readObject();
				}
				/*
				 * ObjectOutputStream
				 * 构造方法: ObjectOutputStream(OutputSteam out)
				 * 传递任意的字节输出流
				 * void writeObject(Object obj)写出对象的方法
				 */
				public static void writeObject() throws IOException{
					//创建字节输出流,封装文件
					FileOutputStream fos = new FileOutputStream("c:\\person.txt");
					//创建写出对象的序列化流的对象,构造方法传递字节输出流
					ObjectOutputStream oos = new ObjectOutputStream(fos);
					Person p = new Person("lisi",25);
					//调用序列化流的方法writeObject,写出对象
					oos.writeObject(p);
					oos.close();
				}
			}
			
### 07ObjectInputStream流读取对象
	* A: ObjectInputStream流读取对象
		* a: 简单介绍
			* ObjectInputStream
			* 构造方法:ObjectInputStream(InputStream in)
			* 传递任意的字节输入流,输入流封装文件,必须是序列化的文件
			* Object readObject()  读取对象
		* b: 案例代码
			/*
			 *  IO流对象,实现对象Person序列化,和反序列化
			 *  ObjectOutputStream 写对象,实现序列化
			 *  ObjectInputStream 读取对象,实现反序列化
			 */
			public class ObjectStreamDemo {
				public static void main(String[] args)throws IOException, ClassNotFoundException {
					readObject();
				}
				/*
				 * ObjectInputStream
				 * 构造方法:ObjectInputStream(InputStream in)
				 * 传递任意的字节输入流,输入流封装文件,必须是序列化的文件
				 * Object readObject()  读取对象
				 */
				public static void readObject() throws IOException, ClassNotFoundException{
					FileInputStream fis = new FileInputStream("c:\\person.txt");
					//创建反序列化流,构造方法中,传递字节输入流
					ObjectInputStream ois = new ObjectInputStream(fis);
					//调用反序列化流的方法 readObject()读取对象
					Object obj =ois.readObject();
					System.out.println(obj);
					ois.close();
				}				
			}
						
### 08静态不能序列化
	* A: 静态不能序列化
		* a: 原因
			* 序列化是把对象数据进行持久化存储
			* 静态的东西不属于对象，而属于类
 
### 09transient关键字
	* A: transient关键字
		* a: 作用
			* 被transient修饰的属性不会被序列化
			* transient关键字只能修饰成员变量
			
		
### 10Serializable接口的含义
	* A：Serializable接口的含义
		* a: 作用
			* 给需要序列化的类上加标记。该标记中没有任何抽象方法
			* 只有实现了 Serializable接口的类的对象才能被序列化
				
### 11序列化中的序列号冲突问题
	* A: 序列化中的序列号冲突问题
		* a: 问题产生原因
			* 当一个类实现Serializable接口后，创建对象并将对象写入文件，之后更改了源代码(比如：将成员变量的修饰符有private改成public)，
				再次从文件中读取对象时会报异常
			* 见day25_source文件夹下的"序列号的冲突.JPG"文件

### 12序列化中自定义的序列号
	* A: 序列化中自定义的序列号
		* a: 定义方式
			* private static final long serialVersionUID = 1478652478456L;
				* 这样每次编译类时生成的serialVersionUID值都是固定的 	
		
		* b: 案例代码
			public class Person implements Serializable{
				public String name;
				public /*transient阻止成员变量序列化*/ int age;
				//类,自定义了序列号,编译器不会计算序列号
				private static final long serialVersionUID = 1478652478456L;

				public Person(String name, int age) {
					super();
					this.name = name;
					this.age = age;
				}
				public Person(){}
				
				public String getName() {
					return name;
				}
				public void setName(String name) {
					this.name = name;
				}
				public int getAge() {
					return age;
				}
				public void setAge(int age) {
					this.age = age;
				}
				@Override
				public String toString() {
					return "Person [name=" + name + ", age=" + age + "]";
				}				
			}

### 13打印流和特性
	* A: 打印流和特性
		* a: 概述
			* 打印流添加输出数据的功能，使它们能够方便地打印各种数据值表示形式.
			* 打印流根据流的分类：
				* 字节打印流	PrintStream
				* 字符打印流	PrintWriter
			* 方法：
				* void print(String str): 输出任意类型的数据，
				* void println(String str): 输出任意类型的数据，自动写入换行操作
		* b: 特点			
			* 此流不负责数据源,只负责数据目的
			* 为其他输出流,添加功能
			* 永远不会抛出IOException，但是可能抛出别的异常  
			* 两个打印流的方法,完全一致
			* 构造方法,就是打印流的输出目的端
			* PrintStream构造方法
				* 接收File类型,接收字符串文件名,接收字节输出流OutputStream
			* PrintWriter构造方法
				* 接收File类型,接收字符串文件名,接收字节输出流OutputStream, 接收字符输出流Writer

				
### 14打印流输出目的是File对象
	* A: 打印流输出目的是File对象
		* a: 案例代码
			public class PrintWriterDemo {
				public static void main(String[] args) throws  IOException {
					function_3();

				}
				
				/*
				 * 打印流,向File对象的数据目的写入数据
				 * 方法print println  原样输出
				 * write方法走码表
				 */
				public static void function() throws FileNotFoundException{
					File file = new File("c:\\1.txt");
					PrintWriter pw = new PrintWriter(file);
					pw.println(true);
					pw.write(100);
					pw.close();
				}
			}
			
### 15输出语句是char数组
	* A: 输出语句是char数组
		* a: 案例代码
			public class Demo {
				public static void main(String[] args) {
					int[] arr = {1};
					System.out.println(arr);
					
					char[] ch = {'a','b'};
					System.out.println(ch);
					
					byte[] b = {};
					System.out.println(b);
				}
			}
		* b: 结果分析
			* println数组，只有打印字符数组时只有容，其余均打印数组的地址
				* 因为api中定义了打印字符数组的方法，其底层是在遍历数组中的元素
				* 而其他打印数组的方法，都是将数组对象编程Object，其底层再将对象编程String，调用了String s = String.valueOf(x);方法
		
### 16打印流输出目的是String和流对象
	* A: 打印流输出目的是String和流对象
		* a: 案例代码
			public class PrintWriterDemo {
				public static void main(String[] args) throws  IOException {
					function_2();

				}
					
				/*
				 * 打印流,输出目的,是流对象
				 * 可以是字节输出流,可以是字符的输出流
				 * OutputStream  Writer
				 */
				public static void function_2() throws IOException{
				//	FileOutputStream fos = new FileOutputStream("c:\\3.txt");
					FileWriter fw = new FileWriter("c:\\4.txt");
					PrintWriter pw = new PrintWriter(fw);
					pw.println("打印流");
					pw.close();
				}
				/*
				 * 打印流,输出目的,String文件名
				 */
				public static void function_1() throws FileNotFoundException{
					PrintWriter pw = new PrintWriter("c:\\2.txt");
					pw.println(3.5);
					pw.close();
				}	
				
			}
			
### 17打印流开启自动刷新
	* A: 打印流开启自动刷新
		* 案例代码
			public class PrintWriterDemo {
				public static void main(String[] args) throws  IOException {
					function_3();

				}
				/* 
				 * 打印流,可以开启自动刷新功能
				 * 满足2个条件:
				 *   1. 输出的数据目的必须是流对象
				 *       OutputStream  Writer
				 *   2. 必须调用println,printf,format三个方法中的一个,启用自动刷新
				 */
				public static void function_3()throws  IOException{
					//File f = new File("XXX.txt");
					FileOutputStream fos = new FileOutputStream("c:\\5.txt");
					PrintWriter pw = new PrintWriter(fos,true);
					pw.println("i");
					pw.println("love");
					pw.println("java");
					pw.close();
				}
			}
			
### 18打印流复制文本文件
	* A: 打印流复制文本文件
		* a: 案例代码
			/*
			 * 打印流实现文本复制
			 *   读取数据源  BufferedReader+File 读取文本行
			 *   写入数据目的 PrintWriter+println 自动刷新
			 */
			public class PrintWriterDemo1 {
				public static void main(String[] args) throws IOException{
					BufferedReader bfr = new BufferedReader(new FileReader("c:\\a.txt"));
					PrintWriter pw = new PrintWriter(new FileWriter("d:\\a.txt"),true);
					String line = null;
					while((line = bfr.readLine())!=null){
						pw.println(line);
					}
					pw.close();
					bfr.close();
				}
			}
			
### 19commons-io工具类介绍
	* A: commons-io工具类介绍
		* a: 工具类介绍
			* 解压缩commons-io-2.4.zip文件
			* commons-io-2.4.jar需要导入到项目中的jar包，里面存放的是class文件
			* commons-io-2.4-sources.jar工具类中原代码
			* docs是帮助文档
			
### 20使用工具类commons_io
	* A: 使用工具类commons_io
		* a: 导入jar包
			* 加入classpath的第三方jar包内的class文件才能在项目中使用
			* 创建lib文件夹
			* 将commons-io.jar拷贝到lib文件夹
			* 右键点击commons-io.jar，Build Path→Add to Build Path
		* b: 学会如何看源代码

### 21IO工具类FilenameUtils
	* A: IO工具类FilenameUtils
		* a: 方法介绍
			* getExtension(String path)：获取文件的扩展名；
			* getName()：获取文件名；
			* isExtension(String fileName,String ext)：判断fileName是否是ext后缀名；
		* b: 案例代码
			public class Commons_IODemo {
				public static void main(String[] args) {
					function_2();
				}
				/*
				 * FilenameUtils类的方法
				 * static boolean isExtension(String filename,String extension)
				 * 判断文件名的后缀是不是extension
				 */
				public static void function_2(){
					boolean b = FilenameUtils.isExtension("Demo.java", "java");
					System.out.println(b);
				}
				
				/*
				 * FilenameUtils类的方法
				 * static String getName(String filename)
				 * 获取文件名
				 */
				public static void function_1(){
					String name = FilenameUtils.getName("c:\\windows\\");
					System.out.println(name);
				}
				
				/*
				 * FilenameUtils类的方法
				 * static String getExtension(String filename)
				 * 获取文件名的扩展名
				 */
				 public static void function(){
					 String name = FilenameUtils.getExtension("c:\\windows");
					 System.out.println(name);
				 }
			}

### 22IO工具类FileUtils
	* A: IO工具类FileUtils
		* a: 方法介绍
			* readFileToString(File file)：读取文件内容，并返回一个String；
			* writeStringToFile(File file，String content)：将内容content写入到file中；
			* copyDirectoryToDirectory(File srcDir,File destDir);文件夹复制
			* copyFile(File srcFile,File destFile);文件复制
			
		* b: 案例代码
			public class Commons_IODemo1 {
				public static void main(String[] args)throws IOException {
					function_3();
				}
				/*
				 * FileUtils工具类方法
				 * static void copyDirectoryToDirectory(File src,File desc)
				 * 复制文件夹
				 */
				public static void function_3() throws IOException{
					FileUtils.copyDirectoryToDirectory(new File("d:\\demo"), new File("c:\\"));
				}
				
				/*
				 * FileUtils工具类的方法
				 * static void copyFile(File src,File desc)
				 * 复制文件
				 */
				public static void function_2() throws IOException{
					FileUtils.copyFile(new File("c:\\k.jpg"),new File("d:\\k.jpg"));
				}
				
				/*
				 * FileUtils工具类的方法
				 * static void writeStringToFile(File src,String date)
				 * 将字符串直接写到文件中
				 */
				public static void function_1() throws IOException{
					FileUtils.writeStringToFile(new File("c:\\b.txt"),"我爱Java编程");
				}
				
				/*
				 * FileUtils工具类的方法
				 * static String readFileToString(File src)读取文本,返回字符串
				 */
				 public static void function() throws IOException{
					 String s = FileUtils.readFileToString(new File("c:\\a.txt"));
					 System.out.println(s);
				 }
			}

### 23总结
	* 把今天的知识点总结一遍。
			
今日内容介绍
1、多线程
2、线程池

 

 


=======================第一节课开始=============================================

### 01进程概念
*A:进程概念 
   *a:进程：进程指正在运行的程序。确切的来说，当一个程序进入内存运行，
        即变成一个进程，进程是处于运行过程中的程序，并且具有一定独立功能。

### 02线程的概念 
 *A:线程的概念
   *a:线程：线程是进程中的一个执行单元(执行路径)，负责当前进程中程序的执行，
          一个进程中至少有一个线程。一个进程中是可以有多个线程的，
          这个应用程序也可以称之为多线程程序。
    简而言之：一个程序运行后至少有一个进程，一个进程中可以包含多个线程

### 03深入线程的概念
  A:深入线程的概念
    什么是多线程呢？
     即就是一个程序中有多个线程在同时执行。
     一个核心的CPU在多个线程之间进行着随即切换动作,由于切换时间很短(毫秒甚至是纳秒级别),导致我们感觉不出来
    
    单线程程序：即，若有多个任务只能依次执行。当上一个任务执行结束后，下一个任务开始执行。如去            网吧上网，网吧只能让一个人上网，当这个人下机后，下一个人才能上网。
    多线程程序：即，若有多个任务可以同时执行。如，去网吧上网，网吧能够让多个人同时上网。

### 04迅雷的多线程下载
   A:迅雷的多线程下载
     多线程,每个线程都读一个文件

### 05线程的运行模式
   A:线程的运行模式
    a:分时调度
      所有线程轮流使用 CPU 的使用权，平均分配每个线程占用 CPU 的时间。
    
    b:抢占式调度
     优先让优先级高的线程使用 CPU，如果线程的优先级相同，那么会随机选择一个(线程随机性)，Java使用的为抢占式调度。
    
     大部分操作系统都支持多进程并发运行，现在的操作系统几乎都支持同时运行多个程序。比如：现在我们上课一边使用编辑器，一边使用录屏软件，同时还开着画图板，dos窗口等软件。此时，这些程序是在同时运行，”感觉这些软件好像在同一时刻运行着“。

     实际上，CPU(中央处理器)使用抢占式调度模式在多个线程间进行着高速的切换。对于CPU的一个核而言，某个时刻，只能执行一个线程，而 CPU的在多个线程间切换速度相对我们的感觉要快，看上去就是在同一时刻运行。
     其实，多线程程序并不能提高程序的运行速度，但能够提高程序运行效率，让CPU的使用率更高。


 
### 06main的主线程
  *A:main的主线程
    /*
     *  程序中的主线程
     */
    public class Demo {
      public static void main(String[] args) {
        System.out.println(0/0);
        function();
        System.out.println(Math.abs(-9));
      }
      
      public static void function(){
        for(int i = 0 ; i < 10000;i++){
          System.out.println(i);
        }
      }
    }



=======================第二节课开始=============================================
### 07Thread类介绍
  A:Thread类介绍:Thread是程序中的执行线程。Java 虚拟机允许应用程序并发地运行多个执行线程。
     发现创建新执行线程有两种方法。
     a:一种方法是将类声明为 Thread 的子类。该子类应重写 Thread 类的 run 方法。创建对象，开启线程。run方法相当于其他线程的main方法。
     b:另一种方法是声明一个实现 Runnable 接口的类。该类然后实现 run 方法。然后创建Runnable的子类对象，传入到某个线程的构造方法中，开启线程。


### 08实现线程程序继承Thread
   *A:实现线程程序继承Thread
	    /*
       * 创建和启动一个线程
       *   创建Thread子类对象
       *   子类对象调用方法start()
       *      让线程程序执行,JVM调用线程中的run
       */
      public class ThreadDemo {
        public static void main(String[] args) {
          SubThread st = new SubThread();
          SubThread st1 = new SubThread();
          st.start();
          st1.start();
          for(int i = 0; i < 50;i++){
            System.out.println("main..."+i);
          }
        }
      }
      /*
       *  定义子类,继承Thread 
       *  重写方法run 
       */
      public class SubThread  extends Thread{
        public void run(){
          for(int i = 0; i < 50;i++){
            System.out.println("run..."+i);
          }
        }
      }

	 


### 09线程执行的随机性
   *A:线程执行的随机性
    /*
      代码分析:
         整个程序就只有三个线程,
         一个是主线程
           启动另外两个线程
            st.start();
            st1.start();
            for(int i = 0; i < 50;i++){
              System.out.println("main..."+i);
            }
         一个是st(Thread-0)线程
         for(int i = 0; i < 50;i++){
           System.out.println("run..."+i);
         }
         一个是st1(Thread-1)线程下 

    */
     public class ThreadDemo {
       public static void main(String[] args) {
         SubThread st = new SubThread();
         SubThread st1 = new SubThread();
         st.start();
         st1.start();
         for(int i = 0; i < 50;i++){
           System.out.println("main..."+i);
         }
       }
     }
     /*
      *  定义子类,继承Thread 
      *  重写方法run 
      */
     public class SubThread  extends Thread{
       public void run(){
         for(int i = 0; i < 50;i++){
           System.out.println("run..."+i);
         }
       }
     }


### 10为什么要继承Thread
   *A:什么要继承Thread
    a:我们为什么要继承Thread类，并调用其的start方法才能开启线程呢？
       继承Thread类：因为Thread类用来描述线程，具备线程应该有功能。那为什么不直接创建Thread类的对象呢？
       如下代码：
        Thread t1 = new Thread();
        t1.start();//这样做没有错，但是该start调用的是Thread类中的run方法
                  //而这个run方法没有做什么事情，更重要的是这个run方法中并没有定义我们需要让线程执行的代码。

    b:创建线程的目的是什么？
     是为了建立程序单独的执行路径，让多部分代码实现同时执行。也就是说线程创建并执行需要给定线程要执行的任务。
     对于之前所讲的主线程，它的任务定义在main函数中。自定义线程需要执行的任务都定义在run方法中。

### 11多线程内存图解
   *A:多线程内存图解
      多线程执行时，到底在内存中是如何运行的呢？
        多线程执行时，在栈内存中，其实每一个执行线程都有一片自己所属的栈内存空间。进行方法的压栈和弹栈。
        当执行线程的任务结束了，线程自动在栈内存中释放了。但是当所有的执行线程都结束了，那么进程就结束了。
 

=======================第三节课开始=============================================
### 12获取线程名字Thread类方法getName
   *A:获取线程名字Thread类方法getName 
    /*
     *  获取线程名字,父类Thread方法
     *    String getName()
     */
    public class NameThread extends Thread{
      
      public NameThread(){
        super("小强");
      }
      
      public void run(){
        System.out.println(getName());
      }
    }
    
    /*
     *  每个线程,都有自己的名字
     *  运行方法main线程,名字就是"main"
     *  其他新键的线程也有名字,默认 "Thread-0","Thread-1"
     *  
     *  JVM开启主线程,运行方法main,主线程也是线程,是线程必然就是
     *  Thread类对象
     */
    public class ThreadDemo {
      public static void main(String[] args) {
        NameThread nt = new NameThread();
        nt.start();
        
         

      }
    }
### 13获取线程名字Thread类方法currentThread
  *A:获取线程名字Thread类方法currentThread
   /*
    *  获取线程名字,父类Thread方法
    *    String getName()
    */
   public class NameThread extends Thread{

     public void run(){
       System.out.println(getName());
     }
   }
   
   /*
    *  每个线程,都有自己的名字
    *  运行方法main线程,名字就是"main"
    *  其他新键的线程也有名字,默认 "Thread-0","Thread-1"
    *  
    *  JVM开启主线程,运行方法main,主线程也是线程,是线程必然就是
    *  Thread类对象
    *  Thread类中,静态方法
    *   static Thread currentThread()返回正在执行的线程对象
    */
   public class ThreadDemo {
     public static void main(String[] args) {
       NameThread nt = new NameThread();
       nt.start();
       
       /*Thread t =Thread.currentThread();
       System.out.println(t.getName());*/
       System.out.println(Thread.currentThread().getName());


     }
   }
 
### 14线程名字设置
   A:线程名字设置
      /*
       *  获取线程名字,父类Thread方法
       *    String getName()
       */
      public class NameThread extends Thread{
        
        public NameThread(){
          super("小强");
        }
        
        public void run(){
          System.out.println(getName());
        }
      }
      
      /*
       *  每个线程,都有自己的名字
       *  运行方法main线程,名字就是"main"
       *  其他新键的线程也有名字,默认 "Thread-0","Thread-1"
       *  
       *  JVM开启主线程,运行方法main,主线程也是线程,是线程必然就是
       *  Thread类对象
       *  Thread类中,静态方法
       *   static Thread currentThread()返回正在执行的线程对象
       */
      public class ThreadDemo {
        public static void main(String[] args) {
          NameThread nt = new NameThread();
          nt.setName("旺财");
          nt.start();

        }
      }


### 15Thread类方法sleep
   A:Thread类方法sleep
     public class ThreadDemo {
      public static void main(String[] args) throws Exception{
        /*for(int i = 0 ; i < 5 ;i++){
          Thread.sleep(50);
          System.out.println(i);
        }*/
        
        new SleepThread().start();
      }
     }
     
     public class SleepThread extends Thread{
      public void run(){
        for(int i = 0 ; i < 5 ;i++){
          try{
            Thread.sleep(500);//睡眠500ms,500ms已到并且cpu切换到该线程继续向下执行
          }catch(Exception ex){
            
          }
          System.out.println(i);
        }
      }
     }

 
   
### 16实现线程的另一种方式实现Runnable接口
   A:实现线程的另一种方式实现Runnable接口
	   /*
      *  实现接口方式的线程
      *    创建Thread类对象,构造方法中,传递Runnable接口实现类
      *    调用Thread类方法start()
      */
     public class ThreadDemo {
      public static void main(String[] args) {
        SubRunnable sr = new SubRunnable();
        Thread t = new Thread(sr);
        t.start();
        for(int i = 0 ; i < 50; i++){
          System.out.println("main..."+i);
        }
      }
     }
   
     /*
      *  实现线程成功的另一个方式,接口实现
      *  实现接口Runnable,重写run方法
      */
     public class SubRunnable implements Runnable{
      public void run(){
        for(int i = 0 ; i < 50; i++){
          System.out.println("run..."+i);
        }
      }
     }


### 17实现接口方式的好处 
    A:实现接口方式的好处
     第二种方式实现Runnable接口避免了单继承的局限性，所以较为常用。
     实现Runnable接口的方式，更加的符合面向对象，线程分为两部分，一部分线程对象，一部分线程任务。
     继承Thread类，线程对象和线程任务耦合在一起。
     一旦创建Thread类的子类对象，既是线程对象，有又有线程任务。
     实现runnable接口，将线程任务单独分离出来封装成对象，类型就是Runnable接口类型。Runnable接口对线程对象和线程任务进行解耦。
     (降低紧密性或者依赖性,创建线程和执行任务不绑定)

### 18匿名内部类实现线程程序 
    *A:匿名内部类实现线程程序 
    /*
     *  使用匿名内部类,实现多线程程序
     *  前提: 继承或者接口实现
     *  new 父类或者接口(){
     *     重写抽象方法
     *  }
     */
    public class ThreadDemo {
      public static void main(String[] args) {
        //继承方式  XXX extends Thread{ public void run(){}}
        new Thread(){
          public void run(){
            System.out.println("!!!");
          }
        }.start();
        
        //实现接口方式  XXX implements Runnable{ public void run(){}}
        
        Runnable r = new Runnable(){
          public void run(){
            System.out.println("### ");
          }
        };
        new Thread(r).start();
        
        
        new Thread(new Runnable(){
          public void run(){
            System.out.println("@@@");
          }
        }).start();
        
      }
    }
=======================第四节课开始=============================================

### 19线程的状态图
   A:线程的状态图
	    a:参见线程状态图.jpg

### 20线程池的原理
   A:线程池的原理
      1.在java中，如果每个请求到达就创建一个新线程，开销是相当大的。
      2.在实际使用中，创建和销毁线程花费的时间和消耗的系统资源都相当大，甚至可能要比在处理实际的用户请求的时间和资源要多的多。
      3.除了创建和销毁线程的开销之外，活动的线程也需要消耗系统资源。
        如果在一个jvm里创建太多的线程，可能会使系统由于过度消耗内存或“切换过度”而导致系统资源不足。
        为了防止资源不足，需要采取一些办法来限制任何给定时刻处理的请求数目，尽可能减少创建和销毁线程的次数，特别是一些资源耗费比较大的线程的创建和销毁，尽量利用已有对象来进行服务。
      线程池主要用来解决线程生命周期开销问题和资源不足问题。通过对多个任务重复使用线程，线程创建的开销就被分摊到了多个任务上了，而且由于在请求到达时线程已经存在，所以消除了线程创建所带来的延迟。这样，就可以立即为请求服务，使用应用程序响应更快。另外，通过适当的调整线程中的线程数目可以防止出现资源不足的情况。


### 21JDK5实现线程池
    A:JDK5实现线程池
	    /*
       *  JDK1.5新特性,实现线程池程序
       *  使用工厂类 Executors中的静态方法创建线程对象,指定线程的个数
       *   static ExecutorService newFixedThreadPool(int 个数) 返回线程池对象
       *   返回的是ExecutorService接口的实现类 (线程池对象)
       *   
       *   接口实现类对象,调用方法submit (Ruunable r) 提交线程执行任务
       *          
       */
      public class ThreadPoolDemo {
        public static void main(String[] args) {
          //调用工厂类的静态方法,创建线程池对象
          //返回线程池对象,是返回的接口
          ExecutorService es = Executors.newFixedThreadPool(2);
            //调用接口实现类对象es中的方法submit提交线程任务
          //将Runnable接口实现类对象,传递
          es.submit(new ThreadPoolRunnable());
          es.submit(new ThreadPoolRunnable());
          es.submit(new ThreadPoolRunnable());
        
        }
      }

      public class ThreadPoolRunnable implements Runnable {
        public void run(){
          System.out.println(Thread.currentThread().getName()+" 线程提交任务");
        }
      }


### 22实现线程的Callable接口方式
  A:实现线程的Callable接口方式
     /*
      *  实现线程程序的第三个方式,实现Callable接口方式
      *  实现步骤
      *    工厂类 Executors静态方法newFixedThreadPool方法,创建线程池对象
      *    线程池对象ExecutorService接口实现类,调用方法submit提交线程任务
      *    submit(Callable c)
      */
     public class ThreadPoolDemo1 {
      public static void main(String[] args)throws Exception {
        ExecutorService es = Executors.newFixedThreadPool(2);
        //提交线程任务的方法submit方法返回 Future接口的实现类
        Future<String> f = es.submit(new ThreadPoolCallable());
        String s = f.get();
        System.out.println(s);
      }
     }
     /*
      * Callable 接口的实现类,作为线程提交任务出现
      * 使用方法返回值
      */

     import java.util.concurrent.Callable;

     public class ThreadPoolCallable implements Callable<String>{
      public String call(){
        return "abc";
      }
     }


### 23线程实现异步计算
  A:线程实现异步计算


    /*
     * 使用多线程技术,求和
     * 两个线程,1个线程计算1+100,另一个线程计算1+200的和
     * 多线程的异步计算
     */
    public class ThreadPoolDemo {
      public static void main(String[] args)throws Exception {
        ExecutorService es = Executors.newFixedThreadPool(2);
        Future<Integer> f1 =es.submit(new GetSumCallable(100));
        Future<Integer> f2 =es.submit(new GetSumCallable(200));
        System.out.println(f1.get());
        System.out.println(f2.get());
        es.shutdown();
      }
    }

     

    public class GetSumCallable implements Callable<Integer>{
      private int a;
      public GetSumCallable(int a){
        this.a=a;
      }
      
      public Integer call(){
        int sum = 0 ;
        for(int i = 1 ; i <=a ; i++){
          sum = sum + i ;
        }
        return sum;
      }
    }
今日内容介绍
1、多线程安全问题
2、等待唤醒机制

 
 


=======================第一节课开始=============================================

### 01线程操作共享数据的安全问题
  *A:线程操作共享数据的安全问题
    如果有多个线程在同时运行，而这些线程可能会同时运行这段代码。
    程序每次运行结果和单线程运行的结果是一样的，而且其他的变量的值也和预期的是一样的，就是线程安全的。
  
### 02售票的案例
 *A:售票的案例
     /*
      * 多线程并发访问同一个数据资源
      * 3个线程,对一个票资源,出售
      */
     public class ThreadDemo {
      public static void main(String[] args) {
        //创建Runnable接口实现类对象
        Tickets t = new Tickets();
        //创建3个Thread类对象,传递Runnable接口实现类
        Thread t0 = new Thread(t);
        Thread t1 = new Thread(t);
        Thread t2 = new Thread(t);
        
        t0.start();
        t1.start();
        t2.start();
        
      }
     }
    
     public class Tickets implements Runnable{
      
      //定义出售的票源
      private int ticket = 100;
      private Object obj = new Object();
      
      public void run(){
        while(true){
       
            if( ticket > 0){
              
              System.out.println(Thread.currentThread().getName()+" 出售第 "+ticket--);
            }
          
        }
      }
     }


### 03线程安全问题引发
 *A:线程安全问题引发
    /*
     * 多线程并发访问同一个数据资源
     * 3个线程,对一个票资源,出售
     */
    public class ThreadDemo {
     public static void main(String[] args) {
       //创建Runnable接口实现类对象
       Tickets t = new Tickets();
       //创建3个Thread类对象,传递Runnable接口实现类
       Thread t0 = new Thread(t);
       Thread t1 = new Thread(t);
       Thread t2 = new Thread(t);
       
       t0.start();
       t1.start();
       t2.start();
       
     }
    }
    /*
     *  通过线程休眠,出现安全问题
     */
    public class Tickets implements Runnable{
     
     //定义出售的票源
     private int ticket = 100;
     private Object obj = new Object();
     
     public void run(){
       while(true){
 
         //对票数判断,大于0,可以出售,变量--操作
           if( ticket > 0){
             try{
                Thread.sleep(10); //加了休眠让其他线程有执行机会
             }catch(Exception ex){}
             System.out.println(Thread.currentThread().getName()+" 出售第 "+ticket--);
           }
       }
     }
    }

### 04同步代码块解决线程安全问题
  *A:同步代码块解决线程安全问题
      *A:售票的案例
          /*
           * 多线程并发访问同一个数据资源
           * 3个线程,对一个票资源,出售
           */
          public class ThreadDemo {
           public static void main(String[] args) {
             //创建Runnable接口实现类对象
             Tickets t = new Tickets();
             //创建3个Thread类对象,传递Runnable接口实现类
             Thread t0 = new Thread(t);
             Thread t1 = new Thread(t);
             Thread t2 = new Thread(t);
             
             t0.start();
             t1.start();
             t2.start();
             
           }
          }
          /*
           *  通过线程休眠,出现安全问题
           *  解决安全问题,Java程序,提供技术,同步技术
           *  公式:
           *    synchronized(任意对象){
           *      线程要操作的共享数据
           *    }
           *    同步代码块
           */
          public class Tickets implements Runnable{
           
           //定义出售的票源
           private int ticket = 100;
           private Object obj = new Object();
           
           public void run(){
             while(true){
               //线程共享数据,保证安全,加入同步代码块
               synchronized(obj){
               //对票数判断,大于0,可以出售,变量--操作
                 if( ticket > 0){
                   try{
                      Thread.sleep(10);
                   }catch(Exception ex){}
                   System.out.println(Thread.currentThread().getName()+" 出售第 "+ticket--);
                 }
               }
             }
           }
          }

### 05同步代码块的执行原理
   A:同步代码块的执行原理
     同步代码块: 在代码块声明上 加上synchronized
     synchronized (锁对象) {
       可能会产生线程安全问题的代码
     }
     同步代码块中的锁对象可以是任意的对象；但多个线程时，要使用同一个锁对象才能够保证线程安全。


=======================第二节课开始============================================= 
### 06同步的上厕所原理
  *A:同步的上厕所原理
    a:不使用同步:线程在执行的过程中会被打扰
       线程比喻成人
       线程执行代码就是上一个厕所
      第一个人正在上厕所,上到一半,被另外一个人拉出来
    b:使用同步:
       线程比喻成人
       线程执行代码就是上一个厕所
       锁比喻成厕所门
      第一个人上厕所,会锁门
      第二个人上厕所,看到门锁上了,等待第一个人上完再去上厕所


### 07同步方法
  *A:同步方法:
  /*
   * 多线程并发访问同一个数据资源
   * 3个线程,对一个票资源,出售
   */
  public class ThreadDemo {
    public static void main(String[] args) {
      //创建Runnable接口实现类对象
      Tickets t = new Tickets();
      //创建3个Thread类对象,传递Runnable接口实现类
      Thread t0 = new Thread(t);
      Thread t1 = new Thread(t);
      Thread t2 = new Thread(t);
      
      t0.start();
      t1.start();
      t2.start();
      
    }
  }

  *A:同步方法
     /*
      *  采用同步方法形式,解决线程的安全问题
      *  好处: 代码简洁
      *  将线程共享数据,和同步,抽取到一个方法中
      *  在方法的声明上,加入同步关键字
      *  
      *  问题:
      *    同步方法有锁吗,肯定有,同步方法中的对象锁,是本类对象引用 this
      *    如果方法是静态的呢,同步有锁吗,绝对不是this
      *    锁是本类自己.class 属性
      *    静态方法,同步锁,是本类类名.class属性
      */
     public class Tickets implements Runnable{

      //定义出售的票源
      private  int ticket = 100;
      
      public void run(){
        while(true){
          payTicket();
        }
      }
      
      public  synchronized void payTicket(){  
          if( ticket > 0){
            try{
               Thread.sleep(10);
            }catch(Exception ex){}
            System.out.println(Thread.currentThread().getName()+" 出售第 "+ticket--);
          }
        
      }
     }



### 08JDK1.5新特性Lock接口
   *A:JDK1.5新特性Lock接口
	    查阅API，查阅Lock接口描述，Lock 实现提供了比使用 synchronized 方法和语句可获得的更广泛的锁定操作。
       Lock接口中的常用方法
            void lock()
            void unlock()
      Lock提供了一个更加面对对象的锁，在该锁中提供了更多的操作锁的功能。
      我们使用Lock接口,以及其中的lock()方法和unlock()方法替代同步，对电影院卖票案例中Ticket



### 09Lock接口改进售票案例
   *A:Lock接口改进售票案例
      /*
       * 多线程并发访问同一个数据资源
       * 3个线程,对一个票资源,出售
       */
      public class ThreadDemo {
        public static void main(String[] args) {
          //创建Runnable接口实现类对象
          Tickets t = new Tickets();
          //创建3个Thread类对象,传递Runnable接口实现类
          Thread t0 = new Thread(t);
          Thread t1 = new Thread(t);
          Thread t2 = new Thread(t);
          
          t0.start();
          t1.start();
          t2.start();
          
        }
      }
      /*
       *  使用JDK1.5 的接口Lock,替换同步代码块,实现线程的安全性
       *  Lock接口方法:
       *     lock() 获取锁
       *     unlock()释放锁
       *  实现类ReentrantLock
       */
      public class Tickets implements Runnable{
        
        //定义出售的票源
        private int ticket = 100;
        //在类的成员位置,创建Lock接口的实现类对象
        private Lock lock = new ReentrantLock();
        
        public void run(){
          while(true){
            //调用Lock接口方法lock获取锁
              lock.lock();
            //对票数判断,大于0,可以出售,变量--操作
              if( ticket > 0){
                try{
                   Thread.sleep(10);
                   System.out.println(Thread.currentThread().getName()+" 出售第 "+ticket--);
                }catch(Exception ex){
                  
                }finally{
                  //释放锁,调用Lock接口方法unlock
                  lock.unlock();
                }
              }
          }
        }
      }

=======================第三节课开始============================================= 
### 10线程的死锁原理
   *A:线程的死锁原理  
     当线程任务中出现了多个同步(多个锁)  时，如果同步中嵌套了其他的同步。这时容易引发一种现象：程序出现无限等待，这种现象我们称为死锁。这种情况能避免就避免掉。
        synchronzied(A锁){
            synchronized(B锁){
                      
            }
        }


### 11线程的死锁代码实现
   *A:线程的死锁代码实现
       public class DeadLock implements Runnable{
        private int i = 0;
        public void run(){
          while(true){
            if(i%2==0){
              //先进入A同步,再进入B同步
              synchronized(LockA.locka){
                System.out.println("if...locka");
                synchronized(LockB.lockb){
                  System.out.println("if...lockb");
                }
              }
            }else{
              //先进入B同步,再进入A同步
              synchronized(LockB.lockb){
                System.out.println("else...lockb");
                synchronized(LockA.locka){
                  System.out.println("else...locka");
                }
              }
            }
            i++;
          }
        }
       }
    
      public class DeadLockDemo {
        public static void main(String[] args) {
          DeadLock dead = new DeadLock();
          Thread t0 = new Thread(dead);
          Thread t1 = new Thread(dead);
          t0.start();
          t1.start();
        }
      }


      public class LockA {
        private LockA(){}
        
        public  static final LockA locka = new LockA();
      }

      
      public class LockB {
        private LockB(){}
        
        public static final LockB lockb = new LockB();
      }



 ### 12线程等待与唤醒案例介绍
   *A:线程等待与唤醒案例介绍 
     等待唤醒机制所涉及到的方法：
         wait（） :等待，将正在执行的线程释放其执行资格 和 执行权，并存储到线程池中。
         notify（）：唤醒，唤醒线程池中被wait（）的线程，一次唤醒一个，而且是任意的。
         notifyAll（）： 唤醒全部：可以将线程池中的所有wait() 线程都唤醒。
       其实，所谓唤醒的意思就是让 线程池中的线程具备执行资格。必须注意的是，这些方法都是在 同步中才有效。同时这些方法在使用时必须标明所属锁，这样才可以明确出这些方法操作的到底是哪个锁上的线程。




### 13线程等待与唤醒案例资源类编写
  *A:线程等待与唤醒案例资源类编写
    /*
     *  定义资源类,有2个成员变量
     *  name,sex
     *  同时有2个线程,对资源中的变量操作
     *  1个对name,age赋值
     *  2个对name,age做变量的输出打印
     */
    public class Resource {
      public String name;
      public String sex;
    }

 
### 14线程等待与唤醒案例输入和输出线程
   A:线程等待与唤醒案例输入和输出线程
     /*
       *  输入的线程,对资源对象Resource中成员变量赋值
       *  一次赋值 张三,男
       *  下一次赋值 lisi,nv
     */
      public class Input implements Runnable {
        private Resource r=new Resource();
       
        public void run() {
          int i=0;
          while(true){
            if(i%2==0){
               r.name="张三";
               r.sex="男";
             }else{
                r.name="lisi";
                r.sex="女";
              }
            i++;
          }
        }
      }

      /*
       *  输出线程,对资源对象Resource中成员变量,输出值
       */
      public class Output implements Runnable {
        private Resource r=new Resource() ;
         
        public void run() {
          while(true){
             System.out.println(r.name+"..."+r.sex); 
            }
          }
      }

=================================第四节课=========================================
### 15线程等待与唤醒案例测试类
   A:线程等待与唤醒案例测试类
      /*
       *  开启输入线程和输出线程,实现赋值和打印值
       */
      public class ThreadDemo{
        public static void main(String[] args) {
          
          Resource r = new Resource();
          
          Input in = new Input();
          Output out = new Output();
          
          Thread tin = new Thread(in);
          Thread tout = new Thread(out);
          
          tin.start();
          tout.start();
        }
      }


 
   
### 16线程等待与唤醒案例null值解决
   A:线程等待与唤醒案例null值解决
	    /*
        *  输入的线程,对资源对象Resource中成员变量赋值
        *  一次赋值 张三,男
        *  下一次赋值 lisi,nv
      */
       public class Input implements Runnable {
         private Resource r;
         public Input(Resource r){
           this.r=r;
         }
        
         public void run() {
           int i=0;
           while(true){
             if(i%2==0){
                r.name="张三";
                r.sex="男";
              }else{
                 r.name="lisi"
                 r.sex="女"
               }
             i++;
           }
         }
       }

       /*
        *  输出线程,对资源对象Resource中成员变量,输出值
        */ 
       public class Output implements Runnable {
         private Resource r;
         public Output(Resource r){
            this.r=r;
         } 
         public void run() {
           while(true){
              System.out.println(r.name+"..."+r.sex); 
             }
           }
         }

       }
       /*
        *  开启输入线程和输出线程,实现赋值和打印值
        */
       public class ThreadDemo{
         public static void main(String[] args) {
           
           Resource r = new Resource();
           
           Input in = new Input(r);
           Output out = new Output(r);
           
           Thread tin = new Thread(in);
           Thread tout = new Thread(out);
           
           tin.start();
           tout.start();
         }
       }



### 17线程等待与唤醒案例数据安全解决
    A:线程等待与唤醒案例数据安全解决
            /*
              *  输入的线程,对资源对象Resource中成员变量赋值
              *  一次赋值 张三,男
              *  下一次赋值 lisi,nv
            */
             public class Input implements Runnable {
               private Resource r;
               public Input(Resource r){
                 this.r=r;
               }
              
               public void run() {
                 int i=0;
                 while(true){
                  synchronized(r){
                   if(i%2==0){
                      r.name="张三";
                      r.sex="男";
                    }else{
                       r.name="lisi"
                       r.sex="女"
                     }
                   i++;
                 }

               }
             }

             /*
              *  输出线程,对资源对象Resource中成员变量,输出值
              */ 
             public class Output implements Runnable {
               private Resource r;
               public Output(Resource r){
                  this.r=r;
               } 
               public void run() {
                 while(true){
                    synchronized(r){
                     System.out.println(r.name+"..."+r.sex); 
                    }
                   }
                 }
               }

             }
             /*
              *  开启输入线程和输出线程,实现赋值和打印值
              */
             public class ThreadDemo{
               public static void main(String[] args) {
                 
                 Resource r = new Resource();
                 
                 Input in = new Input(r);
                 Output out = new Output(r);
                 
                 Thread tin = new Thread(in);
                 Thread tout = new Thread(out);
                 
                 tin.start();
                 tout.start();
               }
             }


### 18线程等待与唤醒案例通信的分析
    *A:线程等待与唤醒案例通信的分析
        输入:赋值后,执行方法wait()永远等待
        输出:变量值打印输出,在输出等待之前,唤醒
        输入的notify(),自己在wait()永远等待
        输入:被唤醒后,重新对变量赋值,赋值后,必须唤醒输出的线程notify(),
             自己的wait()

### 19线程等待与唤醒案例的实现
   *A 线程等待与唤醒案例的实现

     /*
      *  定义资源类,有2个成员变量
      *  name,sex
      *  同时有2个线程,对资源中的变量操作
      *  1个对name,age赋值
      *  2个对name,age做变量的输出打印
      */
     public class Resource {
      public String name;
      public String sex;
      public boolean flag = false;
     }

     /*
      *  输入的线程,对资源对象Resource中成员变量赋值
      *  一次赋值 张三,男
      *  下一次赋值 lisi,nv
      */
     public class Input implements Runnable {
      private Resource r ;
      
      public Input(Resource r){
        this.r = r;
      }
      
      public void run() {
        int i = 0 ;
        while(true){
          synchronized(r){
            //标记是true,等待
              if(r.flag){
                try{r.wait();}catch(Exception ex){}
              }
            
            if(i%2==0){
              r.name = "张三";
              r.sex = "男";
            }else{
              r.name = "lisi";
              r.sex = "nv";
            }
            //将对方线程唤醒,标记改为true
            r.flag = true;
            r.notify();
          }
          i++;
        }
      }

     }
     
     /*
      *  输出线程,对资源对象Resource中成员变量,输出值
      */
     public class Output implements Runnable {
      private Resource r ;
      
      public Output(Resource r){
        this.r = r;
      }
      public void run() {
        while(true){
          synchronized(r){  
            //判断标记,是false,等待
          if(!r.flag){
            try{r.wait();}catch(Exception ex){}
            }
          System.out.println(r.name+".."+r.sex);
          //标记改成false,唤醒对方线程
          r.flag = false;
          r.notify();
          }
        }
      }

     }

     /*
      *  开启输入线程和输出线程,实现赋值和打印值
      */
     public class ThreadDemo{
      public static void main(String[] args) {
        
        Resource r = new Resource();
        
        Input in = new Input(r);
        Output out = new Output(r);
        
        Thread tin = new Thread(in);
        Thread tout = new Thread(out);
        
        tin.start();
        tout.start();
      }
     }

### 20eclipse问题
   A:eclipse问题
   

 
今日内容介绍
1、网络三要素及传输协议
2、实现UDP协议的发送端和接收端
3、实现TCP协议的客户端和服务器
4、TCP上传文件案例
 


=======================第一节课开始=============================================

### 01网络模型
  *A:网络模型
     TCP/IP协议中的四层分别是应用层、传输层、网络层和链路层，每层分别负责不同的通信功能，接下来针对这四层进行详细地讲解。
       链路层：链路层是用于定义物理传输通道，通常是对某些网络连接设备的驱动协议，例如针对光纤、网线提供的驱动。
       网络层：网络层是整个TCP/IP协议的核心，它主要用于将传输的数据进行分组，将分组数据发送到目标计算机或者网络。
       传输层：主要使网络程序进行通信，在进行网络通信时，可以采用TCP协议，也可以采用UDP协议。
       应用层：主要负责应用程序的协议，例如HTTP协议、FTP协议等。

### 02IP地址
 *A:IP地址
      在TCP/IP协议中，这个标识号就是IP地址，它可以唯一标识一台计算机，
      目前，IP地址广泛使用的版本是IPv4，它是由4个字节大小的二进制数来表示，如：00001010000000000000000000000001。
      由于二进制形式表示的IP地址非常不便记忆和处理，因此通常会将IP地址写成十进制的形式，
      每个字节用一个十进制数字(0-255)表示，数字间用符号“.”分开，如 “192.168.1.100”
      127.0.0.1 为本地主机地址(本地回环地址)
### 03端口号
 *A:端口号
    通过IP地址可以连接到指定计算机，但如果想访问目标计算机中的某个应用程序，还需要指定端口号。
    在计算机中，不同的应用程序是通过端口号区分的。
    端口号是用两个字节（16位的二进制数）表示的，它的取值范围是0~65535，
    其中，0~1023之间的端口号用于一些知名的网络服务和应用，用户的普通应用程序需要使用1024以上的端口号，从而避免端口号被另外一个应用或服务所占用

### 04InetAddress类
  *A:InetAddress类
     /*
      *  表示互联网中的IP地址
      *    java.net.InetAddress
      *  静态方法
      *    static InetAddress  getLocalHost()   LocalHost本地主机
      *    返回本地主机,返回值InetAddress对象
      *    
      *    static InetAddress getByName(String hostName)传递主机名,获取IP地址对象
      *    
      *  非静态方法
      *     String getHoustAddress()获取主机IP地址
      *     String getHoustName()获取主机名
      *    
      */
     public class InetAddressDemo {
      public static void main(String[] args)throws UnknownHostException {
        function_1();
      }
      /*
       * static InetAddress getByName(String hostName)传递主机名,获取IP地址对象
       */
      public static void function_1()throws UnknownHostException {
        InetAddress inet = InetAddress.getByName("www.baidu.com");
        System.out.println(inet);
      }
      
      /*
       *  static InetAddress  getLocalHost()   LocalHost本地主机
       */
      public static void function() throws UnknownHostException{
        InetAddress inet = InetAddress.getLocalHost();
        //输出结果就是主机名,和 IP地址
        System.out.println(inet.toString());
        
        String ip = inet.getHostAddress();
        String name = inet.getHostName();
        System.out.println(ip+"   "+name);
        
        /*String host = inet.toString();
        String[] str = host.split("/");
        for(String s : str){
          System.out.println(s);
        }*/
      }
     }


### 05UDP协议
   A:UDP协议
     a:UDP协议概述:
      UDP是无连接通信协议，即在数据传输时，数据的发送端和接收端不建立逻辑连接。
      简单来说，当一台计算机向另外一台计算机发送数据时，发送端不会确认接收端是否存在，就会发出数据，同样接收端在收到数据时，也不会向发送端反馈是否收到数据。
     b:UDP协议特点:
      由于使用UDP协议消耗资源小，通信效率高，所以通常都会用于音频、视频和普通数据的传输例如视频会议都使用UDP协议，
      因为这种情况即使偶尔丢失一两个数据包，也不会对接收结果产生太大影响。


### 06TCP协议
  *A:TCP协议
    TCP协议是面向连接的通信协议，即在传输数据前先在发送端和接收端建立逻辑连接，然后再传输数据，它提供了两台计算机之间可靠无差错的数据传输。
    在TCP连接中必须要明确客户端与服务器端，
      由客户端向服务端发出连接请求，每次连接的创建都需要经过“三次握手”。
      第一次握手，客户端向服务器端发出连接请求，等待服务器确认
      第二次握手，服务器端向客户端回送一个响应，通知客户端收到了连接请求
      第三次握手，客户端再次向服务器端发送确认信息，确认连接

========================================第二节课=========================================
### 07数据包和发送对象介绍
  *A:数据包和发送对象介绍:
    DatagramPacket数据包的作用就如同是“集装箱”，
       可以将发送端或者接收端的数据封装起来。然而运输货物只有“集装箱”是不够的，还需要有码头。
       在程序中需要实现通信只有DatagramPacket数据包也同样不行，为此JDK中提供的一个DatagramSocket类。
       DatagramSocket类的作用就类似于码头，使用这个类的实例对象就可以发送和接收DatagramPacket数据包
    DatagramPacket:封装数据
    DatagramSocket:发送DatagramPacket

### 08UDP发送端
   *A:UDP发送端
	     /*
        *  实现UDP协议的发送端:
        *    实现封装数据的类 java.net.DatagramPacket  将你的数据包装
        *    实现数据传输的类 java.net.DatagramSocket  将数据包发出去
        *    
        *  实现步骤:
        *    1. 创建DatagramPacket对象,封装数据, 接收的地址和端口
        *    2. 创建DatagramSocket
        *    3. 调用DatagramSocket类方法send,发送数据包
        *    4. 关闭资源
        *    
        *    DatagramPacket构造方法:
        *      DatagramPacket(byte[] buf, int length, InetAddress address, int port) 
        *      
        *    DatagramSocket构造方法:
        *      DatagramSocket()空参数
        *      方法: send(DatagramPacket d)
        *      
        */
       public class UDPSend {
        public static void main(String[] args) throws IOException{
          //创建数据包对象,封装要发送的数据,接收端IP,端口
          byte[] date = "你好UDP".getBytes();
          //创建InetAddress对象,封装自己的IP地址
          InetAddress inet = InetAddress.getByName("127.0.0.1");
          DatagramPacket dp = new DatagramPacket(date, date.length, inet,6000);
          //创建DatagramSocket对象,数据包的发送和接收对象
          DatagramSocket ds = new DatagramSocket();
          //调用ds对象的方法send,发送数据包
          ds.send(dp);
          //关闭资源
          ds.close();
        }
       }



### 09UDP接收端
   *A:UDP接收端
       /*
        *  实现UDP接收端
        *    实现封装数据包 java.net.DatagramPacket 将数据接收
        *    实现输出传输     java.net.DatagramSocket 接收数据包
        *    
        *  实现步骤:
        *     1. 创建DatagramSocket对象,绑定端口号
        *         要和发送端端口号一致
        *     2. 创建字节数组,接收发来的数据
        *     3. 创建数据包对象DatagramPacket
        *     4. 调用DatagramSocket对象方法
        *        receive(DatagramPacket dp)接收数据,数据放在数据包中
        *     5. 拆包
        *          发送的IP地址
        *            数据包对象DatagramPacket方法getAddress()获取的是发送端的IP地址对象
        *            返回值是InetAddress对象
        *          接收到的字节个数
        *            数据包对象DatagramPacket方法 getLength()
        *          发送方的端口号
        *            数据包对象DatagramPacket方法 getPort()发送端口
        *     6. 关闭资源
        */
       public class UDPReceive {
        public static void main(String[] args)throws IOException {
          //创建数据包传输对象DatagramSocket 绑定端口号
          DatagramSocket ds = new DatagramSocket(6000);
          //创建字节数组
          byte[] data = new byte[1024];
          //创建数据包对象,传递字节数组
          DatagramPacket dp = new DatagramPacket(data, data.length);
          //调用ds对象的方法receive传递数据包
          ds.receive(dp);
          
      
        }
       }


### 10UDP接收端的拆包
   *A:UDP接收端的拆包 
      
      /*
       *  实现UDP接收端
       *    实现封装数据包 java.net.DatagramPacket 将数据接收
       *    实现输出传输     java.net.DatagramSocket 接收数据包
       *    
       *  实现步骤:
       *     1. 创建DatagramSocket对象,绑定端口号
       *         要和发送端端口号一致
       *     2. 创建字节数组,接收发来的数据
       *     3. 创建数据包对象DatagramPacket
       *     4. 调用DatagramSocket对象方法
       *        receive(DatagramPacket dp)接收数据,数据放在数据包中
       *     5. 拆包
       *          发送的IP地址
       *            数据包对象DatagramPacket方法getAddress()获取的是发送端的IP地址对象
       *            返回值是InetAddress对象
       *          接收到的字节个数
       *            数据包对象DatagramPacket方法 getLength()
       *          发送方的端口号
       *            数据包对象DatagramPacket方法 getPort()发送端口
       *     6. 关闭资源
       */
      public class UDPReceive {
        public static void main(String[] args)throws IOException {
          //创建数据包传输对象DatagramSocket 绑定端口号
          DatagramSocket ds = new DatagramSocket(6000);
          //创建字节数组
          byte[] data = new byte[1024];
          //创建数据包对象,传递字节数组
          DatagramPacket dp = new DatagramPacket(data, data.length);
          //调用ds对象的方法receive传递数据包
          ds.receive(dp);
          
          //获取发送端的IP地址对象
          String ip=dp.getAddress().getHostAddress();
          
          //获取发送的端口号
          int port = dp.getPort();
          
          //获取接收到的字节个数
          int length = dp.getLength();
          System.out.println(new String(data,0,length)+"..."+ip+":"+port);
          ds.close();
        }
      }



### 11键盘输入的聊天
   *A:键盘输入的聊天
    *a:发送端:
      /*
       * 实现UDP发送,键盘输入的形式
       * 输入完毕,发送给接收端      
       */
      public class UDPSend {
        public static void main(String[] args) throws IOException{
          Scanner sc = new Scanner(System.in);
          DatagramSocket ds = new DatagramSocket();
          InetAddress inet = InetAddress.getByName("127.0.0.1");
          while(true){
          String message = sc.nextLine();
          /*if("886".equals(message)){
            break;
          }*/
          byte[] date = message.getBytes();
          DatagramPacket dp = new DatagramPacket(date, date.length, inet,6000);
          ds.send(dp);
          }
        //  ds.close();
        }
      }
       
       

       /*
        *  实现UDP接收端
        *  永不停歇的接收端
        */
       public class UDPReceive {
        public static void main(String[] args)throws IOException {
          //创建数据包传输对象DatagramSocket 绑定端口号
          DatagramSocket ds = new DatagramSocket(6000);
          //创建字节数组
          byte[] data = new byte[1024];
          //创建数据包对象,传递字节数组
          while(true){
          DatagramPacket dp = new DatagramPacket(data, data.length);
          //调用ds对象的方法receive传递数据包
          ds.receive(dp);
          
          //获取发送端的IP地址对象
          String ip=dp.getAddress().getHostAddress();
          
          //获取发送的端口号
          int port = dp.getPort();
          
          //获取接收到的字节个数
          int length = dp.getLength();
          System.out.println(new String(data,0,length)+"..."+ip+":"+port);
          }
          //ds.close();
        }
       }

=======================第三节课======================================
### 12TCP的客户端和服务器
   *A:TCP的客户端和服务器
      TCP通信同UDP通信一样，都能实现两台计算机之间的通信，通信的两端都需要创建socket对象。
      区别在于，UDP中只有发送端和接收端，不区分客户端与服务器端，计算机之间可以任意地发送数据。
      而TCP通信是严格区分客户端与服务器端的，在通信时，必须先由客户端去连接服务器端才能实现通信，
      服务器端不可以主动连接客户端，并且服务器端程序需要事先启动，等待客户端的连接。
      在JDK中提供了两个类用于实现TCP程序，一个是ServerSocket类，用于表示服务器端，一个是Socket类，用于表示客户端。
      通信时，首先创建代表服务器端的ServerSocket对象，该对象相当于开启一个服务，并等待客户端的连接，然后创建代表客户端的Socket对象向服务器端发出连接请求，服务器端响应请求，两者建立连接开始通信。


### 13TCP的客户端程序
  *A:TCP的客户端程序
   /*
    *  实现TCP客户端,连接到服务器
    *  和服务器实现数据交换
    *  实现TCP客户端程序的类 java.net.Socket
    *  
    *  构造方法:
    *      Socket(String host, int port)  传递服务器IP和端口号
    *      注意:构造方法只要运行,就会和服务器进行连接,连接失败,抛出异常
    *      
    *    OutputStream  getOutputStream() 返回套接字的输出流
    *      作用: 将数据输出,输出到服务器
    *      
    *    InputStream getInputStream() 返回套接字的输入流
    *      作用: 从服务器端读取数据
    *      
    *    客户端服务器数据交换,必须使用套接字对象Socket中的获取的IO流,自己new流,不行
    */
   public class TCPClient {
    public static void main(String[] args)throws IOException {
      //创建Socket对象,连接服务器
      Socket socket = new Socket("127.0.0.1", 8888);
      //通过客户端的套接字对象Socket方法,获取字节输出流,将数据写向服务器
      OutputStream out = socket.getOutputStream();
      out.write("服务器OK".getBytes());
      
 
      
      socket.close();
    }
   }

 
### 14TCP的服务器程序accept方法
   A:TCP的服务器程序accept方法
     /*
      *  实现TCP服务器程序
      *  表示服务器程序的类 java.net.ServerSocket
      *  构造方法:
      *    ServerSocket(int port) 传递端口号
      *  
      *  很重要的事情: 必须要获得客户端的套接字对象Socket
      *    Socket  accept()
      */
     public class TCPServer {
      public static void main(String[] args) throws IOException{
        ServerSocket server = new ServerSocket(8888);
        //调用服务器套接字对象中的方法accept() 获取客户端套接字对象
        Socket socket = server.accept();
        //通过客户端套接字对象,socket获取字节输入流,读取的是客户端发送来的数据
        InputStream in = socket.getInputStream();
        byte[] data = new byte[1024];
        int len = in.read(data);
        System.out.println(new String(data,0,len));
      
        
        socket.close();
        server.close();
      }
     }


### 15TCP的服务器程序读取客户端数据
   A:TCP的服务器程序读取客户端数据
      
      /*
       *  实现TCP客户端,连接到服务器
       *  和服务器实现数据交换
       *  实现TCP客户端程序的类 java.net.Socket
       *  
       *  构造方法:
       *      Socket(String host, int port)  传递服务器IP和端口号
       *      注意:构造方法只要运行,就会和服务器进行连接,连接失败,抛出异常
       *      
       *    OutputStream  getOutputStream() 返回套接字的输出流
       *      作用: 将数据输出,输出到服务器
       *      
       *    InputStream getInputStream() 返回套接字的输入流
       *      作用: 从服务器端读取数据
       *      
       *    客户端服务器数据交换,必须使用套接字对象Socket中的获取的IO流,自己new流,不行
       */
      public class TCPClient {
        public static void main(String[] args)throws IOException {
          //创建Socket对象,连接服务器
          Socket socket = new Socket("127.0.0.1", 8888);
          //通过客户端的套接字对象Socket方法,获取字节输出流,将数据写向服务器
          OutputStream out = socket.getOutputStream();
          out.write("服务器OK".getBytes());
          socket.close();
        }
      }
      /*
       *  实现TCP服务器程序
       *  表示服务器程序的类 java.net.ServerSocket
       *  构造方法:
       *    ServerSocket(int port) 传递端口号
       *  
       *  很重要的事情: 必须要获得客户端的套接字对象Socket
       *    Socket  accept()
       */
      public class TCPServer {
        public static void main(String[] args) throws IOException{
          ServerSocket server = new ServerSocket(8888);
          //调用服务器套接字对象中的方法accept() 获取客户端套接字对象
          Socket socket = server.accept();
          //通过客户端套接字对象,socket获取字节输入流,读取的是客户端发送来的数据
          InputStream in = socket.getInputStream();
          byte[] data = new byte[1024];
          int len = in.read(data);
          System.out.println(new String(data,0,len));
        
        }
      }


 
   
### 16TCP的服务器和客户端的数据交换
   A:TCP的服务器和客户端的数据交换
      /*
       *  实现TCP客户端,连接到服务器
       *  和服务器实现数据交换
       *  实现TCP客户端程序的类 java.net.Socket
       *  
       *  构造方法:
       *      Socket(String host, int port)  传递服务器IP和端口号
       *      注意:构造方法只要运行,就会和服务器进行连接,连接失败,抛出异常
       *      
       *    OutputStream  getOutputStream() 返回套接字的输出流
       *      作用: 将数据输出,输出到服务器
       *      
       *    InputStream getInputStream() 返回套接字的输入流
       *      作用: 从服务器端读取数据
       *      
       *    客户端服务器数据交换,必须使用套接字对象Socket中的获取的IO流,自己new流,不行
       */
      public class TCPClient {
        public static void main(String[] args)throws IOException {
          //创建Socket对象,连接服务器
          Socket socket = new Socket("127.0.0.1", 8888);
          //通过客户端的套接字对象Socket方法,获取字节输出流,将数据写向服务器
          OutputStream out = socket.getOutputStream();
          out.write("服务器OK".getBytes());
          
          //读取服务器发回的数据,使用socket套接字对象中的字节输入流
          InputStream in = socket.getInputStream();
          byte[] data = new byte[1024];
          int len = in.read(data);
          System.out.println(new String(data,0,len));
          
          socket.close();
        }
      }
      /*
       *  实现TCP服务器程序
       *  表示服务器程序的类 java.net.ServerSocket
       *  构造方法:
       *    ServerSocket(int port) 传递端口号
       *  
       *  很重要的事情: 必须要获得客户端的套接字对象Socket
       *    Socket  accept()
       */
      public class TCPServer {
        public static void main(String[] args) throws IOException{
          ServerSocket server = new ServerSocket(8888);
          //调用服务器套接字对象中的方法accept() 获取客户端套接字对象
          Socket socket = server.accept();
          //通过客户端套接字对象,socket获取字节输入流,读取的是客户端发送来的数据
          InputStream in = socket.getInputStream();
          byte[] data = new byte[1024];
          int len = in.read(data);
          System.out.println(new String(data,0,len));
          
          //服务器向客户端回数据,字节输出流,通过客户端套接字对象获取字节输出流
          OutputStream out = socket.getOutputStream();
          out.write("收到,谢谢".getBytes());
          
          socket.close();
          server.close();
        }
      }
      



### 17TCP的中的流对象
    *A:TCP的中的流对象
        参见图解TCP中的流对象.jpg  

======================================第四节课=================================================
### 18TCP图片上传案例分析
    *A:图片上传案例分析
         参见图解TCP上传图片案例.jpg  

### 19TCP上传客户端
   *A TCP上传客户端
   /*
    *  实现TCP图片上传客户端
    *  实现步骤:
    *    1. Socket套接字连接服务器
    *    2. 通过Socket获取字节输出流,写图片
    *    3. 使用自己的流对象,读取图片数据源
    *         FileInputStream
    *    4. 读取图片,使用字节输出流,将图片写到服务器
    *       采用字节数组进行缓冲
    *    5. 通过Socket套接字获取字节输入流
    *       读取服务器发回来的上传成功
    *    6. 关闭资源
    */
   public class TCPClient {
    public static void main(String[] args) throws IOException{
      Socket socket = new Socket("127.0.0.1", 8000);
      //获取字节输出流,图片写到服务器
      OutputStream out = socket.getOutputStream();
      //创建字节输入流,读取本机上的数据源图片
      FileInputStream fis = new FileInputStream("c:\\t.jpg");
      //开始读写字节数组
      int len = 0 ;
      byte[] bytes = new byte[1024];
      while((len = fis.read(bytes))!=-1){
        out.write(bytes, 0, len);
      }
      //给服务器写终止序列
      //socket.shutdownOutput();
      
      //获取字节输入流,读取服务器的上传成功
      InputStream in = socket.getInputStream();

      len = in.read(bytes);
      System.out.println(new String(bytes,0,len));
      
      fis.close();
      socket.close();
    }
   }
### 20TCP上传服务器
   A:TCP上传服务器
   /*
    *  TCP图片上传服务器
    *   1. ServerSocket套接字对象,监听端口8000
    *   2. 方法accept()获取客户端的连接对象
    *   3. 客户端连接对象获取字节输入流,读取客户端发送图片
    *   4. 创建File对象,绑定上传文件夹
    *       判断文件夹存在, 不存,在创建文件夹
    *   5. 创建字节输出流,数据目的File对象所在文件夹
    *   6. 字节流读取图片,字节流将图片写入到目的文件夹中
    *   7. 将上传成功会写客户端
    *   8. 关闭资源
    *       
    */
   public class TCPServer {
    public static void main(String[] args) throws IOException{
      ServerSocket server = new ServerSocket(8000);
      Socket socket = server.accept();
      //通过客户端连接对象,获取字节输入流,读取客户端图片
      InputStream in = socket.getInputStream();
      //将目的文件夹封装到File对象
      File upload = new File("d:\\upload");
      if(!upload.exists())
        upload.mkdirs();
       
      //创建字节输出流,将图片写入到目的文件夹中                         
      FileOutputStream fos = new FileOutputStream(upload+"t.jpg");
      //读写字节数组
      byte[] bytes = new byte[1024];
      int len = 0 ;
      while((len = in.read(bytes))!=-1){
        fos.write(bytes, 0, len);
      }
      //通过客户端连接对象获取字节输出流
      //上传成功写回客户端
      socket.getOutputStream().write("上传成功".getBytes());
      
      fos.close();
      socket.close();
      server.close();
    }
   }
### 21TCP图片上传问题解决
/*
 *  实现TCP图片上传客户端
 *  实现步骤:
 *    1. Socket套接字连接服务器
 *    2. 通过Socket获取字节输出流,写图片
 *    3. 使用自己的流对象,读取图片数据源
 *         FileInputStream
 *    4. 读取图片,使用字节输出流,将图片写到服务器
 *       采用字节数组进行缓冲
 *    5. 通过Socket套接字获取字节输入流
 *       读取服务器发回来的上传成功
 *    6. 关闭资源
 */
public class TCPClient {
  public static void main(String[] args) throws IOException{
    Socket socket = new Socket("127.0.0.1", 8000);
    //获取字节输出流,图片写到服务器
    OutputStream out = socket.getOutputStream();
    //创建字节输入流,读取本机上的数据源图片
    FileInputStream fis = new FileInputStream("c:\\t.jpg");
    //开始读写字节数组
    int len = 0 ;
    byte[] bytes = new byte[1024];
    while((len = fis.read(bytes))!=-1){
      out.write(bytes, 0, len);
    }
    //给服务器写终止序列
    socket.shutdownOutput();//想服务端写入一个结束标志
    
    //获取字节输入流,读取服务器的上传成功
    InputStream in = socket.getInputStream();

    len = in.read(bytes);
    System.out.println(new String(bytes,0,len));
    
    fis.close();
    socket.close();
  }
}

### TCP上传文件名 
  *A:TCP上传文件名
   /*
    *  TCP图片上传服务器
    *   1. ServerSocket套接字对象,监听端口8000
    *   2. 方法accept()获取客户端的连接对象
    *   3. 客户端连接对象获取字节输入流,读取客户端发送图片
    *   4. 创建File对象,绑定上传文件夹
    *       判断文件夹存在, 不存,在创建文件夹
    *   5. 创建字节输出流,数据目的File对象所在文件夹
    *   6. 字节流读取图片,字节流将图片写入到目的文件夹中
    *   7. 将上传成功会写客户端
    *   8. 关闭资源
    *       
    */
   public class TCPServer {
    public static void main(String[] args) throws IOException{
      ServerSocket server = new ServerSocket(8000);
      Socket socket = server.accept();
      //通过客户端连接对象,获取字节输入流,读取客户端图片
      InputStream in = socket.getInputStream();
      //将目的文件夹封装到File对象
      File upload = new File("d:\\upload");
      if(!upload.exists())
        upload.mkdirs();
      
      //防止文件同名被覆盖,从新定义文件名字
      //规则:  域名+毫秒值+6位随机数
      String filename="itcast"+System.currentTimeMillis()+new Random().nextInt(999999)+".jpg";
      //创建字节输出流,将图片写入到目的文件夹中                         
      FileOutputStream fos = new FileOutputStream(upload+File.separator+filename);
      //读写字节数组
      byte[] bytes = new byte[1024];
      int len = 0 ;
      while((len = in.read(bytes))!=-1){
        fos.write(bytes, 0, len);
      }
      //通过客户端连接对象获取字节输出流
      //上传成功写回客户端
      socket.getOutputStream().write("上传成功".getBytes());
      
      fos.close();
      socket.close();
      server.close();
    }
   }

### 多线程上传案例
*A:多线程上传案例
  public class TCPThreadServer {
    public static void main(String[] args) throws IOException {
      ServerSocket server = new ServerSocket(8000);
      while (true) {
        // 获取到一个客户端,必须开启新线程,为这个客户端服务
        Socket socket = server.accept(); 
        new Thread(new Upload(socket)).start();
      }
    }
  }

  public class Upload implements Runnable {

    private Socket socket;

    public Upload(Socket socket) {
      this.socket = socket;
    }

    public void run() {
      try {
        // 通过客户端连接对象,获取字节输入流,读取客户端图片
        InputStream in = socket.getInputStream();
        // 将目的文件夹封装到File对象
        File upload = new File("d:\\upload");
        if (!upload.exists())
          upload.mkdirs();

        // 防止文件同名被覆盖,从新定义文件名字
        // 规则: 域名+毫秒值+6位随机数
        String filename = "itcast" + System.currentTimeMillis() + new Random().nextInt(999999) + ".jpg";
        // 创建字节输出流,将图片写入到目的文件夹中
        FileOutputStream fos = new FileOutputStream(upload + File.separator + filename);
        // 读写字节数组
        byte[] bytes = new byte[1024];
        int len = 0;
        while ((len = in.read(bytes)) != -1) {
          fos.write(bytes, 0, len);
        }
        // 通过客户端连接对象获取字节输出流
        // 上传成功写回客户端
        socket.getOutputStream().write("上传成功".getBytes());

        fos.close();
        socket.close();
      } catch (Exception ex) {

      }
    }

  }
今日内容介绍
1、JDBC
2、DBUtils

### 01JDBC概念和数据库驱动程序
	* A: JDBC概念和数据库驱动程序
		* a: JDBC概述		
			* JDBC（Java Data Base Connectivity,java数据库连接）是一种用于执行SQL语句的Java API，
				可以为多种关系数据库提供统一访问，它由一组用Java语言编写的类和接口组成。是Java访问数据库的标准规范
			* JDBC提供了一种基准,据此可以构建更高级的工具和接口，使数据库开发人员能够编写数据库应用程序。
			* JDBC需要连接驱动，驱动是两个设备要进行通信，满足一定通信数据格式，数据格式由设备提供商规定，
				设备提供商为设备提供驱动软件，通过软件可以与该设备进行通信。
			* 我们使用的是mysql的驱动mysql-connector-java-5.1.39-bin.jar
		* b: 总结
			* JDBC是java提供给开发人员的一套操作数据库的接口
			* 数据库驱动就是实现该接口的实现类
			



### 02JDBC原理
	* A: JDBC原理
		* a: 描述
			* Java提供访问数据库规范称为JDBC，而生产厂商提供规范的实现类称为驱动
			* DBC是接口，驱动是接口的实现，没有驱动将无法完成数据库连接，从而不能操作数据库！
				每个数据库厂商都需要提供自己的驱动，用来连接自己公司的数据库，也就是说驱动一般都由数据库生成厂商提供。
			* 图解见day29_source/JDBC实现原理.JPG
					
### 03准备数据
	* A: 准备数据
		* a: 创建数据库和表结构
			#创建数据库
			create database mybase;
			#使用数据库
			use mybase;
			### 创建分类表
			create table sort(
			  sid int PRIMARY KEY AUTO_INCREMENT,
			  sname varchar(100),
			  sprice DOUBLE,
			  sdesc VARCHAR(500)
			);
			
		* b: 向表中插入数据
			#初始化数据
			insert into sort(sname,sprice,sdesc) values('家电',2000, '优惠的促销');
			insert into sort(sname,sprice,sdesc) values('家具',8900, '家具价格上调,原材料涨价');
			insert into sort(sname,sprice,sdesc) values('儿童玩具',290, '赚家长的钱');
			insert into sort(sname,sprice,sdesc) values('生鲜',500.99, '生鲜商品');
			insert into sort(sname,sprice,sdesc) values('服装',24000, '换季销售');
			insert into sort(sname,sprice,sdesc) values('洗涤',50, '洗发水促销');			
			
### 04JDBC的开发步骤
	* A: JDBC的开发步骤
		* a: 步骤介绍
			1.注册驱动
				告知JVM使用的是哪一个数据库的驱动
			2.获得连接
				使用JDBC中的类,完成对MySQL数据库的连接
			3.获得语句执行平台
				通过连接对象获取对SQL语句的执行者对象
			4.执行sql语句
				使用执行者对象,向数据库执行SQL语句
				获取到数据库的执行后的结果
			5.处理结果
			6.释放资源  一堆close()
						
### 05导入mysql数据库驱动程序jar包
	* A: 导入mysql数据库驱动程序jar包
		* a: 步骤
			* 创建lib目录，用于存放当前项目需要的所有jar包
			* 选择jar包，右键执行build path / Add to Build Path

 
### 06注册数据库驱动程序
	* A: 注册数据库驱动程序
		* a: 案例代码
			public class JDBCDemo {
				public static void main(String[] args)throws ClassNotFoundException,SQLException{
					//1.注册驱动 反射技术,将驱动类加入到内容
					// 使用java.sql.DriverManager类静态方法 registerDriver(Driver driver)
					// Diver是一个接口,参数传递,MySQL驱动程序中的实现类
					//DriverManager.registerDriver(new Driver());
					//驱动类源代码,注册2次驱动程序
					Class.forName("com.mysql.jdbc.Driver");					
				}
			}

			
		
### 07获取数据库的连接对象
	* A：获取数据库的连接对象
		* a: 案例代码
			public class JDBCDemo {
				public static void main(String[] args)throws ClassNotFoundException,SQLException{
					//1.注册驱动 反射技术,将驱动类加入到内容
					// 使用java.sql.DriverManager类静态方法 registerDriver(Driver driver)
					// Diver是一个接口,参数传递,MySQL驱动程序中的实现类
					//DriverManager.registerDriver(new Driver());
					//驱动类源代码,注册2次驱动程序
					Class.forName("com.mysql.jdbc.Driver");
					
					//2.获得数据库连接  DriverManager类中静态方法
					//static Connection getConnection(String url, String user, String password)  
					//返回值是Connection接口的实现类,在mysql驱动程序
					//url: 数据库地址  jdbc:mysql://连接主机IP:端口号//数据库名字
					String url = "jdbc:mysql://localhost:3296/mybase";
					//用户名和密码用自己的
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);
					System.out.println(con);					
				}
			}

				
### 08获取SQL语句的执行对象对象
	* A: 获取SQL语句的执行对象对象
		* a: 案例代码
			public class JDBCDemo {
				public static void main(String[] args)throws ClassNotFoundException,SQLException{
					//1.注册驱动 反射技术,将驱动类加入到内容
					// 使用java.sql.DriverManager类静态方法 registerDriver(Driver driver)
					// Diver是一个接口,参数传递,MySQL驱动程序中的实现类
					//DriverManager.registerDriver(new Driver());
					//驱动类源代码,注册2次驱动程序
					Class.forName("com.mysql.jdbc.Driver");
					
					//2.获得数据库连接  DriverManager类中静态方法
					//static Connection getConnection(String url, String user, String password)  
					//返回值是Connection接口的实现类,在mysql驱动程序
					//url: 数据库地址  jdbc:mysql://连接主机IP:端口号//数据库名字
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);
					
					//3.获得语句执行平台, 通过数据库连接对象,获取到SQL语句的执行者对象
					// con对象调用方法   Statement createStatement() 获取Statement对象,将SQL语句发送到数据库
					// 返回值是 Statement接口的实现类对象,,在mysql驱动程序
					Statement stat = con.createStatement();
					System.out.println(stat);
				}
			}

### 09执行insert语句获取结果集
	* A: 执行insert语句获取结果集
		* a: 案例代码
			public class JDBCDemo {
				public static void main(String[] args)throws ClassNotFoundException,SQLException{
					//1.注册驱动 反射技术,将驱动类加入到内容
					// 使用java.sql.DriverManager类静态方法 registerDriver(Driver driver)
					// Diver是一个接口,参数传递,MySQL驱动程序中的实现类
					//DriverManager.registerDriver(new Driver());
					//驱动类源代码,注册2次驱动程序
					Class.forName("com.mysql.jdbc.Driver");
					
					//2.获得数据库连接  DriverManager类中静态方法
					//static Connection getConnection(String url, String user, String password)  
					//返回值是Connection接口的实现类,在mysql驱动程序
					//url: 数据库地址  jdbc:mysql://连接主机IP:端口号//数据库名字
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);
					
					//3.获得语句执行平台, 通过数据库连接对象,获取到SQL语句的执行者对象
					// con对象调用方法   Statement createStatement() 获取Statement对象,将SQL语句发送到数据库
					// 返回值是 Statement接口的实现类对象,,在mysql驱动程序
					Statement stat = con.createStatement();
					//	4.执行sql语句
					// 通过执行者对象调用方法执行SQL语句,获取结果
					// int executeUpdate(String sql)  执行数据库中的SQL语句, insert delete update
					// 返回值int,操作成功数据表多少行
					int row = stat.executeUpdate
							("INSERT INTO sort(sname,sprice,sdesc) VALUES('汽车用品',50000,'疯狂涨价')");
					System.out.println(row);
					
					//6.释放资源  一堆close()
					stat.close();
					con.close();
				}
			}
			


### 10执行select语句获取结果集
	* A: 执行select语句获取结果集
		* a: 案例代码
			public class JDBCDemo1 {
				public static void main(String[] args) throws Exception{
					//1. 注册驱动
					Class.forName("com.mysql.jdbc.Driver");
					//2. 获取连接对象
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);
					//3 .获取执行SQL 语句对象
					Statement stat = con.createStatement();
					// 拼写查询的SQL
					String sql = "SELECT * FROM sort";
					//4. 调用执行者对象方法,执行SQL语句获取结果集
					// ResultSet executeQuery(String sql)  执行SQL语句中的select查询
					// 返回值ResultSet接口的实现类对象,实现类在mysql驱动中
					ResultSet rs = stat.executeQuery(sql);
					//5 .处理结果集
					// ResultSet接口方法 boolean next() 返回true,有结果集,返回false没有结果集
					while(rs.next()){
						//获取每列数据,使用是ResultSet接口的方法 getXX方法参数中,建议写String列名
						System.out.println(rs.getInt("sid")+"   "+rs.getString("sname")+
								"   "+rs.getDouble("sprice")+"   "+rs.getString("sdesc"));
					}
					
					rs.close();
					stat.close();
					con.close();
				}
			}


				
### 11SQL注入攻击
	* A: SQL注入攻击
		* a: 注入问题
			* 假设有登录案例SQL语句如下:
			* SELECT * FROM 用户表 WHERE NAME = 用户输入的用户名 AND PASSWORD = 用户输的密码;
			* 此时，当用户输入正确的账号与密码后，查询到了信息则让用户登录。
				但是当用户输入的账号为XXX 密码为：XXX’  OR ‘a’=’a时，则真正执行的代码变为：
				* SELECT * FROM 用户表 WHERE NAME = ‘XXX’ AND PASSWORD =’ XXX’  OR ’a’=’a’;
			* 此时，上述查询语句时永远可以查询出结果的。那么用户就直接登录成功了，显然我们不希望看到这样的结果，这便是SQL注入问题。
		* b: 案例演示
			CREATE TABLE users(
				 id INT PRIMARY KEY AUTO_INCREMENT,
				 username VARCHAR(100),
				 PASSWORD VARCHAR(100)
			);

			INSERT INTO users (username,PASSWORD) VALUES ('a','1'),('b','2');

			SELECT * FROM users;

			-- 登录查询
			SELECT * FROM users WHERE username='dsfsdfd' AND PASSWORD='wrethiyu'1 
			OR 1=1

			SELECT * FROM users WHERE username='a' AND PASSWORD='1'OR'1=1'
			键盘录入：
			1
			1'OR' 1=1
			

			
### 12SQL注入攻击用户登录案例
	* A: SQL注入攻击用户登录案例
		* a: 案例代码
			public class JDBCDemo2 {
				public static void main(String[] args)throws Exception {
					Class.forName("com.mysql.jdbc.Driver");
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username = "root";
					String password = "123";
					Connection con = DriverManager.getConnection(url, username, password);
					Statement stat = con.createStatement();
					
					Scanner sc = new Scanner(System.in);
					String user = sc.nextLine();
					String pass = sc.nextLine();
					
					//执行SQL语句,数据表,查询用户名和密码,如果存在,登录成功,不存在登录失败
			//		String sql = "SELECT * FROM users WHERE username='dsfsdfd' AND PASSWORD='wrethiyu' OR 1=1";
					String sql = "SELECT * FROM users WHERE username='"+user+"' AND PASSWORD='"+pass+"'";
					System.out.println(sql);
					ResultSet rs = stat.executeQuery(sql);
					while(rs.next()){
						System.out.println(rs.getString("username")+"   "+rs.getString("password"));
					}
					
					rs.close();
					stat.close();
					con.close();
				}
			}

		
### 13PrepareStatement接口预编译SQL语句
	* A: PrepareStatement接口预编译SQL语句
		* a: 预处理对象
			* 使用PreparedStatement预处理对象时，建议每条sql语句所有的实际参数，都使用逗号分隔。
			* String sql = "insert into sort(sid,sname) values(?,?)";;
			* PreparedStatement预处理对象代码：
			* PreparedStatement psmt = conn.prepareStatement(sql)
			
		* b: 执行SQL语句的方法介绍
			* int executeUpdate(); --执行insert update delete语句.
			* ResultSet executeQuery(); --执行select语句.
			* boolean execute(); --执行select返回true 执行其他的语句返回false.
		* c: 设置实际参数
			* void setXxx(int index, Xxx xx) 将指定参数设置为给定Java的xx值。在将此值发送到数据库时，驱动程序将它转换成一个 SQL Xxx类型值。
			* 例如：
				* setString(2, "家用电器") 把SQL语句中第2个位置的占位符？ 替换成实际参数 "家用电器"
		* d: 案例代码
			/*
			 *  Java程序实现用户登录,用户名和密码,数据库检查
			 *  防止注入攻击
			 *  Statement接口实现类,作用执行SQL语句,返回结果集
			 *  有一个子接口PreparedStatement  (SQL预编译存储,多次高效的执行SQL) 
			 *  PreparedStatement的实现类数据库的驱动中,如何获取接口的实现类
			 *  
			 *  是Connection数据库连接对象的方法
			 *  PreparedStatement prepareStatement(String sql) 
					  
			 */
			public class JDBCDemo3 {
				public static void main(String[] args)throws Exception {
					Class.forName("com.mysql.jdbc.Driver");
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username = "root";
					String password = "123";
					Connection con = DriverManager.getConnection(url, username, password);
					Scanner sc = new Scanner(System.in);
					String user = sc.nextLine();
					String pass = sc.nextLine();
					
					//执行SQL语句,数据表,查询用户名和密码,如果存在,登录成功,不存在登录失败
					String sql = "SELECT * FROM users WHERE username=? AND PASSWORD=?";
					//调用Connection接口的方法prepareStatement,获取PrepareStatement接口的实现类
					//方法中参数,SQL语句中的参数全部采用问号占位符
					PreparedStatement pst =  con.prepareStatement(sql);
					System.out.println(pst);
					//调用pst对象set方法,设置问号占位符上的参数
					pst.setObject(1, user);
					pst.setObject(2, pass);
					
					//调用方法,执行SQL,获取结果集
					ResultSet rs = pst.executeQuery();
					while(rs.next()){
						System.out.println(rs.getString("username")+"   "+rs.getString("password"));
					}
					
					rs.close();
					pst.close();
					con.close();
				}
			}




			
### 14PrepareStatement接口预编译SQL语句执行修改
	* A: PrepareStatement接口预编译SQL语句执行修改
		* 案例代码
			/*
			 *  使用PrepareStatement接口,实现数据表的更新操作
			 */
			public class JDBCDemo {
				public static void main(String[] args) throws Exception{
					Class.forName("com.mysql.jdbc.Driver");
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);	
					
					//拼写修改的SQL语句,参数采用?占位
					String sql = "UPDATE sort SET sname=?,sprice=? WHERE sid=?";
					//调用数据库连接对象con的方法prepareStatement获取SQL语句的预编译对象
					PreparedStatement pst = con.prepareStatement(sql);
					//调用pst的方法setXXX设置?占位
					pst.setObject(1, "汽车美容");
					pst.setObject(2, 49988);
					pst.setObject(3, 7);
					//调用pst方法执行SQL语句
					pst.executeUpdate();
					
					pst.close();
					con.close();
				}
			}

			
### 15PrepareStatement接口预编译SQL语句执行查询
	* A: PrepareStatement接口预编译SQL语句执行查询
		* a: 案例代码
			/*
			 *  PrepareStatement接口实现数据表的查询操作
			 */
			public class JDBCDemo1 {
				public static void main(String[] args) throws Exception{
					Class.forName("com.mysql.jdbc.Driver");
					String url = "jdbc:mysql://localhost:3296/mybase";
					String username="root";
					String password="123";
					Connection con = DriverManager.getConnection(url, username, password);	
					
					String sql = "SELECT * FROM sort";
					
					PreparedStatement pst = con.prepareStatement(sql);
					
					//调用pst对象的方法,执行查询语句,Select
					ResultSet rs=pst.executeQuery();
					while(rs.next()){
						System.out.println(rs.getString("sid")+"  "+rs.getString("sname")+"  "+rs.getString("sprice")+"  "+rs.getString("sdesc"));
					}
					rs.close();
					pst.close();
					con.close();
				}
			}

			
### 16JDBC的工具类和测试
	* A: JDBC的工具类和测试
		* a: 案例代码
			//JDBCUtils工具类代码
			public class JDBCUtils {
				private JDBCUtils(){}
				private static Connection con ;
				
				static{
					try{
						Class.forName("com.mysql.jdbc.Driver");
						String url = "jdbc:mysql://localhost:3296/mybase";
						String username="root";
						String password="123";
						con = DriverManager.getConnection(url, username, password);
					}catch(Exception ex){
						throw new RuntimeException(ex+"数据库连接失败");
					}
				}
				
				/*
				 * 定义静态方法,返回数据库的连接对象
				 */
				public static Connection getConnection(){
					return con;
				}
				
				
				public static void close(Connection con,Statement stat){
					 
					 if(stat!=null){
						 try{
							 stat.close();
						 }catch(SQLException ex){}
					 }
					 
					 if(con!=null){
						 try{
							 con.close();
						 }catch(SQLException ex){}
					 }
					 
				}
				
				
				public static void close(Connection con,Statement stat , ResultSet rs){
					 if(rs!=null){
						 try{
							 rs.close();
						 }catch(SQLException ex){}
					 }
					 
					 if(stat!=null){
						 try{
							 stat.close();
						 }catch(SQLException ex){}
					 }
					 
					 if(con!=null){
						 try{
							 con.close();
						 }catch(SQLException ex){}
					 }
					 
				}
			}
		//测试JDBCUtils工具类的代码
		public class TestJDBCUtils {
			public static void main(String[] args)throws Exception {
				Connection con = JDBCUtils.getConnection();
				PreparedStatement pst = con.prepareStatement("SELECT sname FROM sort");
				ResultSet rs = pst.executeQuery();
				while(rs.next()){
					System.out.println(rs.getString("sname"));
				}
				JDBCUtils.close(con, pst, rs);
			}
		}
		
### 17数据表数据存储对象
	* A: 数据表数据存储对象
		* a: 准备工作
			* 导入jar包
			* 拷贝day32定义的工具类JDBCUtils
			
		* b: 案例代码
			//定义实体类Sort
			public class Sort {
				private int sid;
				private String sname;
				private double sprice;
				private String sdesc;
				public Sort(int sid, String sname, double sprice, String sdesc) {
					this.sid = sid;
					this.sname = sname;
					this.sprice = sprice;
					this.sdesc = sdesc;
				}
				public Sort(){}
				public int getSid() {
					return sid;
				}
				public void setSid(int sid) {
					this.sid = sid;
				}
				public String getSname() {
					return sname;
				}
				public void setSname(String sname) {
					this.sname = sname;
				}
				public double getSprice() {
					return sprice;
				}
				public void setSprice(double sprice) {
					this.sprice = sprice;
				}
				public String getSdesc() {
					return sdesc;
				}
				public void setSdesc(String sdesc) {
					this.sdesc = sdesc;
				}
				@Override
				public String toString() {
					return "Sort [sid=" + sid + ", sname=" + sname + ", sprice=" + sprice + ", sdesc=" + sdesc + "]";
				}				
			}
			
			/*
			 *  JDBC读取数据表sort,每行数据封装到Sort类的对象中
			 *  很多个Sort类对象,存储到List集合中
			 */
			public class JDBCDemo {
				public static void main(String[] args) throws Exception{
					//使用JDBC工具类,直接获取数据库连接对象
					Connection con = JDBCUtils.getConnection();
					//连接获取数据库SQL语句执行者对象
					PreparedStatement pst = con.prepareStatement("SELECT * FROM sort");
					//调用查询方法,获取结果集
					ResultSet rs = pst.executeQuery();
					//创建集合对象
					List<Sort> list = new ArrayList<Sort>();
					while(rs.next()){
						//获取到每个列数据,封装到Sort对象中
						Sort s = new Sort(rs.getInt("sid"),rs.getString("sname"),rs.getDouble("sprice"),rs.getString("sdesc"));
						//封装的Sort对象,存储到集合中
						list.add(s);
					}
					JDBCUtils.close(con, pst, rs);
					//遍历List集合
					for(Sort s : list){
						System.out.println(s);
					}
				}
			}

			


		
	
### 18properties配置文件
	* A: properties配置文件		
		* a: 相关介绍
			* 开发中获得连接的4个参数（驱动、URL、用户名、密码）通常都存在配置文件中，方便后期维护，程序如果需要更换数据库，
				只需要修改配置文件即可。
			* 通常情况下，我们习惯使用properties文件，此文件我们将做如下要求：
				1.	文件位置：任意，建议src下
				2.	文件名称：任意，扩展名为properties
				3.	文件内容：一行一组数据，格式是“key=value”.
					a)	key命名自定义，如果是多个单词，习惯使用点分隔。例如：jdbc.driver
					b)	value值不支持中文，如果需要使用非英文字符，将进行unicode转换。

### 19properties文件的创建和编写
	* A: properties文件的创建和编写
		* a: properties文件的创建
			* src路径下建立database.properties(其实就是一个文本文件)
		* b: properties文件的编写(内容如下)
			driverClass=com.mysql.jdbc.Driver
			url=jdbc:mysql://localhost:3296/mybase
			username=root
			password=123		

### 20加载配置文件
	* A: 加载配置文件
		* a: 案例代码		
			/*
			 *  加载properties配置文件
			 *  IO读取文件,键值对存储到集合
			 *  从集合中以键值对方式获取数据库的连接信息,完成数据库的连接
			 */
			public class PropertiesDemo {
				public static void main(String[] args) throws Exception{
					FileInputStream fis = new FileInputStream("database.properties");
					System.out.println(fis);
					//使用类的加载器
					InputStream in = PropertiesDemo.class.getClassLoader().getResourceAsStream("database.properties");
					System.out.println(in);
					Properties pro = new Properties();
					pro.load(in);
					System.out.println(in);					
				}
			}




### 21通过配置文件连接数据库
	* A: 通过配置文件连接数据库
		* a: 案例代码
			/*
			 *  加载properties配置文件
			 *  IO读取文件,键值对存储到集合
			 *  从集合中以键值对方式获取数据库的连接信息,完成数据库的连接
			 */
			public class PropertiesDemo {
				public static void main(String[] args) throws Exception{
					FileInputStream fis = new FileInputStream("database.properties");
					System.out.println(fis);
					//使用类的加载器
					InputStream in = PropertiesDemo.class.getClassLoader().getResourceAsStream("database.properties");
					System.out.println(in);
					Properties pro = new Properties();
					pro.load(in);
					//获取集合中的键值对
					String driverClass=pro.getProperty("driverClass");
					String url = pro.getProperty("url");
					String username = pro.getProperty("username");
					String password = pro.getProperty("password");
					Class.forName(driverClass);
					Connection con = DriverManager.getConnection(url, username, password);
					System.out.println(con);
					
				}
			}

					
### 22读取配置文件的工具类
	* A: 读取配置文件的工具类
		* a: 案例代码
			/*
			 *  编写数据库连接的工具类,JDBC工具类
			 *  获取连接对象采用读取配置文件方式
			 *  读取文件获取连接,执行一次,static{}
			 */
			public class JDBCUtilsConfig {
				private static Connection con ;
				private static String driverClass;
				private static String url;
				private static String username;
				private static String password;
				
				static{
					try{
						readConfig();
						Class.forName(driverClass);
						con = DriverManager.getConnection(url, username, password);
					}catch(Exception ex){
						throw new RuntimeException("数据库连接失败");
					}
				}
				
				private static void readConfig()throws Exception{
					InputStream in = JDBCUtilsConfig.class.getClassLoader().getResourceAsStream("database.properties");
					 Properties pro = new Properties();
					 pro.load(in);
					 driverClass=pro.getProperty("driverClass");
					 url = pro.getProperty("url");
					 username = pro.getProperty("username");
					 password = pro.getProperty("password");
				}
				
				
				public static Connection getConnection(){
					return con;
				}
				
			}			
			
### 23测试工具类
	* A: 测试工具类
		* a: 案例代码
			public class TestJDBCUtils {
				public static void main(String[] args) {
					Connection con = JDBCUtilsConfig.getConnection();
					System.out.println(con);
				}
			}

### 24总结
	* 把今天的知识点总结一遍。
			
今日内容介绍
1、DBUtils
2、连接池						
### 01DButils工具类的介绍个三个核心类
	* A: DButils工具类的介绍个三个核心类
		* a: 概述
			* DBUtils是java编程中的数据库操作实用工具，小巧简单实用。
			* DBUtils封装了对JDBC的操作，简化了JDBC操作，可以少写代码。
			* DBUtils就是JDBC的简化开发工具包。需要项目导入commons-dbutils-1.6.jar才能够正常使用DBUtils工具。
		* b: Dbutils三个核心功能介绍
			* QueryRunner中提供对sql语句操作的API.
				* update(Connection conn, String sql, Object... params) ，用来完成表数据的增加、删除、更新操作
				* query(Connection conn, String sql, ResultSetHandler<T> rsh, Object... params) ，用来完成表数据的查询操作
			* ResultSetHandler接口，用于定义select操作后，怎样封装结果集.
			* DbUtils类，它就是一个工具类,定义了关闭资源与事务处理的方法


 
### 02事务的简单介绍(此知识点简单了解，难度较大，就业班会详细 讲解)
	* A: 事务的简单介绍
		* a: 见day32/day32_source/事务.jgp
		
### 03QueryRunner类的update方法介绍
	* A：QueryRunner类的update方法介绍
		* a: 方法介绍
			* update(Connection conn, String sql, Object... params) ，用来完成表数据的增加、删除、更新操作
			*  使用QueryRunner类,实现对数据表的insert delete update
			*  调用QueryRunner类的方法 update (Connection con,String sql,Object...param)
				*  Object...param 可变参数,Object类型,SQL语句会出现?占位符
				*  数据库连接对象,自定义的工具类传递
 
				
### 04QueryRunner类实现insert添加数据
	* A: QueryRunner类实现insert添加数据
		* a: 案例代码
			public class QueryRunnerDemo {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args)throws SQLException {
					insert();			
				}				
				/*
				 * 定义方法,使用QueryRunner类的方法update向数据表中,添加数据
				 */
				public static void insert()throws SQLException{
					//创建QueryRunner类对象
					QueryRunner qr = new QueryRunner();
					String sql = "INSERT INTO sort (sname,sprice,sdesc)VALUES(?,?,?)";
					//将三个?占位符的实际参数,写在数组中
					Object[] params = {"体育用品",289.32,"购买体育用品"};
					//调用QueryRunner类的方法update执行SQL语句
					int row = qr.update(con, sql, params);
					System.out.println(row);
					DbUtils.closeQuietly(con);
				}
			}


### 05QueryRunner类实现update修改数据
	* A: QueryRunner类实现update修改数据
		* a: 案例代码
			public class QueryRunnerDemo {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args)throws SQLException {
					update();
				}				
				/*
				 *  定义方法,使用QueryRunner类的方法update将数据表的数据修改
				 */
				public static void update()throws SQLException{
					//创建QueryRunner类对象
					QueryRunner qr = new QueryRunner();	
					//写修改数据的SQL语句
					String sql = "UPDATE sort SET sname=?,sprice=?,sdesc=? WHERE sid=?";
					//定义Object数组,存储?中的参数
					Object[] params = {"花卉",100.88,"情人节玫瑰花",4};
					//调用QueryRunner方法update
					int row = qr.update(con, sql, params);
					System.out.println(row);
					DbUtils.closeQuietly(con);
				}				
			}

			


### 06QueryRunner类实现delete删除数据
	* A: QueryRunner类实现delete删除数据
		* a: 案例代码
			public class QueryRunnerDemo {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args)throws SQLException {
					delete();
				}
				/*
				 *  定义方法,使用QueryRunner类的方法delete将数据表的数据删除
				 */
				public static void delete()throws SQLException{
					//创建QueryRunner类对象
					QueryRunner qr = new QueryRunner();	
					//写删除的SQL语句
					String sql = "DELETE FROM sort WHERE sid=?";
					//调用QueryRunner方法update
					int row = qr.update(con, sql, 8);
					System.out.println(row);
					/*
					 *  判断insert,update,delete执行是否成功
					 *  对返回值row判断
					 *  if(row>0) 执行成功
					 */
					DbUtils.closeQuietly(con);
				}				
			}
				
### 07JavaBean类
	* A: JavaBean类
		* a: 概念
			* JavaBean就是一个类，在开发中常用封装数据。具有如下特性
				1.	需要实现接口：java.io.Serializable ，通常实现接口这步骤省略了，不会影响程序。
				2.	提供私有字段：private 类型 字段名;
				3.	提供getter/setter方法：
				4.	提供无参构造
			
### 08DBUtils工具类结果集处理的方式
	* A: DBUtils工具类结果集处理的方式
		* a: QueryRunner实现查询操作
			*	query(Connection conn, String sql, ResultSetHandler<T> rsh, Object... params) ，用来完成表数据的查询操作
		* b: ResultSetHandler结果集处理类
			* ArrayHandler	将结果集中的第一条记录封装到一个Object[]数组中，数组中的每一个元素就是这条记录中的每一个字段的值
			* ArrayListHandler	将结果集中的每一条记录都封装到一个Object[]数组中，将这些数组在封装到List集合中。
			* BeanHandler	将结果集中第一条记录封装到一个指定的javaBean中。
			* BeanListHandler	将结果集中每一条记录封装到指定的javaBean中，将这些javaBean在封装到List集合中
			* ColumnListHandler	将结果集中指定的列的字段值，封装到一个List集合中
			* ScalarHandler	它是用于单数据。例如select count(*) from 表操作。
			* MapHandler	将结果集第一行封装到Map集合中,Key 列名, Value 该列数据
			* MapListHandler	将结果集第一行封装到Map集合中,Key 列名, Value 该列数据,Map集合存储到List集合
			
### 09QueryRunner类的方法query
	* A: QueryRunner类的方法query
		* a: QueryRunner数据查询操作
			* 调用QueryRunner类方法query(Connection con,String sql,ResultSetHandler r, Object..params)
			*  ResultSetHandler r 结果集的处理方式,传递ResultSetHandler接口实现类
			*  Object..params SQL语句中的?占位符
			*  注意: query方法返回值,返回的是T 泛型, 具体返回值类型,跟随结果集处理方式变化
		* b: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
			}
					
### 10结果集处理ArrayHandler
	* A: 结果集处理ArrayHandler
		* 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					arrayHandler();
				}	
				/*
				 *  结果集第一种处理方法, ArrayHandler
				 *  将结果集的第一行存储到对象数组中  Object[]
				 */
				public static void arrayHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT * FROM sort";
					//调用方法query执行查询,传递连接对象,SQL语句,结果集处理方式的实现类
					//返回对象数组
					Object[] result = qr.query(con, sql, new ArrayHandler());
					for(Object obj : result){
						System.out.print(obj);
					}
				}	
			}
			
### 11结果集处理ArrayListHandler
	* A: 结果集处理ArrayListHandler
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					arrayListHandler();
				}
				/*
				 *  结果集第二种处理方法,ArrayListHandler
				 *  将结果集的每一行,封装到对象数组中, 出现很多对象数组
				 *  对象数组存储到List集合
				 */
				public static void arrayListHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT * FROM sort";		
					//调用query方法,结果集处理的参数上,传递实现类ArrayListHandler
					//方法返回值 每行是一个对象数组,存储到List
					List<Object[]> result=  qr.query(con, sql, new ArrayListHandler());
					
					//集合的遍历
					for( Object[] objs  : result){
						//遍历对象数组
						for(Object obj : objs){
							System.out.print(obj+"  ");
						}
						System.out.println();
					}
				}
			}


			
### 12结果集处理BeanHandler
	* A: 结果集处理BeanHandler
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					beanHandler();
				}
				/*
				 *  结果集第三种处理方法,BeanHandler
				 *  将结果集的第一行数据,封装成JavaBean对象
				 *  注意: 被封装成数据到JavaBean对象, Sort类必须有空参数构造
				 */
				public static void beanHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT * FROM sort ";
					//调用方法,传递结果集实现类BeanHandler
					//BeanHandler(Class<T> type) 
					Sort s = qr.query(con, sql, new BeanHandler<Sort>(Sort.class));
					System.out.println(s);
				}
			}


### 13结果集处理BeanListHandler
	* A: 结果集处理BeanListHandler
		* a: 案例代码
		public class QueryRunnerDemo1 {
			private static Connection con = JDBCUtilsConfig.getConnection();
			public static void main(String[] args) throws SQLException{
				beanListHander();
			}
			/*
			 *  结果集第四种处理方法, BeanListHandler
			 *  结果集每一行数据,封装JavaBean对象
			 *  多个JavaBean对象,存储到List集合
			 */
			public static void beanListHander()throws SQLException{
				QueryRunner qr = new QueryRunner();
				String sql = "SELECT * FROM sort ";
				//调用方法query,传递结果集处理实现类BeanListHandler
				List<Sort> list = qr.query(con, sql, new BeanListHandler<Sort>(Sort.class));
				for(Sort s : list){
					System.out.println(s);
				}
			}
		}

		
### 14结果集处理ColumnListHandler
	* A: 结果集处理ColumnListHandler
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					columnListHandler();
				}	
				/*
				 *  结果集第五种处理方法,ColumnListHandler
				 *  结果集,指定列的数据,存储到List集合
				 *  List<Object> 每个列数据类型不同
				 */
				public static void columnListHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT * FROM sort ";		
					//调用方法 query,传递结果集实现类ColumnListHandler
					//实现类构造方法中,使用字符串的列名
					List<Object> list = qr.query(con, sql, new ColumnListHandler<Object>("sname"));
					for(Object obj : list){
						System.out.println(obj);
					}
				}	
			}

		
### 15结果集处理ScalarHandler
	* A: 结果集处理ScalarHandler
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					scalarHandler();
				}	
				/*
				 *  结果集第六种处理方法,ScalarHandler
				 *  对于查询后,只有1个结果
				 */
				public static void scalarHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT COUNT(*) FROM sort";
					//调用方法query,传递结果集处理实现类ScalarHandler
					long count = qr.query(con, sql, new ScalarHandler<Long>());
					System.out.println(count);
				}
			}

### 16结果集处理MapHandler
	* A: 结果集处理MapHandler
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					mapHandler();
				}
				/*
				 *  结果集第七种处理方法,MapHandler
				 *  将结果集第一行数据,封装到Map集合中
				 *  Map<键,值> 键:列名  值:这列的数据
				 */
				public static void mapHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT  * FROM sort";
					//调用方法query,传递结果集实现类MapHandler
					//返回值: Map集合,Map接口实现类, 泛型
					Map<String,Object> map = qr.query(con, sql, new MapHandler());
					//遍历Map集合
					for(String key : map.keySet()){
						System.out.println(key+".."+map.get(key));
					}
				}
			}

### 17结果集处理MapListHandler
	* A: 结果集处理MapListHandlerr
		* a: 案例代码
			public class QueryRunnerDemo1 {
				private static Connection con = JDBCUtilsConfig.getConnection();
				public static void main(String[] args) throws SQLException{
					mapListHandler();
				}
				/*
				 *  结果集第八种处理方法,MapListHandler
				 *  将结果集每一行存储到Map集合,键:列名,值:数据
				 *  Map集合过多,存储到List集合
				 */
				public static void mapListHandler()throws SQLException{
					QueryRunner qr = new QueryRunner();
					String sql = "SELECT  * FROM sort";
					//调用方法query,传递结果集实现类MapListHandler
					//返回值List集合, 存储的是Map集合
					List<Map<String,Object>> list = qr.query(con, sql, new MapListHandler());
					//遍历集合list
					for( Map<String,Object> map : list ){
						for(String key : map.keySet()){
							System.out.print(key+"..."+map.get(key));
						}
						System.out.println();
					}
					
				}
			}
			
### 18连接池介绍
	* A: 连接池介绍
		* a: 连接池介绍
			* 实际上就是存放连接的池子(容器)
			* 在开发中“获得连接”或“释放资源”是非常消耗系统资源的两个过程
			* 为了解决此类性能问题，通常情况我们采用连接池技术，来共享连接Connection。
			* 这样我们就不需要每次都创建连接、释放连接了，这些操作都交给了连接池			
		
### 19连接池概念规范和DataSource接口
	* A: 连接池概念规范和DataSource接口	
		* a: 连接池概念规范
			* 用池来管理Connection，这样可以重复使用Connection。
			* 不用自己来创建Connection，而是通过池来获取Connection对象
			* 使用完Connection后，调用Connection的close()方法也不会真的关闭Connection，而是把Connection“归还”给池
			* 连接池技术可以完成Connection对象的再次利用
		* b: DataSource接口
			* Java为数据库连接池提供了公共的接口：javax.sql.DataSource
			* 各个厂商需要让自己的连接池实现这个接口。这样应用程序可以方便的切换不同厂商的连接池
			* 常见的连接池：DBCP、C3P0
### 20DBCP连接池介绍
	* A: DBCP连接池介绍
		* a: DBCP连接池介绍
			* DBCP也是一个开源的连接池，是Apache Common成员之一，在企业开发中也比较常见，tomcat内置的连接池
		* tomcat服务器简单介绍	

### 21导入jar包
	* A: 导入jar包
		* a: jar包介绍	
			* mysql-connector-java-5.1.37-bin.jar：数据库驱动
			* commons-dbutils-1.6.jar：提供QueryRunner类方便进行增删改查操作
			* commons-dbcp-1.4.jar：
			* commons-pool-1.5.6.jar：提供高效的数据库连接池技术
		* b: 导入jar包
			* 在项目根路径下建立文件夹lib
			* 拷贝以上jar包，选定拷贝的jar包/右键/Build Path/Add to Build Path
			



### 22BasicDataSource类的使用
	* A: BasicDataSource类的使用
		* a: 案例代码
			/*
			 *  连接池jar包中,定义好一个类 BasicDataSource
			 *  实现类数据源的规范接口 javax.sql.DataSource
			 */
			public class DataSoruceDemo {
				public static void main(String[] args) {
					//创建DataSource接口的实现类对象
					//实现类, org.apache.commons.dbcp
					BasicDataSource dataSource = new BasicDataSource();
					//连接数据库的4个最基本信息,通过对象方法setXXX设置进来
					dataSource.setDriverClassName("com.mysql.jdbc.Driver");
					dataSource.setUrl("jdbc:mysql://localhost:3306/mybase");
					dataSource.setUsername("root");
					dataSource.setPassword("123");
					
					try{
					//调用对象方法getConnection获取数据库的连接
						Connection con = dataSource.getConnection();
						System.out.println(con);
					}catch(SQLException ex){
			//			System.out.println(ex);
						ex.printStackTrace();
						throw new RuntimeException("数据库连接失败");
					}
				}
			}

					
### 23BasicDataSource类的常见配置
	* A: BasicDataSource类的常见配置
		* a: 常见配置
			分类	属性			描述
			必须项	
					driverClassName	数据库驱动名称
					url				数据库的地址
					username		用户名
					password		密码
			基本项（扩展）	
					maxActive		最大连接数量
					minIdle			最小空闲连接
					maxIdle 		最大空闲连接
					initialSize		初始化连接

			
### 24实现数据库连接池工具类
	* A: 实现数据库连接池工具类
		* a: 案例代码
			/*
			 *  使用DBCP实现数据库的连接池
			 *  连接池配置,自定义类,
			 *  最基本四项完整
			 *  对于数据库连接池其他配置,自定义
			 */

			import javax.sql.DataSource;

			import org.apache.commons.dbcp.BasicDataSource;
			public class JDBCUtils{
				//创建出BasicDataSource类对象
				private static BasicDataSource datasource = new BasicDataSource();
				
				//静态代码块,对象BasicDataSource对象中的配置,自定义
				static{
					//数据库连接信息,必须的
					datasource.setDriverClassName("com.mysql.jdbc.Driver");
					datasource.setUrl("jdbc:mysql://localhost:3306/day33_user");
					datasource.setUsername("root");
					datasource.setPassword("123");
					//对象连接池中的连接数量配置,可选的
					datasource.setInitialSize(10);//初始化的连接数
					datasource.setMaxActive(8);//最大连接数量
					datasource.setMaxIdle(5);//最大空闲数
					datasource.setMinIdle(1);//最小空闲
				}
				
				
				//定义静态方法,返回BasicDataSource类的对象
				public static DataSource getDataSource(){
					return datasource;
				}
			}

						
### 25工具类的测试
	* A: 工具类的测试
		* a: 案例代码
			/*
			 *  测试写好的工具类,
			 *  提供的是一个DataSource接口的数据源
			 *  QueryRunner类构造方法,接收DataSource接口的实现类
			 *  后面,调用方法update,query,无需传递他们Connection连接对象
			 */

			import java.sql.SQLException;
			import java.util.List;

			import org.apache.commons.dbutils.QueryRunner;
			import org.apache.commons.dbutils.handlers.ArrayListHandler;

			import cn.itcast.jdbcutils.JDBCUtils;
			public class QueryRunnerDemo{
				public static void main(String[] args) {
					select();
				}
				//定义2个方法,实现数据表的添加,数据表查询
				//QueryRunner类对象,写在类成员位置
				private static QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource()); 
				
				//数据表查询
				public static void select(){
					String sql = "SELECT * FROM sort";
					try{
					List<Object[]> list = qr.query(sql, new ArrayListHandler());
					for(Object[] objs : list){
						for(Object obj : objs){
							System.out.print(obj+"\t");
						}
						System.out.println();
					}
					}catch(SQLException ex){
						throw new RuntimeException("数据查询失败");
					}
				}
				
				//数据表添加数据
				public static void insert(){
					String sql = "INSERT INTO sort (sname,sprice,sdesc)VALUES(?,?,?)";
					Object[] params = {"水果",100.12,"刚刚上市的核桃"};
					try{
						int row = qr.update(sql, params);
						System.out.println(row);
					}catch(SQLException ex){
						throw new RuntimeException("数据添加失败");
					}
				}
				
			}
		
### 26总结
	* 把今天的知识点总结一遍。
			
今日内容介绍
1、管家婆项目

### 01项目训练目标
	* A: 项目训练目标
		* a: 项目目标
			* 综合运用前面所学习的知识点
			* 熟练View层、Service层、Dao层之间的方法相互调用操作、
			* 熟练dbutils操作数据库表完成增删改查
			* 了解公司项目开发的流程，充分的掌握项目需求分析、设计与功能的代码实现。提高同学们独立分析需求与功能实现的能力。			
		
### 02项目中的功能模块
	* A: 项目中的功能模块	
		* a: 五大模块
			* 查询账务
			* 多条件组合查询账务
			* 添加账务
			* 编辑账务
			* 删除账务
			
### 03技术的选择和相关jar包
	* A: 技术的选择和相关jar包
		* a: apache的commons组件：
			* commons-dbutils-1.4.jar：封装并简化了JDBC；
			* commons-dbcp-1.4.jar：apache commons提供的数据库连接池组件，命名为DBCP；
		* b: commons.pool-1.3.jar：DBCP连接池依赖该jar包；
			* mysql-connector-java-5.1.28-bin.jar：MySQL的JDBC驱动包，用JDBC连接MySQL数据库必须使用该JAR包。


### 04项目中的工具类
	* A: 项目中的工具类
		* a: 工具类的介绍	
			* 每个项目中都会有很多个工具类，不要求每个工具类对能独立写出来，但是要会使用工具类
			* JDBCUtils：用来创建数据库连接池对象

### 05数据表的设计
	* A: 数据表的设计
		* a: 数据表的设计(详见：day34_source/表关系.JPG)
			* 表与表之间是有关系的
			* 主表和从表的关系
			* 主表中的主键作为从表中的外键

					
### 06创建数据库数据表写入测试数据
	* A: 创建数据库数据表写入测试数据
		* a: 创建数据库数据表
			/*
			  创建管家婆的数据库
			  名字 gjp
			*/
			CREATE DATABASE gjp;

			USE gjp;

			/*
			  创建数据表,表名账务
			  字段,列
			  主键
			  分类名称  可变字符
			  金额  double
			  账户  可变字符 (支付,收入方法)
			  创建日期 date
			  账务描述 可变字符
			*/

			CREATE TABLE gjp_zhangwu(
			   -- 主键
			   zwid INT PRIMARY KEY AUTO_INCREMENT,
			   -- 分类名称   
			   flname VARCHAR(200),
			   -- 金额
			   money DOUBLE,
			   -- 账户
			   zhanghu VARCHAR(100),
			   -- 创建日期
			   createtime DATE,
			   -- 账务描述
			   description  VARCHAR(1000)
			);
			SELECT * FROM gjp_zhangwu;
		* b: 写入数据
			-- 写入测试的数据
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (1,'吃饭支出',247,'交通银行','2016-03-02','家庭聚餐');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (2,'工资收入',12345,'现金','2016-03-15','开工资了');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (3,'服装支出',1998,'现金','2016-04-02','买衣服');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (4,'吃饭支出',325,'现金','2016-06-18','朋友聚餐');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (5,'股票收入',8000,'工商银行','2016-10-28','股票大涨');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (6,'股票收入',5000,'工商银行','2016-10-28','股票又大涨');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (7,'工资收入',5000,'交通银行','2016-10-28','又开工资了');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (8,'礼金支出',5000,'现金','2016-10-28','朋友结婚');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (9,'其他支出',1560,'现金','2016-10-29','丢钱了');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (10,'交通支出',2300,'交通银行','2016-10-29','油价还在涨啊');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (11,'吃饭支出',1000,'工商银行','2016-10-29','又吃饭');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (12,'工资收入',1000,'现金','2016-10-30','开资');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (13,'交通支出',2000,'现金','2016-10-30','机票好贵');
			INSERT  INTO gjp_zhangwu(zwid,flname,money,zhangHu,createtime,description) VALUES (14,'工资收入',5000,'现金','2016-10-30','又开资');



			
### 07项目中的分层设计
	* A: 项目中的分层设计
		* a: 各层功能介绍
			* view层作用: 视图层,即项目中的界面
			* controller层作用: 控制层, 获取界面上的数据,为界面设置数据; 将要实现的功能交给业务层处理
			* service层作用: 业务层, 功能的实现, 与controller控制层和数据访问层DAO交互, 将对数据库的操作交给DAO数据访问层来处理
			* dao层作用: 数据访问层, 用来操作数据库表的数据
			* db数据库: 这里指MySQL
			* domain 实体包: 存放JavaBean
			* tools工具包:存放项目中使用到的工具类
			* test 测试包: 存放项目功能测试的代码


						
### 08创建项目_分层_导入jar包
	* A: 创建项目_分层_导入jar包
		* a: 创建工程包
			* cn.itcast.gjp.app: 存放main方法类；
			* cn.itcast.gjp.domain: 存放JavaBean；
			* cn.itcast.gjp.view: 存放界面，及表现层类；
			* cn.itcast.gjp.service: 存放业务层类；
			* cn.itcast.gjp.dao: 存放数据访问层类;
			* cn.itcast.gjp.tools:存放工具类
		* b: 导入jar包
			* 在项目根路径下建立文件夹lib
			* 导入以下jar包
				* mysql-connector-java-5.1.37-bin.jar：数据库驱动
				* commons-dbutils-1.6.jar：提供QueryRunner类方便进行增删改查操作
				* commons-dbcp-1.4.jar：
				* commons-pool-1.5.6.jar：提供高效的数据库连接池技术				
			* 拷贝以上jar包，选定拷贝的jar包/右键/Build Path/Add to Build Path

 
### 09创建domain包中的类
	* A: 创建domain包中的类
		* a: 案例代码
			public class ZhangWu {
				 private int  zwid;
				  
				 private String flname; 
				
				 private double  money; 
				  
				 private String zhanghu;
				
				 private String createtime; 
				
				 private String description;
				 //注意生成空参构造、有参构造、set和get方法、toString方法等
			}
		
### 10创建JDBCUtils工具类
	* A：创建JDBCUtils工具类
		* a: 案例代码
			public class JDBCUtils{
				//创建BasicDataSource对象
				private static BasicDataSource datasource = new BasicDataSource();
				//静态代码块,实现必要参数设置
				static{
					datasource.setDriverClassName("com.mysql.jdbc.Driver");
					datasource.setUrl("jdbc:mysql://localhost:3306/gjp");
					datasource.setUsername("root");
					datasource.setPassword("123");
					datasource.setMaxActive(10);
					datasource.setMaxIdle(5);
					datasource.setMinIdle(2);
					datasource.setInitialSize(10);
				}
				public static DataSource getDataSource(){
					return datasource;
				}
			}
 
				
### 11创建其他包中的类

	* A: 创建其他包中的类
		* a: cn.itcast.gjp.dao包中创建ZhangWuDao类
			/*
			 *  实现对数据表 gjp_zhangwu 数据增删改查操作
			 *  dbuils工具类完成,类成员创建QueryRunner对象,指定数据源
			 */
			public class ZhangWuDao {
				private QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource());
			}
		* b: cn.itcast.gjp.service包中创建ZhangWuService类
			/*
			 *  业务层类
			 *  接收上一层,控制层controller的数据
			 *  经过计算,传递给dao层,操作数据库
			 *  调用dao层中的类,类成员位置,创建Dao类的对象
			 */
			public class ZhangWuService {
				private ZhangWuDao dao = new ZhangWuDao();
				
			}
		* c: cn.itcast.gjp.controller包中建立ZhangWuController类
			/*
			 *  控制器层
			 *  接收视图层的数据,数据传递给service层
			 *  成员位置,创建service对象
			 */
			public class ZhangWuController {
				private ZhangWuService service = new ZhangWuService();				
			}
		* d: cn.itcast.gjp.view包中建立MainView类
			/*
			 *  试图层,用户看到和操作的界面
			 *  数据传递给controller层实现
			 *  成员位置,创建controller对象
			 */
			public class MainView {
				private ZhangWuController controller = new ZhangWuController();
				
			}
		* e: cn.itcast.gjp.app包中建立MainApp类
			/*
			 *  主程序类,作用,开启软件程序
			 */
			public class MainApp {
				public static void main(String[] args) {
					new MainView().run();
				}
			}
			
### 12实现用户的界面菜单
	* A: 实现用户的界面菜单
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类中添加run方法
			/*
			 *  实现界面效果
			 *  接收用户的输入
			 *  根据数据,调用不同的功能方法
			 */
			public void run(){
				//创建Scanner类对象,反复键盘输入
				Scanner sc = new Scanner(System.in);
				while(true){
					System.out.println("---------------管家婆家庭记账软件---------------");
					System.out.println("1.添加账务　2.编辑账务　3.删除账务　4.查询账务　5.退出系统");
					System.out.println("请输入要操作的功能序号[1-5]:");
					//接收用户的菜单选择
					int choose = sc.nextInt();
					//对选择的菜单判断,调用不同的功能
					switch(choose){
					case 1:
					   // 选择添加账务,调用添加账务的方法
						break;
					case 2:
						// 选择的编辑账务,调用编辑账务方法
						break;
					case 3:
						// 选择的删除账务,调用删除账务方法
						break;
					case 4:
						// 选择的是查询账务,调用查询方法
						//selectZhangWu();
						break;
					case 5:
						System.exit(0);
						break;
					}
				}
			}
			

			


### 13实现查询的界面菜单
	* A: 实现查询的界面菜单
		* a: 案例核心代码
			*  cn.itcast.gjp.view包中建立MainView类中添加selectZhangWu方法、selectAll方法、select方法
				/*
				 * 定义方法 selectZhangWu()
				 * 显示查询的方式 1 所有查询   2 条件查询
				 * 接收用户的选择
				 */
				 public void selectZhangWu(){
					 System.out.println("1. 查询所有    2. 条件查询");
					 Scanner sc = new Scanner(System.in);
					 int selectChooser = sc.nextInt();
					 //判断根据用户的选择,调用不同的功能
					 switch(selectChooser){
					 case 1:
						 //选择的查询所有,调用查询所有的方法
						 selectAll();
						 break;
					 case 2:
						 //选的条件查询,调用带有查询条件的方法
						 select();
						 break;
					 }
				 }
				 /*
				  * 定义方法,实现查询所有的账务数据
				  */
				 public void selectAll(){
					 
				 }
				
				 /*
				  * 定义方法,实现条件查询账务数据
				  * 提供用户的输入日期,开始日期结束日期
				  * 就2个日期,传递到controller层
				  * 调用controller的方法,传递2个日期参数
				  * 获取到controller查询的结果集,打印出来
				  */
				 public void select(){
					
				 }
		
### 14实现查询所有账务的控制,业务层的实现
	* A: 实现查询所有账务的控制,业务层的实现
		* a: 案例核心代码
			* a: cn.itcast.gjp.dao包中创建ZhangWuDao类
			/*
			 *  实现对数据表 gjp_zhangwu 数据增删改查操作
			 *  dbuils工具类完成,类成员创建QueryRunner对象,指定数据源
			 */
			public class ZhangWuDao {
				private QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource());
				/*
				 * 定义方法,查询数据库,获取所有的账务数据
				 * 方法,由业务层调用
				 * 结果集,将所有的账务数据,存储到Bean对象中,存储到集合中
				 */
				public List<ZhangWu> selectAll(){					
					return null;
				}
			}
			* b: cn.itcast.gjp.service包中创建ZhangWuService类
				/*
				 *  业务层类
				 *  接收上一层,控制层controller的数据
				 *  经过计算,传递给dao层,操作数据库
				 *  调用dao层中的类,类成员位置,创建Dao类的对象
				 */
				public class ZhangWuService {
					private ZhangWuDao dao = new ZhangWuDao();
					/*
					 *  定义方法,实现查询所有的账务数据
					 *  此方法,由控制层调用, 去调用dao层的方法
					 *  返回存储ZhangWu对象的List集合
					 */
					public List<ZhangWu> selectAll(){
						return dao.selectAll();
					}
				}
			* c: cn.itcast.gjp.controller包中建立ZhangWuController类
				/*
				 *  控制器层
				 *  接收视图层的数据,数据传递给service层
				 *  成员位置,创建service对象
				 */
				public class ZhangWuController {
					private ZhangWuService service = new ZhangWuService();		
					/*
					 * 控制层类定义方法,实现查询所有的账务数据
					 * 方法由试图层调用,方法调用service层
					 */
					public List<ZhangWu> selectAll(){
						return service.selectAll();
					}					
				}
			
### 15实现查询所有账务的dao层的实现
	* A: 实现查询所有账务的dao层的实现
		* a: 案例核心代码
			* a: cn.itcast.gjp.dao包中创建ZhangWuDao类selectAll方法
			/*
			 *  实现对数据表 gjp_zhangwu 数据增删改查操作
			 *  dbuils工具类完成,类成员创建QueryRunner对象,指定数据源
			 */
			public class ZhangWuDao {
				private QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource());
				/*
				 * 定义方法,查询数据库,获取所有的账务数据
				 * 方法,由业务层调用
				 * 结果集,将所有的账务数据,存储到Bean对象中,存储到集合中
				 */
				public List<ZhangWu> selectAll(){
					try{
						//查询账务数据的SQL语句
							String sql = "SELECT * FROM gjp_zhangwu";
							//调用qr对象的方法,query方法,结果集BeanListHandler
							List<ZhangWu> list = qr.query(sql, new BeanListHandler<>(ZhangWu.class));
							return list;
						}catch(SQLException ex){
							System.out.println(ex);
							throw new RuntimeException("查询所有账务失败");
						}
				}
			}

			
### 16实现查询所有账务的view层的实现
	* A: 实现查询所有账务的view层的实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类selectAll方法
			/*
			  * 定义方法,实现查询所有的账务数据
			  */
			 public void selectAll(){
				 //调用控制层中的方法,查询所有的账务数据
				 List<ZhangWu> list = controller.selectAll();
				//输出表头
				 System.out.println("ID\t\t类别\t\t账户\t\t金额\t\t时间\t\t说明");
				 //遍历集合,结果输出控制台
				 for(ZhangWu zw : list){
					 System.out.println(zw.getZwid()+"\t\t"+zw.getFlname()+"\t\t"+zw.getZhanghu()+"\t\t"+
					 zw.getMoney()+"\t\t"+zw.getCreatetime()+"\t"+zw.getDescription());
				 }
			 }

### 17实现条件查询账务的菜单实现
	* A: 实现条件查询账务的菜单实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类select方法
			  /*
			  * 定义方法,实现条件查询账务数据
			  * 提供用户的输入日期,开始日期结束日期
			  * 就2个日期,传递到controller层
			  * 调用controller的方法,传递2个日期参数
			  * 获取到controller查询的结果集,打印出来
			  */
			 public void select(){
				 System.out.println("选择条件查询,输入日期格式XXXX-XX-XX");
				 Scanner sc = new Scanner(System.in);
				 System.out.print("请输入开始日期:");
				 String startDate = sc.nextLine();
				 System.out.print("请输入结果日期:");
				 String endDate = sc.nextLine();
				 //调用controller层的方法,传递日期,获取查询结果集
				 
			 }
			 
### 18实现条件查询账务的控制层,业务层实现
	* A: 实现条件查询账务的控制层,业务层实现
		* a: 案例核心代码
			* a: cn.itcast.gjp.dao包中创建ZhangWuDao类
				/*
				 *  实现对数据表 gjp_zhangwu 数据增删改查操作
				 *  dbuils工具类完成,类成员创建QueryRunner对象,指定数据源
				 */
				public class ZhangWuDao {
					private QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource());
					/*
					 * 定义方法,查询数据库,带有条件去查询账务表
					 * 由业务层调用,查询结果集存储到Bean对象,存储到List集合
					 * 调用者传递2个日期字符串
					 */
					public List<ZhangWu> select(String startDate,String endDate){
						return null;
					}
				}
			* b: cn.itcast.gjp.service包中创建ZhangWuService类
				/*
				 *  业务层类
				 *  接收上一层,控制层controller的数据
				 *  经过计算,传递给dao层,操作数据库
				 *  调用dao层中的类,类成员位置,创建Dao类的对象
				 */
				public class ZhangWuService {
					private ZhangWuDao dao = new ZhangWuDao();
					/*
					 * 定义方法,实现条件查询账务
					 * 方法由控制层调用,传递2个日期字符串
					 * 调用dao层的方法,传递2个日期字符串
					 * 获取到查询结果集
					 */
					public List<ZhangWu> select(String startDate,String endDate){
						return dao.select(startDate, endDate);
					}
				}
			* c: cn.itcast.gjp.controller包中建立ZhangWuController类
				/*
				 *  控制器层
				 *  接收视图层的数据,数据传递给service层
				 *  成员位置,创建service对象
				 */
				public class ZhangWuController {
					private ZhangWuService service = new ZhangWuService();		
					/*
					 * 定义方法,实现条件查询账务
					 * 方法由试图层调用,传递两个日期的字符串
					 * 调用service层的方法,传递两个日期字符串,获取结果集
					 * 结果集返回给试图
					 */
					public List<ZhangWu> select(String startDate,String endDate){
						return service.select(startDate, endDate);
					}					
				}
### 19实现条件查询账务的dao层实现
	* A: 实现条件查询账务的dao层实现
		* a: 案例核心代码
			* a: cn.itcast.gjp.dao包中创建ZhangWuDao类select方法
				/*
				 *  实现对数据表 gjp_zhangwu 数据增删改查操作
				 *  dbuils工具类完成,类成员创建QueryRunner对象,指定数据源
				 */
				public class ZhangWuDao {
					private QueryRunner qr = new QueryRunner(JDBCUtils.getDataSource());
					/*
					 * 定义方法,查询数据库,带有条件去查询账务表
					 * 由业务层调用,查询结果集存储到Bean对象,存储到List集合
					 * 调用者传递2个日期字符串
					 */
					public List<ZhangWu> select(String startDate,String endDate){
						try{
							//拼写条件查询的SQL语句
							String sql = "SELECT * FROM gjp_zhangwu WHERE createtime BETWEEN ? AND ?";
							//定义对象数组,存储?占位符
							Object[] params = {startDate,endDate};
							//调用qr对象的方法query查询数据表,获取结果集
							return qr.query(sql, new BeanListHandler<>(ZhangWu.class),params);
						}catch(SQLException ex){
							System.out.println(ex);
							throw new RuntimeException("条件查询失败");
						}
					}
				}

### 20实现条件查询账务的view层实现
	* A: 实现条件查询账务的view层实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类selectAll方法优化、抽取print方法、select方法
			/*
			  * 定义方法,实现查询所有的账务数据
			  */
			 public void selectAll(){
				 //调用控制层中的方法,查询所有的账务数据
				 List<ZhangWu> list = controller.selectAll();
				 if(list.size()!=0)
					 print(list);
				 else
					 System.out.println("没有查询到数据");
			 }
			
			 /*
			  * 定义方法,实现条件查询账务数据
			  * 提供用户的输入日期,开始日期结束日期
			  * 就2个日期,传递到controller层
			  * 调用controller的方法,传递2个日期参数
			  * 获取到controller查询的结果集,打印出来
			  */
			 public void select(){
				 System.out.println("选择条件查询,输入日期格式XXXX-XX-XX");
				 Scanner sc = new Scanner(System.in);
				 System.out.print("请输入开始日期:");
				 String startDate = sc.nextLine();
				 System.out.print("请输入结果日期:");
				 String endDate = sc.nextLine();
				 //调用controller层的方法,传递日期,获取查询结果集
				 List<ZhangWu> list = controller.select(startDate, endDate);
				 if(list.size()!=0)
					 print(list);
				 else
					 System.out.println("没有查询到数据");
			 }
			 
			 //输出账务数据方法,接收List集合,遍历集合,输出表格
			 private void print(List<ZhangWu> list) {
					//输出表头
					 System.out.println("ID\t\t类别\t\t账户\t\t金额\t\t时间\t\t说明");
					 //遍历集合,结果输出控制台
					 for(ZhangWu zw : list){
						 System.out.println(zw.getZwid()+"\t\t"+zw.getFlname()+"\t\t"+zw.getZhanghu()+"\t\t"+
						 zw.getMoney()+"\t\t"+zw.getCreatetime()+"\t"+zw.getDescription());
					 }
				}
				
### 21添加账务功能分析
	* A: 添加账务功能分析
		* a: 编写MainView类中addZhangWu方法
			* 键盘输入新添加的账务信息
			* 调用ZhangWuService类中addZhangWu方法，用来指定账务的添加
			* 添加完毕后，使用输出语句，提示“添加账务成功！”
		* b: 编写ZhangWuService类中addZhangWu方法
			* 调用ZhangWuDao类中addZhangWu方法，用来指定账务的添加
		* c: 编写ZhangWuDao类中addZhangWu方法
			* 通过QueryRunner对象，调用update方法更新数据库表gjp_zhangwu，完成指定账务添加到数据库表中
		
		
### 22添加账务功能菜单和输入功能实现
	* A: 添加账务功能菜单和输入功能实现	
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类addZhangWu方法
			/*
			 * 定义方法addZhangWu
			 * 添加账务的方法，用户在界面中选择菜单1的时候调用、
			 * 实现思想：
			 * 	  接收键盘输入，5项输入，调用controller层方法
			 */
			public void addZhangWu() {
				System.out.println("选择的添加账务功能，请输入以下内容");
				Scanner sc = new Scanner(System.in);
				System.out.println("输入分类名称");
				String flname = sc.next();
				System.out.println("输入金额");
				double money = sc.nextDouble();
				System.out.println("输入账户");
				String zhanghu = sc.next();
				System.out.println("输入日期：格式XXXX-XX-xx");
				String createtime = sc.next();
				System.out.println("输入具体描述");
				String description = sc.next();
				//将接收到的数据，调用controller层的方法，传递参数，实现数据添加
				
			}
			
### 23添加账务功能控制层,业务层实现
	* A: 添加账务功能控制层,业务层实现
		* a: 案例核心代码
			* cn.itcast.gjp.controller包中的ZhangWuController类addZhangWu方法
				/*
				 * 定义方法，实现账务添加功能
				 * 由视图层调用，传递参数(传递过来的参数不能是5个数据，传递的是一个ZhangWu类型的对象)
				 * 本方法调用service层的方法，传递ZhangWu对象，获取到添加后的结果集(添加成功影响的行数，int)
				 * 
				 */
				public void addZhangWu(ZhangWu zw) {
					service.addZhangWu(zw);
				}
			* cn.itcast.gjp.service包中的ZhangWuService类addZhangWu方法
				/*
				 * 定义方法，实现添加账务
				 * 是由控制层调用，传递ZhangWu对象
				 */
				public void addZhangWu(ZhangWu zw) {
					dao.addZhangWu(zw);
				}
			* cn.itcast.gjp.dao包中的ZhangWuDao类addZhangWu方法
				/*
				 * 定义方法，实现添加账务功能
				 * 由业务层调用，传递ZhangWu对象
				 * 将ZhangWu对象中的数据，添加到数据库
				 */
				public void addZhangWu(ZhangWu zw) {
					 
				}
				
### 24添加账务功能dao层实现
	* A: 添加账务功能dao层实现
		* a: 案例核心代码	
			* cn.itcast.gjp.dao包中的ZhangWuDao类的addZhangWu方法
				public void addZhangWu(ZhangWu zw) {
					try{
						 //拼接添加数据的sql
						String sql = "INSERT INTO gjp_zhangwu (flname,money,zhanghu,createtime,description) VALUES(?,?,?,?,?)";
						//创建对象数组，处处5个占位符的实际参数
						//实际参数来源是传递过来的对象ZhangWu
						Object[] params = {zw.getFlname(),zw.getMoney(),zw.getZhanghu(),zw.getCreatetime(),zw.getDescription()};
						//调用qr对象中的方法update执行添加
						qr.update(sql, params);
					}catch(SQLException ex) {
						System.out.println(ex);
						throw new RuntimeException("账务添加失败");
					}
				}
		
### 25添加账务功能view层实现
	* A: 添加账务功能view层实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类addZhangWu方法
				public void addZhangWu() {
					System.out.println("选择的添加账务功能，请输入以下内容");
					Scanner sc = new Scanner(System.in);
					System.out.println("输入分类名称");
					String flname = sc.next();
					System.out.println("输入金额");
					double money = sc.nextDouble();
					System.out.println("输入账户");
					String zhanghu = sc.next();
					System.out.println("输入日期：格式XXXX-XX-xx");
					String createtime = sc.next();
					System.out.println("输入具体描述");
					String description = sc.next();
					//将接收到的数据，调用controller层的方法，传递参数，实现数据添加
					//将用户输入的所有参数，封装成ZhangWu对象
					ZhangWu zw = new ZhangWu(0, flname, money, zhanghu, createtime, description);
					controller.addZhangWu(zw);
					System.out.println("恭喜添加账务成功");
				}

					
### 26编辑账务功能分析
	* A: 编辑账务功能分析
		* a: 编写MainView类中editZhangWu方法
			* 键盘输入要编辑的账务信息ID号
			* 键盘输入要修改的账务信息内容
			* 调用ZhangWuService类中editZhangWu方法，用来将指定的账务信息进行更新
			* 更新完毕后，使用输出语句，提示 “编辑账务成功！”
		* b: 编写ZhangWuService类中editZhangWu方法
			* 调用ZhangWuDao类中editZhangWu方法，用来将指定的账务信息进行更新
		* c: 编写ZhangWuDao类中editZhangWu方法
			* 通过QueryRunner对象，调用update方法更新数据库表gjp_zhangwu，完成数据库表中指定账务更新操作



			
### 27编辑账务功能功能之前实现查询所有
	* A: 编辑账务功能功能之前实现查询所有
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类editZhangWu方法
				public void editZhangWu() {
					//调用查询所有账务数据的功能，显示出来
					//看到所有数据，从中选择一项，进行修改
					selectAll();
					System.out.println("选择的是编辑功能，请输入数据");
					
					
				}
						
### 28编辑账务功能菜单实现
	* A: 编辑账务功能菜单实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类editZhangWu方法
				public void editZhangWu() {
					//调用查询所有账务数据的功能，显示出来
					//看到所有数据，从中选择一项，进行修改
					selectAll();
					System.out.println("选择的是编辑功能，请输入数据");
					Scanner sc = new Scanner(System.in);
					System.out.print("请输入ID");
					int zwid = sc.nextInt();
					System.out.println("输入分类名称");
					String flname = sc.next();
					System.out.println("输入金额");
					double money = sc.nextDouble();
					System.out.println("输入账户");
					String zhanghu = sc.next();
					System.out.println("输入日期：格式XXXX-XX-xx");
					String createtime = sc.next();
					System.out.println("输入具体描述");
					String description = sc.next();
					//将用户输入的数据，封装到ZhangWu对象中
					//用户输入的ID，必须封装到到对象中
					ZhangWu zw = new ZhangWu(zwid, flname, money, zhanghu, createtime, description);
					//调用controller层中的方法，实现编辑账务
				}			
 
### 29编辑账务功能控制层,业务层实现
	* A: 编辑账务功能控制层,业务层实现
		* a: 案例核心代码
			* cn.itcast.gjp.controller包中的ZhangWuController类editZhangWu方法
				/*
				 * 定义方法，实现编辑账务功能
				 * 由视图层调用，传递参数，也是ZhangWu对象
				 * 调用service层的方法，也是ZhangWu对象
				 */
				public void editZhangWu(ZhangWu zw) {
					service.editZhangWu(zw);
				}
			* cn.itcast.gjp.service包中的ZhangWuService类editZhangWu方法
				/*
				 * 定义方法，实现编辑账务
				 * 由控制层调用，传递ZhangWu对象
				 * 调用dao层的方法，传递ZhangWu对象
				 */
				public void editZhangWu(ZhangWu zw) {
					dao.editZhangWu(zw);
				}
			* cn.itcast.gjp.dao包中的ZhangWuDao类editZhangWu方法
				public void editZhangWu(ZhangWu zw) {
					// TODO Auto-generated method stub
					
				}
		
### 30编辑账务功能dao层实现
	* A：编辑账务功能dao层实现
		* a: 案例核心代码
			* cn.itcast.gjp.dao包中的ZhangWuDao类editZhangWu方法
				/*
				 * 定义方法，实现编辑功能
				 * 由业务层调用，传递ZhangWu对象
				 * 将对象中的数据，更新到数据表
				 */
				public void editZhangWu(ZhangWu zw) {
					try {
						//更新数据的SQL
						String sql = "UPDATE zhangwu SET flname=?,money=?,zhanghu=?,createtime=?,description=? WHERE zwid=?";
						//定义对象数组，封装所有数据
						Object[] params = {zw.getFlname(),zw.getMoney(),zw.getZhanghu(),zw.getCreatetime(),zw.getDescription(),zw.getZwid()};
						//调用qr对象方法update执行更新
						qr.update(sql, params);
					} catch (SQLException ex) {
						System.out.println(ex);
						throw new RuntimeException("编辑账务失败");
					}
					
				}
 
				
### 31编辑账务功能view层实现
	* A: 编辑账务功能view层实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类editZhangWu方法
				/*
				 * 定义方法，实现对账务的编辑功能
				 * 实现思想：
				 * 	接收用户的输入的信息
				 *  封装成ZhangWu对象
				 *  调用控制层的方法，传递ZhangWu对象，实现编辑
				 * 
				 */
				public void editZhangWu() {
					//调用查询所有账务数据的功能，显示出来
					//看到所有数据，从中选择一项，进行修改
					selectAll();
					System.out.println("选择的是编辑功能，请输入数据");
					Scanner sc = new Scanner(System.in);
					System.out.print("请输入ID");
					int zwid = sc.nextInt();
					System.out.println("输入分类名称");
					String flname = sc.next();
					System.out.println("输入金额");
					double money = sc.nextDouble();
					System.out.println("输入账户");
					String zhanghu = sc.next();
					System.out.println("输入日期：格式XXXX-XX-xx");
					String createtime = sc.next();
					System.out.println("输入具体描述");
					String description = sc.next();
					//将用户输入的数据，封装到ZhangWu对象中
					//用户输入的ID，必须封装到到对象中
					ZhangWu zw = new ZhangWu(zwid, flname, money, zhanghu, createtime, description);
					//调用controller层中的方法，实现编辑账务
					controller.editZhangWu(zw);
					System.out.println("账务编辑成功");
				}
		


### 32删除账务功能分析
	* A: 删除账务功能分析
		* a: 编写MainView类中deleteZhangWu方法
			* 键盘输入要删除的账务信息ID号
			* 调用ZhangWuService类中deleteZhangWu方法，用来将指定的账务信息删除
			* 删除完毕后，使用输出语句，提示 “删除账务成功！”
		* b: 编写ZhangWuService类中deleteZhangWu方法
			* 调用ZhangWuDao类中deleteZhangWu方法，用来将指定的账务信息删除
		* c: 编写ZhangWuDao类中deleteZhangWu方法
			* 通过QueryRunner对象，调用update方法更新数据库表gjp_zhangwu，完成数据库表中指定账务删除操作


			


### 33删除账务功能菜单实现
	* A: 删除账务功能菜单实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类deleteZhangWu方法
				/*
				 * 定义方法，实现账务删除
				 * 实现思想：
				 * 	接收用户的输入，输入一个主键数据
				 *  调用控制层方法，传递一个主键
				 */
				public void deleteZhangWu() {
					//调用查询所有账务数据的功能，显示出来
					//看到所有数据，从中选择一项，进行修改
					selectAll();
					System.out.println("选择的是删除功能，请输入序号即可");
					int zwid = new Scanner(System.in).nextInt();
					//调用控制层方法，传递主键id即可
				}
		
### 34删除账务功能控制层,业务层实现
	* A: 删除账务功能控制层,业务层实现
		* a: 案例核心代码
			* cn.itcast.gjp.controller包中的ZhangWuController类deleteZhangWu方法
				/*
				 * 定义方法，实现删除功能
				 * 视图层调用，传递int类型主键
				 * 调用service层方法，传递int主键
				 */
				public void deleteZhangWu(int zwid) {
					service.deleteZhangWu(zwid);
				}
			* cn.itcast.gjp.service包中的ZhangWuService类deleteZhangWu方法
				/*
				 * 定义方法，实现删除账务功能
				 * 由控制层调用，传递主键id
				 * 调用dao层方法，传递主键id
				 */
				public void deleteZhangWu(int zwid) {
					dao.deleteZhangWu(zwid);
				}
			* cn.itcast.gjp.dao包中的ZhangWuDao类deleteZhangWu方法
				public void deleteZhangWu(int zwid) {
		
				}
			
### 35删除账务功能dao实现
	* A: 删除账务功能dao实现
		* a: 案例核心代码
			* cn.itcast.gjp.dao包中的ZhangWuDao类deleteZhangWu方法
				/*
				 * 定义方法，实现删除业务
				 * 业务层调用，传递主键id
				 */
				public void deleteZhangWu(int zwid) {
					try {
						//拼写删除数据SQL
						String sql = "DELETE FROM gjp_zhangwu WHERE zwid=?";
						qr.update(sql, zwid);
					} catch (SQLException ex) {
						System.out.println(ex);
						throw new RuntimeException("删除账务失败");
					}
				}

			
### 36删除账务功能view层实现
	* A: 删除账务功能view层实现
		* a: 案例核心代码
			* cn.itcast.gjp.view包中建立MainView类editZhangWu方法
				/*
				 * 定义方法，实现账务删除
				 * 实现思想：
				 * 	接收用户的输入，输入一个主键数据
				 *  调用控制层方法，传递一个主键
				 */
				public void deleteZhangWu() {
					//调用查询所有账务数据的功能，显示出来
					//看到所有数据，从中选择一项，进行修改
					selectAll();
					System.out.println("选择的是删除功能，请输入序号即可");
					int zwid = new Scanner(System.in).nextInt();
					//调用控制层方法，传递主键id即可
					controller.deleteZhangWu(zwid);
					System.out.println("删除账务成功");
			
### 37总结
	* 把今天的知识点总结一遍。
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 
今日内容介绍
1、类加载器
2、反射构造方法
3、反射成员变量
4、反射成员方法
5、反射配置文件运行类中的方法


第一节课 类加载器
### 01类的加载.avi(11:08)
### 02类的加载时机.avi(06:19)
### 03三种类的加载器.avi(05:14)

第二节课 反射
### 01反射的概念以及作用.avi(09:23)
### 02class文件的产生过程.avi(05:27)

### 03获取class文件对象三种方式.avi(11:57)
### 04反射获取空参数构造方法并运行.avi(15:55)
### 05反射获取有参数的构造方法并运行.avi(06:27)
### 06反射获取构造方法并运行的快速的方式.avi(06:14)

### 07反射获取私有构造方法并运行.avi(09:41)
### 08反射获取成员变量并改值.avi(09:22)
### 09反射获取空参数成员方法并运行.avi(11:23)
### 10反射获取有参数的成员方法并运行.avi(03:43)

### 11反射泛型擦除.avi(10:29)
### 12反射通过配置文件运行的步骤.avi(07:05)
### 13反射通过配置文件运行功能实现.avi(09:12)

============上面的内容,方便我们只做ppt,word教案以及书写下面的简要的笔记=================



### 01类加载器
	* A.类的加载
		当程序要使用某个类时，如果该类还未被加载到内存中，则系统会通过加载，连接，初始化三步来实现对这个类进行初始化。
		* a 加载 
			* 就是指将class文件读入内存，并为之创建一个Class对象。
			* 任何类被使用时系统都会建立一个Class对象
		* b 连接
			* 验证 是否有正确的内部结构，并和其他类协调一致
			* 准备 负责为类的静态成员分配内存，并设置默认初始化值
			* 解析 将类的二进制数据中的符号引用替换为直接引用
		* c 初始化 
			* 就是我们以前讲过的初始化步骤（new 对象）
		* 注：简单的说就是：把.class文件加载到内存里，并把这个.class文件封装成一个Class类型的对象。
	* B.类的加载时机
		以下的情况，会加载这个类。
		* a. 创建类的实例
		* b. 类的静态变量，或者为静态变量赋值
		* c. 类的静态方法
		* d. 使用反射方式来强制创建某个类或接口对应的java.lang.Class对象
		* e. 初始化某个类的子类
		* f. 直接使用java.exe命令来运行某个主类
			
	* C: 类加载器(了解)
		负责将.class文件加载到内在中，并为之生成对应的Class对象。
		* a. Bootstrap ClassLoader 根类加载器
			* 也被称为引导类加载器，负责Java核心类的加载
			* 比如System,String等。在JDK中JRE的lib目录下rt.jar文件中
		* b. Extension ClassLoader 扩展类加载器
			* 负责JRE的扩展目录中jar包的加载。
			* 在JDK中JRE的lib目录下ext目录
		* c. System ClassLoader 系统类加载器
			* 负责在JVM启动时加载来自java命令的class文件，以及classpath环境变量所指定的jar包和类路径。
			* 我们用的是System ClassLoader 系统类加载器

### 02反射
	* A. 反射定义
		* a. JAVA反射机制是在运行状态中，
				对于任意一个类，都能够知道这个类的所有属性和方法；
				对于任意一个对象，都能够调用它的任意一个方法和属性；
			这种动态获取的信息以及动态调用对象的方法的功能称为java语言的反射机制。

		* b.反射技术
			条件：运行状态
			已知：一个类或一个对象(根本是已知.class文件)
			结果：得到这个类或对象的所有方法和属性
	
		* 注: 要想解剖一个类,必须先要获取到该类的字节码文件对象。而解剖使用的就是Class类中的方法.所以先要获取到每一个字节码文件对应的Class类型的对象。
	* B. Class类
		* a. Class类及Class对象的了解
			要想解剖一个类，必须先了解Class对象。
			阅读API的Class类得知，Class 没有公共构造方法。Class 对象是在加载类时由 Java 虚拟机以及通过调用类加载器中的 defineClass 方法自动构造的。
		* b. 得到Class对象
			* 1. 有三个方法
				方式一: 通过Object类中的getClass()方法
					Person person = new Person();
					Class clazz = person.getClass();
				方式二: 通过 类名.class 获取到字节码文件对象（任意数据类型都具备一个class静态属性,看上去要比第一种方式简单）。
					Class clazz = Person.class;
				方式三: 通过Class类中的方法（将类名作为字符串传递给Class类中的静态方法forName即可）。
					Class c3 = Class.forName("Person");
				注：第三种和前两种的区别是：
						前两种你必须明确Person类型.
						后面是指定这种类型的字符串就行.这种扩展更强.我不需要知道你的类.我只提供字符串,按照配置文件加载就可以了

			* 2. 得到Class对象的三个方法代码演示：
				代码演示
				/*
				 * 获取.class字节码文件对象的方式
				 * 		1：通过Object类中的getObject()方法
				 * 		2: 通过 类名.class 获取到字节码文件对象
				 * 		3: 反射中的方法,
				 * 			public static Class<?> forName(String className) throws ClassNotFoundException
				 * 			返回与带有给定字符串名的类或接口相关联的 Class 对象 
				 */
				public class ReflectDemo {
					public static void main(String[] args) throws ClassNotFoundException {
						// 1： 通过Object类中的getObject()方法
						// Person p1 = new Person();
						// Class c1 = p1.getClass();
						// System.out.println("c1 = "+ c1);

						// 2: 通过 类名.class 获取到字节码文件对象
						// Class c2 = Person.class;
						// System.out.println("c2 = "+ c2);

						// 3: 反射中的方法
						Class c3 = Class.forName("cn.itcast_01_Reflect.Person");// 包名.类名
						System.out.println("c3 = " + c3);
					}
				}
				Person类
				package cn.itcast_01_Reflect;
				public class Person {
					//成员变量
					public String name;
					public int age;
					private String address;

					//构造方法
					public Person() {
						System.out.println("空参数构造方法");
					}
					
					public Person(String name) {
						this.name = name;
						System.out.println("带有String的构造方法");
					}
					//私有的构造方法
					private Person(String name, int age){
						this.name = name;
						this.age = age;
						System.out.println("带有String，int的构造方法");
					}
					
					public Person(String name, int age, String address){
						this.name = name;
						this.age = age;
						this.address = address;
						System.out.println("带有String, int, String的构造方法");
					}
					
					//成员方法
					//没有返回值没有参数的方法
					public void method1(){
						System.out.println("没有返回值没有参数的方法");
					}
					//没有返回值，有参数的方法
					public void method2(String name){
						System.out.println("没有返回值，有参数的方法 name= "+ name);
					}
					//有返回值，没有参数
					public int method3(){
						System.out.println("有返回值，没有参数的方法");
						return 123;
					}
					//有返回值，有参数的方法
					public String method4(String name){
						System.out.println("有返回值，有参数的方法");
						return "哈哈" + name;
					}
					//私有方法
					private void method5(){
						System.out.println("私有方法");
					}

					@Override
					public String toString() {
						return "Person [name=" + name + ", age=" + age + ", address=" + address+ "]";
					}
				}
			* 注: Class类型的唯一性
				因为一个.class文件在内存里只生成一个Class对象，所以无论那一种方法得到Class对象，得到的都是同一个对象。
	* C.通过反射获取无参构造方法并使用
		* a. 得到无参构造方法
			public Constructor<?>[] getConstructors() 
				获取所有的public 修饰的构造方法。
				选择无参构造方法，不建议使用。
			public Constructor<T> getConstructor(Class<?>... parameterTypes) 
				获取public修饰, 指定参数类型所对应的构造方法。
				不传参数得到无参构造方法。
		* b. 运行无参构造方法
			public T newInstance(Object... initargs) 
				使用此 Constructor 对象表示的构造方法来创建该构造方法的声明类的新实例，并用指定的初始化参数初始化该实例。 
				因为是无参构造，所以不传参数。
		* c. 通过反射获取无参构造方法并使用的代码演示：
				package cn.itcast.demo1;

				import java.lang.reflect.Constructor;

				/*
				 *  通过反射获取class文件中的构造方法,运行构造方法
				 *  运行构造方法,创建对象
				 *    获取class文件对象
				 *    从class文件对象中,获取需要的成员
				 *    
				 *  Constructor 描述构造方法对象类
				 */
				public class ReflectDemo1 {
					public static void main(String[] args) throws Exception {
					
						Class c = Class.forName("cn.itcast.demo1.Person");
						//使用class文件对象,获取类中的构造方法
						//  Constructor[]  getConstructors() 获取class文件对象中的所有公共的构造方法
						/*Constructor[] cons = c.getConstructors();
						for(Constructor con : cons){
							System.out.println(con);
						}*/
						//获取指定的构造方法,空参数的构造方法
						Constructor con =  c.getConstructor();
						//运行空参数构造方法,Constructor类方法 newInstance()运行获取到的构造方法
						Object obj = con.newInstance();
						System.out.println(obj.toString());
					}
				}
	* D. 通过反射获取有参构造方法并使用
		* a. 得到有参的构造方法
			public Constructor<T> getConstructor(Class<?>... parameterTypes) 
				获取public修饰, 指定参数类型所对应的构造方法。
				传相应的参数类型得到有参构造方法。
		* b. 运行无参构造方法
			public T newInstance(Object... initargs) 
				使用此 Constructor 对象表示的构造方法来创建该构造方法的声明类的新实例，并用指定的初始化参数初始化该实例。 
				因为是有参构造，所以传相应的参数值。
		* c. 通过反射获取有参构造方法并使用的代码演示：
			package cn.itcast.demo1;

			import java.lang.reflect.Constructor;

			/*
			 *  通过反射,获取有参数的构造方法并运行
			 *  方法getConstructor,传递可以构造方法相对应的参数列表即可
			 */
			public class ReflectDemo2 {
				public static void main(String[] args)throws Exception {
					Class c = Class.forName("cn.itcast.demo1.Person");
					//获取带有,String和int参数的构造方法
					//Constructor<T> getConstructor(Class<?>... parameterTypes)  
					//Class<?>... parameterTypes 传递要获取的构造方法的参数列表
					Constructor con = c.getConstructor(String.class,int.class);
					//运行构造方法
					// T newInstance(Object... initargs)  
					//Object... initargs 运行构造方法后,传递的实际参数
					Object obj = con.newInstance("张三",20);
					System.out.println(obj);
				}
			}
	* E. 通过反射获取有参构造方法并使用快捷方式
		* a. 使用的前提
			类有空参的公共构造方法。（如果是同包，默认权限也可以）
		* b. 使用的基础
			Class类的 public T newInstance() 方法
				 创建此 Class 对象所表示的类的一个新实例。
		* c. 通过反射获取有参构造方法并使用快捷方式的代码演示：
			package cn.itcast.demo1;
			/*
			 * 反射获取构造方法并运行,有快捷点的方式
			 * 有前提:
			 *   被反射的类,必须具有空参数构造方法
			 *   构造方法权限必须public
			 */
			public class ReflectDemo3 {
				public static void main(String[] args) throws Exception {
					Class c = Class.forName("cn.itcast.demo1.Person");
					// Class类中定义方法, T newInstance() 直接创建被反射类的对象实例
					Object obj = c.newInstance();
					System.out.println(obj);
				}
			}
	* F. 通过反射获取私有构造方法并使用
		* a. 得到私有的构造方法
			public Constructor<T> getDeclaredConstructor(Class<?>... parameterTypes) 
				获取指定参数类型所对应的构造方法(包含私有的)。
			public Constructor<?>[] getDeclaredConstructors() 
				获取所有的构造方法(包含私有的)。
		* b. 运行私有构造方法
			public void setAccessible(boolean flag)
				将此对象的 accessible 标志设置为指示的布尔值。
				设置为true,这个方法保证我们得到的私有构造方法的运行。（取消运行时期的权限检查。）
			public T newInstance(Object... initargs) 
				使用此 Constructor 对象表示的构造方法来创建该构造方法的声明类的新实例，并用指定的初始化参数初始化该实例。 
		* c. 通过反射获取私有构造方法并使用的代码演示：
			package cn.itcast.demo1;

			import java.lang.reflect.Constructor;

			/*
			 *  反射获取私有的构造方法运行
			 *  不推荐,破坏了程序的封装性,安全性
			 *  暴力反射
			 */
			public class ReflectDemo4 {
				public static void main(String[] args) throws Exception{
					Class c = Class.forName("cn.itcast.demo1.Person");
					//Constructor[] getDeclaredConstructors()获取所有的构造方法,包括私有的
					/*Constructor[] cons = c.getDeclaredConstructors();
					for(Constructor con : cons){
						System.out.println(con);
					}*/
					//Constructor getDeclaredConstructor(Class...c)获取到指定参数列表的构造方法
					Constructor con = c.getDeclaredConstructor(int.class,String.class);
					
					//Constructor类,父类AccessibleObject,定义方法setAccessible(boolean b)
					con.setAccessible(true);
					
					Object obj = con.newInstance(18,"lisi");
					System.out.println(obj);
				}
			}
		* 注：不推荐，破坏了程序的封装性,安全性。
	* G. 反射获取成员变量并改值
		* a. 获取成员变量
			* 得到公共的成员变量
				public Field getField(String name) 
					返回一个 Field 对象，它反映此 Class 对象所表示的类或接口的指定公共成员字段。 
				public Field[] getFields() 
					返回一个包含某些 Field 对象的数组，这些对象反映此 Class 对象所表示的类或接口的所有可访问公共字段。 
			* 得到所有的成员变量(包括私有的，如果要进行修改私有成员变量，要先进行public void setAccessible(boolean flag) 设置。)
				public Field getDeclaredField(String name) 
					返回一个 Field 对象，该对象反映此 Class 对象所表示的类或接口的指定已声明字段。 
				public Field[] getDeclaredFields() 
					返回 Field 对象的一个数组，这些对象反映此 Class 对象所表示的类或接口所声明的所有字段。 
		* b. 修改成员变量(Field)的值
			* 修改公共的成员变量
				public void set(Object obj, Object value) 
					将指定对象变量上此 Field 对象表示的字段设置为指定的新值。 
					obj指的是修改的是那个对象的这个成员变量值。
		* c. 反射获取成员变量并改值的代码演示
			package cn.itcast.demo1;
			import java.lang.reflect.Field;
			/*
			 *  反射获取成员变量,并修改值
			 *  Person类中的成员String name
			 */
			public class ReflectDemo5 {
				public static void main(String[] args) throws Exception{
					Class c = Class.forName("cn.itcast.demo1.Person");
					Object obj = c.newInstance();
					//获取成员变量 Class类的方法 getFields() class文件中的所有公共的成员变量
					//返回值是Field[]    Field类描述成员变量对象的类
					/*Field[] fields = c.getFields();
					for(Field f : fields){
						System.out.println(f);
					}*/
					
					//获取指定的成员变量 String name
					//Class类的方法  Field getField(传递字符串类型的变量名) 获取指定的成员变量
					Field field = c.getField("name");
				   
					//Field类的方法 void set(Object obj, Object value) ,修改成员变量的值
					//Object obj 必须有对象的支持,  Object value 修改后的值
					field.set(obj,"王五");
					System.out.println(obj);
					
				}
			}
	* H. 反射获取空参数成员方法并运行
		* a. 获取空参数成员方法
			* 得到公共的成员方法
				public Method getMethod(String name, Class<?>... parameterTypes) 
					返回一个 Method 对象，它反映此 Class 对象所表示的类或接口的指定公共成员方法。 
				public Method[] getMethods()
					返回一个包含某些 Method 对象的数组，这些对象反映此 Class对象所表示的类或接口（包括那些由该类或接口声明的以及从超类和超接口继承的那些的类或接口）的公共 member 方法。
			* 得到全部的成员方法(包括私有的，如果要使用私有成员方法，要先进行public void setAccessible(boolean flag) 设置。)
				public Method getDeclaredMethod(String name, Class<?>... parameterTypes) 
					返回一个 Method 对象，该对象反映此 Class 对象所表示的类或接口的指定已声明方法。 
				public Method[] getDeclaredMethods() 
					返回 Method 对象的一个数组，这些对象反映此 Class 对象表示的类或接口声明的所有方法，包括公共、保护、默认（包）访问和私有方法，但不包括继承的方法。 
		* b. 使用Method方法对象
			public Object invoke(Object obj, Object... args) 
				对带有指定参数的指定对象调用由此 Method 对象表示的底层方法。 
				obj 指的是调这个方法的对象。
				args 指的是调用这个方法所要用到的参数列表。
				返回值Object就是方法的返回对象。如果方法没有返回值 ，返回的是null.
		* c. 反射获取空参数成员方法并运行代码演示
			package cn.itcast.demo1;

			import java.lang.reflect.Method;

			/*
			 *  反射获取成员方法并运行
			 *  public void eat(){}
			 */
			public class ReflectDemo6 {
				public static void main(String[] args) throws Exception{
					Class c = Class.forName("cn.itcast.demo1.Person");
					Object obj = c.newInstance();
					//获取class对象中的成员方法
					// Method[] getMethods()获取的是class文件中的所有公共成员方法,包括继承的
					// Method类是描述成员方法的对象
					/*Method[] methods = c.getMethods();
					for(Method m : methods){
						System.out.println(m);
					}*/
					
					//获取指定的方法eat运行
					// Method getMethod(String methodName,Class...c)
					// methodName获取的方法名  c 方法的参数列表
					Method method = c.getMethod("eat");
					//使用Method类中的方法,运行获取到的方法eat
					//Object invoke(Object obj, Object...o)
					method.invoke(obj);
				}
			}

	* I. 反射获取有参数成员方法并运行
		* a. 获取有参数成员方法
			* 得到公共的成员方法
				public Method getMethod(String name, Class<?>... parameterTypes) 
					返回一个 Method 对象，它反映此 Class 对象所表示的类或接口的指定公共成员方法。 
				public Method[] getMethods()
					返回一个包含某些 Method 对象的数组，这些对象反映此 Class对象所表示的类或接口（包括那些由该类或接口声明的以及从超类和超接口继承的那些的类或接口）的公共 member 方法。
			* 得到全部的成员方法(包括私有的，如果要使用私有成员方法，要先进行public void setAccessible(boolean flag) 设置。)
				public Method getDeclaredMethod(String name, Class<?>... parameterTypes) 
					返回一个 Method 对象，该对象反映此 Class 对象所表示的类或接口的指定已声明方法。 
				public Method[] getDeclaredMethods() 
					返回 Method 对象的一个数组，这些对象反映此 Class 对象表示的类或接口声明的所有方法，包括公共、保护、默认（包）访问和私有方法，但不包括继承的方法。 
		* b. 使用Method方法对象
			public Object invoke(Object obj, Object... args) 
				对带有指定参数的指定对象调用由此 Method 对象表示的底层方法。 
				obj 指的是调这个方法的对象。
				args 指的是调用这个方法所要用到的参数列表。
				返回值Object就是方法的返回对象。如果方法没有返回值 ，返回的是null.
		* c. 反射获取有参数成员方法并运行代码演示
			package cn.itcast.demo1;
			import java.lang.reflect.Method;

			/*
			 *  反射获取有参数的成员方法并执行
			 *  public void sleep(String,int,double){}
			 */
			public class ReflectDemo7 {
				public static void main(String[] args) throws Exception{
					Class c = Class.forName("cn.itcast.demo1.Person");
					Object obj = c.newInstance();
					//调用Class类的方法getMethod获取指定的方法sleep
					Method method = c.getMethod("sleep", String.class,int.class,double.class);
					//调用Method类的方法invoke运行sleep方法
					method.invoke(obj, "休眠",100,888.99);
				}
			}
	* J. 反射泛型擦除
		* a. 使用情况
			例如：在泛型为String的集合里，添加Integer的数据
			ArrayList<String> list = new ArrayList<String>();
			list.add(100);
		* b. 能用泛型擦除的理论
			伪泛型：在编译后的.class文件里面是没有泛型的。类型为Object。
			用反射的方法绕过编译，得到Class文件对象，直接调用add方法。
		* c. 反射泛型擦除的代码演示
			package cn.itcast.demo2;
			import java.lang.reflect.Method;
			import java.util.ArrayList;

			/*
			 *   定义集合类,泛型String
			 *   要求向集合中添加Integer类型
			 *   
			 *   反射方式,获取出集合ArrayList类的class文件对象
			 *   通过class文件对象,调用add方法
			 *   
			 *   对反射调用方法是否理解
			 */
			public class ReflectTest {
				public static void main(String[] args)throws Exception {
					ArrayList<String> array  = new ArrayList<String>();
					array.add("a");
					//反射方式,获取出集合ArrayList类的class文件对象
					Class c = array.getClass();
					//获取ArrayList.class文件中的方法add
					Method method = c.getMethod("add",Object.class);
					//使用invoke运行ArrayList方法add
					method.invoke(array, 150);
					method.invoke(array, 1500);
					method.invoke(array, 15000);
					System.out.println(array);
					
					
				}
			}
	* K. 反射通过配置文件来决定运行的步骤
		* a. 操作依据
				通过配置文件得到类名和要运行的方法名,用反射的操作类名得到对象和调用方法
		* b. 实现步骤:
			 *    1. 准备配置文件,键值对
			 *    2. IO流读取配置文件  Reader
			 *    3. 文件中的键值对存储到集合中 Properties
			 *        集合保存的键值对,就是类名和方法名
			 *    4. 反射获取指定类的class文件对象
			 *    5. class文件对象,获取指定的方法
			 *    6. 运行方法
		* c. 代码演示
			代码：
			package cn.itcast.demo3;

			import java.io.FileReader;
			import java.lang.reflect.Method;
			import java.util.Properties;

			/*
			 *  调用Person方法,调用Student方法,调用Worker方法
			 *  类不清楚,方法也不清楚
			 *  通过配置文件实现此功能
			 *    运行的类名和方法名字,以键值对的形式,写在文本中
			 *    运行哪个类,读取配置文件即可
			 *  实现步骤:
			 *    1. 准备配置文件,键值对
			 *    2. IO流读取配置文件  Reader
			 *    3. 文件中的键值对存储到集合中 Properties
			 *        集合保存的键值对,就是类名和方法名
			 *    4. 反射获取指定类的class文件对象
			 *    5. class文件对象,获取指定的方法
			 *    6. 运行方法
			 */
			public class Test {
				public static void main(String[] args) throws Exception{
					//IO流读取配置文件
					FileReader r = new FileReader("config.properties");
					//创建集合对象
					Properties pro = new Properties();
					//调用集合方法load,传递流对象
					pro.load(r);
					r.close();
					//通过键获取值
					String className = pro.getProperty("className");
					String methodName = pro.getProperty("methodName");
					//反射获取指定类的class文件对象
					Class c = Class.forName(className);
					Object obj = c.newInstance();
					//获取指定的方法名
					Method method = c.getMethod(methodName);
					method.invoke(obj);
				}
			}
			配置文件：
			#className=cn.itcast.demo3.Student
			#methodName=study
			className=cn.itcast.demo3.Person
			methodName=eat
			#className=cn.itcast.demo3.Worker
			#methodName=job
		
### 3总结
* 把今天的知识点总结一遍。
