## C# Programming Basics



### .NET Framework

.NET框架（.NET Framework） 是由微软开发，一个致力于**敏捷软件开发**（Agile softwaredevelopment）、**快速应用开发**（Rapidapplication development）、**平台无关性和网络透明化的软件开发平台**。.NET是微软为下一个十年对**服务器**和**桌面型软件工程**迈出的第一步。.NET包含许多有助于**互联网**和内部网应用迅捷开发的技术。

Microsoft .NET Framework是用于**Windows**的新托管代码编程模型。. 它将强大的功能与新技术结合起来，用于构建具有视觉上引人注目的**用户体验的应用程序**，实现跨技术边界的无缝通信，并且能支持各种业务流程。

目的：使得建立Web Services以及因特网应用程序的工作变的简单。

.net框架的基本特点：

1. .NET的运行环境
2. 拥有基类库（BCL）和**框架类库（FCL）**
3. 支持**C#**、Python等Languages
5. **OS支持Windows/Linux**

### C# Introduction

C# 是一个现代的、通用的、面向对象的编程语言，它是由微软（Microsoft）开发的。

C# 是专为公共语言基础结构（CLI）设计的。CLI 由可执行代码和运行时环境组成，允许在不同的计算机平台和体系结构上使用各种高级语言。

C# 成为一种广泛应用的专业语言的原因：

- 现代的、通用的编程语言。
- 面向对象。
- 面向组件。
- 容易学习。
- 结构化语言。
- 它产生高效率的程序。
- 它可以在多种计算机平台上编译。
- .Net 框架的一部分。

C# 一些重要的功能：

- 布尔条件（Boolean Conditions）
- 自动垃圾回收（Automatic Garbage Collection）
- 标准库（Standard Library）
- 组件版本（Assembly Versioning）
- 属性（Properties）和事件（Events）
- 委托（Delegates）和事件管理（Events Management）
- 易于使用的泛型（Generics）
- 索引器（Indexers）
- 条件编译（Conditional Compilation）
- 简单的多线程（Multithreading）
- LINQ 和 Lambda 表达式
- 集成 Windows

**C#一般使用Visual Studio作为其集成开发环境**

虽然 .NET 框架是运行在 Windows 操作系统上，但是也有一些运行于其它操作系统上的版本可供选择。**Mono** 是 .NET 框架的一个开源版本，它包含了一个 C# 编译器，且可运行于多种操作系统上，比如各种版本的 **Linux 和 Mac OS**。

### C# Basic Topics

```C#
//简易C#程序主要包括以下部分
using System;	//using 关键字用于在程序中包含命名空间。一个程序可以包含多个 using 语句。
namespace HelloWorldApplication	//命名空间声明
{
    class HelloWorld	//class
    {
        public const int first;	//Class方法
        public int second()	//Class属性
        {
            //......
        }
        
        static void Main(string[] args)	//Main方法
        {
            /* 我的第一个 C# 程序 */	//注释
            Console.WriteLine("Hello World!");	//语句 & 表达式
            Console.ReadKey();
        }
    }
}
```

C# 文件的后缀为 **.cs**。

#### Value Types

1. Int占4字节
1. Float占4字节
1. Double占8字节
2. 赋初始值值时需要注意：0—>整形、0L—>长整形、0.0F—>Float、0.0D—>Double

#### Input

```C#
Console.Read();	//char
Console.ReadLine();	//line
```

#### Output

```c#
Console.Write(a);
Console.Write("{0} + {1} = {2}.", a, b, a + b);
Console.Write("{name} was born in {year}.");
```

#### For循环

```C#
//此处只介绍foreach
foreach (var element in fibarray)	//C#中的var类似于C++中的auto
{
	count += 1;
	System.Console.WriteLine("Element #{0}: {1}", count, element);
}
```

#### 可空类型

```C#
//? 单问号用于对 int、double、bool 等无法直接赋值为 null 的数据类型进行 null 的赋值
//意思是这个数据类型是 Nullable 类型的
int? i = 3;	//i = 3;
int i;	//默认值0;
int? ii;	//默认值null
```

#### 合并运算符？？

```C#
//如果第一个操作数的值为 null，则运算符返回第二个操作数的值，否则返回第一个操作数的值。
double? num1 = null;
double num3;
num3 = num1 ?? 5.34;      // num1 如果为空值则返回 5.34
Console.WriteLine("num3 的值： {0}", num3);
```

#### TryParse

```C#
if (int.TryParse(str, out number))
```

#### C# 类型转换

```C#
//同样与C++类似
//隐式类型转换 - 这些转换是 C# 默认的以安全方式进行的转换, 不会导致数据丢失
//例如，从小的整数类型转换为大的整数类型，从派生类转换为基类。
int i = 5;
long l = i;	//隐式转换

//显式类型转换 - 显式类型转换，即强制类型转换。
//显式转换需要强制转换运算符，而且强制转换会造成数据丢失。
long l = 5;
int i = (int) l;	//显式转换（强制转换）

//常见使用的C#类型转换方法
a.ToChar();	//字节类型
a.ToDouble();	//双精度浮点
a.ToInt32();	//32bit整型
a.ToString();	//字符串类型
```

#### 条件分支语句

```C#
switch (day)
{
    case 1: ...; break;
    case 2: ...; break;
    default: ...; break;
}
```

### C# Advanced Topics

#### Arrays

```C#
int[] number = new int[10];	//分配10个整型的数组
string[] names = { "Peter", "222", "333" };
foreach (var name in names)
{
    Console.WriteLine(name);
}
string[,] matrix = new string[height, wifth];	//二维数组
```

#### List

```C#
List<int> numbers = new List<int>();
numbers.Add(5);
numbers.Insert(3, 1);
numbers.RemoveAt(0);
```

#### Dictionary

```C#
Dictionary<string, string> phonebook = new Dictionary<string, string>();
phonebook["a"] = "111";
phonebook.Remove("a");
```

#### String

```C#
System.String
    
int ret = string.Compare(str1, str2, true);
// ret = 0 -> str1 epuals to str2
// ret < 0 -> str1 is before to str2
//指排列顺序中的相对位置

//比较字符串是否相等
str1 == str2 || str1.Equals(str2);
//对于值类型来说是无差别的，如果对象的值相等则返回true；而对于string以外的引用而言（string类型做过优化），==是比较栈区的两个地址是否相同；而Epuals是比较栈区对应地址指针所指的值是否相等
    
//字符串之间可以使用 + 或者 += 拼接
    
str.IndexOf(string term);	//返回字符串第一次出现的位置 or -1
str.LastIndexOf(string term);	//返回字符串最后一次出现的位置 or -1
    
str.Substring(int startIndex, int length);
str.Substring(int startIndex);
//同C++的substr一样

string[] Split(params char[] separator)
//分隔符，按照参数中的分隔符分割字符串
//返回一个字符串数组
    
str.Replace(string match, string term)
//将str中的match都替换为term
    
str.Remove(int index, int length)
//删除str中的一部分，index是开始部分；length是长度
    
str.ToLower();	//更换为小写
str.ToUpper();	//大写
    
str.Trim();	//去掉str两端的空格
str.Trim(params char[] chars);	//在其中添加其它字符在两边删掉

如果对字符串操作比较多的话，建议使用StringBuilder
StringBuilder出现的原因：string本身是不可改变的，它只能赋值一次，每一次内容发生改变，都会经历一个析构、重新构建生成一个新的对象，而每一次生成新对象都会对系统性能产生影响，这会降低.NET编译器的工作效率。StringBuilder类则不同，每次操作都是对自身对象进行操作，而不是生成新的对象，其所占空间会随着内容的增加而扩充，这样，在做大量的修改操作时，不会因生成大量匿名对象而影响系统性能。

StringBuilder sb = new StringBuilder("Hello World!", 25);
sb.Append(string str1);	//添加str1至sb尾部
sb.Remove(int startIndex, int length);
sb.Insert(int position, string str2);	//在position位置插入str2
sb.Replace(string str1, string str2);	//用str2替换str1
sb.ToString();	//将StringBuilder转换为string类型
```

#### Struct

```C#
struct Books
{
   public string title;
   public string author;
   public string subject;
   public int book_id;
};
```

#### Class

```C#
class Point
{
    public int X { get; set; }	//可读可写
    public int Y { get; set; }	
}
Point[] people = new Point[]
{
    new Point() { X = 1, Y = 2 },
};

//类 vs 结构
//类是引用类型，结构是值类型。（根本区别）
//结构不支持继承。
//结构不能声明默认的构造函数。
//结构体中声明的字段无法赋予初值，类可以
//结构体的构造函数中，必须为结构体所有字段赋值，类的构造函数无此限制

//类的构造函数和析构函数示例
class Line
{
    private double length;   // 线条的长度
    public Line()
    {
        Console.WriteLine("对象已创建");
    }
    ~Line() //析构函数
    {
        Console.WriteLine("对象已删除");
    }
    static void Main(string[] args)
    {
        Line line = new Line();    
    }
}
```

#### Enum

```C#
//直接上程序样例
using System;

public class EnumTest
{
    enum Day { Sun, Mon, Tue, Wed, Thu, Fri, Sat };

    static void Main()
    {
        int x = (int)Day.Sun;
        int y = (int)Day.Fri;
        Console.WriteLine("Sun = {0}", x);
        Console.WriteLine("Fri = {0}", y);
    }
}

//产生结果如下：
//Sun = 0
//Fri = 5
```



#### Stacks and Queues

```C#
Stack<T>
// Count
// Pop()
// Push()
// ToArray() 将stack变为array
// Contains() 判断一个元素是否在stack中
Queue<T>
// Enqueue() 添加一个元素至队尾
// Dequeue() 移除一个元素并返回它
// 剩下和Stack一样
```

#### Sets and Dictionaries

Set和List的区别：List多数都是有序的（添加的顺序）

```
HashSet<T> //无序
SortedSet<T> //有序

Dictionary<key, value>
SortedDictionary<key, value>
ContainsKey() //检查key
ContainsValue() //检查value
TryGetValue() //检查key并返回value
```

#### Files and Directories

```C#
ReadAllText()	//读所有行最后组成一个字符串返回
ReadAllLines()	//读所有行每行组成一个字符串，返回字符串数组
    
CreateDirectory()	//创建一个目录
Delete()
Move()
GetFiles()
```

#### Exceptions（异常处理）

```C#
System.Exception

try
{
   // 引起异常的语句
}
catch( ExceptionName e1 )
{
   // 错误处理代码
}
catch( ExceptionName e2 )
{
   // 错误处理代码
}
catch( ExceptionName eN )
{
   // 错误处理代码
}
finally
{
   // 要执行的语句
}
```

抛出对象

如果异常是直接或间接派生自 **System.Exception** 类，您可以抛出一个对象。您可以在 catch 块中使用 throw 语句来抛出当前的对象，如下所示：

```C#
Catch(Exception e)
{
   //...
   Throw e
}
```



#### Using

```C#
using (//引导使用的资源)
{
    //使用资源
}//自动释放资源 
```

#### 正则表达式

参考python3与NLP笔记即可（纯懒）

#### 匿名类型与方法扩展

匿名类型就是不用给起名字

#### 委托

（1） 从数据结构来讲，委托是和类一样是一种用户自定义**类型**。

（2） 从设计模式来讲，委托（类）提供了**方法**（对象）的抽象。

委托是方法的抽象，它存储的就是一系列具有相同签名和返回回类型的方法的地址。调用委托的时候，委托包含的所有方法将被执行。

委托的定义

```C#
//委托的定义
delegate void MyDel(int x);

//声明委托变量
MyDel del1, del2;

//初始化（两种方式）
del1 = new MyDel( myInstObj.MyM1 );	//使用new运算符
del1 = myInstObj.MyM1;	//隐式转换

//委托的赋值
//由于委托是引用类型，我们可以通过给它赋值来改变包含在委托变量中的方法地址引用。旧的引用会被垃圾回收器回收。
MyDel del;
del = myInstaObj.MyM1; //委托初始化
del = SClass.OtherM2;//委托重新赋值，旧的引用将被回收

//委托的运算
//可以通过 += 和 -= 运算符新增或移除方法
MyDel del = myObj.MyMethod;
del += SClass.OtherM2; // 增加方法
del -= myObj.MyMethod; // 移除方法

//委托调用
//委托调用跟方法调用类似。委托调用后，调用列表的每个方法将会被执行。
//在调用委托前，应判断委托是否为空。调用空委托会抛出异常。
if(null != del)	
{	
    del();//委托调用	
}
                 
//匿名方法
//匿名方法是在初始化委托时内联声明的方法。
delegate int MyDel (int x); //定义一个委托 

MyDel del = delegate( int x){ return x; };
//匿名方法是不会显示声明返回值的。
```

#### Lambda 表达式

Lambda表达式主要用来简化匿名方法的语法。在匿名方法中，delegate关键字有点多余，因为编译器已经知道我们将方法赋值给委托。通过几个简单步骤，我们就可以将匿名方法转换为Lambda表达式

```C#
//删除delegate关键字
//在参数列表和匿名方法主体之间防Lambda运算符=>。Lambda运算符读作"goes to"

MyDel del = delegate( int x) { return x; };//匿名方法
MyDel del2 = (int x) => {return x;};//Lambda表达式
MyDel del3 = x => {return x};//简写的Lambda表达式
```

**Lambda 表达式是一个匿名函数，是一个未命名的方法来代替一个委托实例，用它可以高效简化代码，常用作委托，回调**

**Lambda 表达式都使用运算符`=>`，所以当你见到这个符号，基本上就是一个 Lambda 表达式**

**Lambda 运算符的左边是输入参数()，`=>`，右边是表达式或语句块**

对于lambda表达式的参数，如果只有一个参数可以直接写，若多个参数则需要添加括号

```C#
x => x * x;
(x, y) => x == y;
```

lambda表达式最常用于Func和Action委托，当然现在最常用的都是Func

##### Action中使用Lambda表达式

```C#
//在Action中无返回值
Action<string> print = message => Console.WriteLine(message);
```

##### Func中使用Lambda表达式

```C#
//Func中最后一个参数是return
Func<int, int> increment = number => number + 1;
int a = increment(5);
int b = increment(a);
```

##### Predicate中使用Lambda表达式

```C#
//Predicate是特殊的Func，只能返回bool型变量，只能有一个形参
//其余与Func相同
```

#### LINQ

LINQ（Language Integrated Query )语言集成查询，是一组用于C#和VB语言的拓展，它允许VB或者C#代码以操作内存数据的方式，查询数据库。

LINQ有两种语法形式

```C#
//一：查询语句，类似SQL
Int[] nums={1,2,4,5,6,7};·//数据源
Var list=from a in nums
        Where a%2==0
        Orderby a descending
        Select a;
//必须以from开头。以select或者group by结尾
//结尾select 查出这个筛选之后的a。当然也可以使用匿名对象或者新的已构造的对象
//注意：select只能返回单个属性，如果需要返回多个属性则需要使用new构造匿名对象
//常见字句：
//from子句：指定查询操作的数据源和范围变量
//where子句：筛选元素的逻辑条件，返回值是一个bool类型
//select子句：指定查询结果的类型和表现形式
//orderby子句：对查询结果进行排序（升序或者降序）
//group子句：对查询结果进行分组
//into子句：提供一个临时标识符，该表示可充当对join/group/select子句结果的引用
//join子句：连接多个查询操作的数据源
//let子句：引入用于存储查询表达式中的子表达式结果的范围变量


//二：方法语法
//常见方法有：
//Count（）
//Where（）
//OrderBy（）【默认是升序】OrderByDescending()、
//Select（）
//GroupBy（）
//方法语法中一般结合lambda表达式（委托delegate和匿名的结合）来使用
//比如上述的Where(a => a.Length == 3)。
```

#### 并发（异步式）编程

同步程序的缺点：

##### Thread 和 Task

线程锁

泛型任务

async 和 await

操作系统当中如何实现多线程

#### 定义类（class）

```C#
class Line
   {
      private double length;   // 线条的长度
      public Line(double len)  // 参数化构造函数
      {
         Console.WriteLine("对象已创建，length = {0}", len);
         length = len;
      }

      public void setLength( double len )
      {
         length = len;
      }
      public double getLength()
      {
         return length;
      }

      static void Main(string[] args)
      {
         Line line = new Line(10.0);
         Console.WriteLine("线条的长度： {0}", line.getLength()); 
         // 设置线条长度
         line.setLength(6.0);
         Console.WriteLine("线条的长度： {0}", line.getLength()); 
         Console.ReadKey();
      }
   }
```

##### 方法

```C#
//方法实例
class NumberManipulator
{
   public int FindMax(int num1, int num2)
   {
      /* 局部变量声明 */
      int result;

      if (num1 > num2)
         result = num1;
      else
         result = num2;

      return result;
   }
   //...
}

//修饰词params
//params是一个计算机函数，表示函数的参数是可变个数的，即可变的方法参数，用于表示类型相同，但参数数量不确定。

//用法1：要实现调用方法时想放多个（任意个数）的实参，那么形参就要用params关键字修饰，并且后边跟一个数组，表示是一个可变数量的、同类型的数组参数。
public static void Show(params string[] strs )//params修饰的string类型的形参数组
{
    
}
//用法2：若有多个类型的参数，则params修饰的参数数组要放到最后，并且只使用一次
public static void Show(int a,params string[]strs )
//此时Show方法中有两个形参，一是int类型的形参a，而是params修饰的string类型的形参数组
{
 
}
//用法3：如果想要这个形参数组可以传“不同”类型的，则可以写成object类型
public static void Show(params object[]strs )
//此时Show方法中一个形参params修饰的object类型的形参数组，object可以是任何类型
{
    
}
//params使用注意事项：
//若形参表中含一个参数数组（params形参数组），则该参数数组必须位于形参列表的最后，并且只能使用一次。即在方法声明中的 params 关键字之后不允许任何其他参数，并且在方法声明中只允许一个 params 关键字。
//参数数组必须是一维数组；
//不允许将params修饰符与ref和out修饰符组合起来使用；
//params修饰的参数数组，可以为任何类型，只要设置数组类型为object就可以。
//若实参是数组则按引用传递，若实参是变量或表达式则按值传递。
//C#语法规定，params后边必定跟数组。作用是把不定数量的、同类型的参数装入这个数组中。


//修饰符ref
//ref用作使用引用参数，必须在方法的声明和调用中都使用ref修饰符
//实参必须是变量，不能携带常量，在用作实参前必须被赋值，如果是引用类型变量，可以赋值为一个引用或者null值
static void FuncData(float value )
{                                
    int temp=0;           //实参变量
    FuncData(ref temp);   //包含修饰符ref
    //FuncData(ref temp+1); //错误，必须使用变量
}


//修饰符out
//out用作输出参数，输出参数在方法内部读取之前要必须经过一次赋值操作，并且在函数结束之前必须要进行一次赋值
static void FuncTest(out int value)
{
	var test = value+1;//错误，在方法赋值之前无法读取输出变量
}
```

##### 静态成员

（1）静态成员是class当中的属性或能力，而不是对于成员来说的，其用于对静态字段、只读字段等的初始化。 　 　 　 　 　 　 　

（2）添加static关键字，不能添加访问修饰符（private、public等），因为静态构造函数都是私有的。 　 　 　

（3）类的静态构造函数在给定应用程序域中至多执行一次：只有创建类的实例或者引用类的任何静态成员才激发静态构造函数

（4）静态构造函数是不可继承的，而且不能被直接调用。 　 　 　 　 　 　

（5）如果类中包含用来开始执行的 Main 方法，则该类的静态构造函数将在调用 Main 方法之前执行。任何带有初始值设定项的静态字段，则在执行该类的静态构造函数时，先要按照文本顺序执行那些初始值设定项。 　

（6）如果没有编写静态构造函数，而这时类中包含带有初始值设定的静态字段，那么编译器会自动生成默认的静态构造函数。

##### 静态类与静态方法的关系

静态类：

如果一个类，被声明为静态类，那么该类不可以被实例化，也不可以被继承，同时不可以包含非静态成员。
非静态类中，可以包含静态成员。

静态方法：

静态方法中，不可以访问非静态**成员**（object），也不可以使用this。
非静态方法中，可以调用静态和非静态成员。

#### 封装

优点：降低复杂度、**隐藏内部实现细节**、修改时无需修改客户端代码

五种访问修饰符以及其作用范围

```C#
public //公有访问。不受任何限制。
private //私有访问。只限于本类成员访问，子类，实例都不能访问。
protected //保护访问。只限于本类和子类访问，实例不能访问。
internal //内部访问。只限于本项目内访问，其他不能访问。
protected internal //内部保护访问。只限于本项目或是子类访问，其他不能访问
```

**在实现方法时，若该方法是用于实现接口，一般会设置为public；若该方法用于类的内部使用，则一般会设置为private**

#### 继承

思想：当我们定义了多个类，这多个类都存在重复的成员(共性)。**我们可以将这些重复的成员单独的提取封装到一个类中，作为这些具有相同特征类的父类。**

一般可以使用UML来画类图，描述其依赖关系

继承的好处：

1. 扩展性变强（多态）
2. 重用已有的类，只需对对应的结构和类型做更改即可
3. 提供了抽象，子类只需关注自己是如何实现的，而不用关注父类（基类）

注意：private成员被隐藏，不能继承

在子类中可以重写父类的方法，编译器默认调用子类方法

一个类可以派生自多个类或接口，这意味着它可以从多个基类或接口继承数据和函数。

##### 单继承

```C#
class <基类>
{
 ...
}
class <派生类> : <基类>
{
 ...
}
```

##### 多重继承

多重继承指的是一个类别可以同时从多于一个父类继承行为与特征的功能。与单一继承相对，单一继承指一个类别只可以继承自一个父类。

**C# 不支持多重继承**。但是，您可以使用接口来实现多重继承。下面的程序演示了这点：

```C#
using System;
namespace InheritanceApplication
{
   class Shape
   {
      public void setWidth(int w)
      {
         width = w;
      }
      public void setHeight(int h)
      {
         height = h;
      }
      protected int width;
      protected int height;
   }

   // 基类 PaintCost
   public interface PaintCost
   {
      int getCost(int area);

   }
   // 派生类
   class Rectangle : Shape, PaintCost
   {
      public int getArea()
      {
         return (width * height);
      }
      public int getCost(int area)
      {
         return area * 70;
      }
   }
   class RectangleTester
   {
      static void Main(string[] args)
      {
         Rectangle Rect = new Rectangle();
         int area;
         Rect.setWidth(5);
         Rect.setHeight(7);
         area = Rect.getArea();
         // 打印对象的面积
         Console.WriteLine("总面积： {0}",  Rect.getArea());
         Console.WriteLine("油漆总成本： ${0}" , Rect.getCost(area));
         Console.ReadKey();
      }
   }
}

//输出
//总面积：35
//油漆总成本：$2450
```



#### 多态性

**多态是同一个行为具有多个不同表现形式或形态的能力。**

##### 静态多态性

在编译时，函数和对象的连接机制被称为早期绑定，也被称为静态绑定。C# 提供了两种技术来实现静态多态性。分别为：

- 函数重载
- 运算符重载

函数重载

您可以在同一个范围内对相同的函数名有多个定义。函数的定义必须彼此不同，可以是参数列表中的参数类型不同，也可以是参数个数不同。不能重载只有返回类型不同的函数声明。

```C#
using System;
namespace PolymorphismApplication
{
    public class TestData  
    {  
        public int Add(int a, int b, int c)  
        {  
            return a + b + c;  
        }  
        public int Add(int a, int b)  
        {  
            return a + b;  
        }  
    }  
    class Program  
    {  
        static void Main(string[] args)  
        {  
            TestData dataClass = new TestData();
            int add1 = dataClass.Add(1, 2);  
            int add2 = dataClass.Add(1, 2, 3);

            Console.WriteLine("add1 :" + add1);
            Console.WriteLine("add2 :" + add2);  
        }  
    }  
}
```

运算符重载

```C#
//重载运算符是具有特殊名称的函数，是通过关键字 operator 后跟运算符的符号来定义的。
//与其他函数一样，重载运算符有返回类型和参数列表。

//对于重载运算符样例
//public + static + return类型 + operator + 要重载的运算符 + 两个参数
public static Box operator+ (Box b, Box c)
{
   Box box = new Box();
   box.length = b.length + c.length;
   box.breadth = b.breadth + c.breadth;
   box.height = b.height + c.height;
   return box;
}
```



##### **动态多态性**

动态多态性是通过抽象类和虚方法来实现的。

C# 允许您使用关键字 **abstract** 创建抽象类，用于提供接口的部分类的实现。当一个派生类继承自该抽象类时，实现即完成。**抽象类**包含抽象方法，抽象方法可被派生类实现。派生类具有更专业的功能。

抽象类的注意事项：

- 不能创建一个抽象类的实例。
- 不能在一个抽象类外部声明一个抽象方法。
- 通过在类定义前面放置关键字 **sealed**，可以将类声明为**密封类**。当一个类被声明为 **sealed** 时，它不能被继承。抽象类不能被声明为 sealed。

```C#
//抽象类样例代码
using System;
namespace PolymorphismApplication
{
   abstract class Shape
   {
       abstract public int area();
   }
   class Rectangle:  Shape
   {
      private int length;
      private int width;
      public Rectangle( int a=0, int b=0)
      {
         length = a;
         width = b;
      }
      public override int area ()
      {
         Console.WriteLine("Rectangle 类的面积：");
         return (width * length);
      }
   }

   class RectangleTester
   {
      static void Main(string[] args)
      {
         Rectangle r = new Rectangle(10, 7);
         double a = r.area();
         Console.WriteLine("面积： {0}",a);
         Console.ReadKey();
      }
   }
}
```



**虚方法**

当有一个定义在类中的函数需要在继承类中实现时，可以使用**虚方法**。

**虚方法，可以理解为 “一个不完整”/“可以扩展” 的方法**

**Virtual (虚)与 Override (重写) 是同时出现的**

**在子类中，重写 Override (重写)虚方法时，父类中的函数才会被重写（必须是Virtual + Override）**

**在子类中，重写时，写明了 base ，并重写时，子类基于父类函数进行扩展**

```C#
using System;
using System.Collections.Generic;

public class Shape
{
    public int X { get; private set; }
    public int Y { get; private set; }
    public int Height { get; set; }
    public int Width { get; set; }
   
    // 虚方法
    public virtual void Draw()
    {
        Console.WriteLine("执行基类的画图任务");
    }
}

class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("画一个圆形");
        base.Draw();
    }
}
class Rectangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("画一个长方形");
        base.Draw();
    }
}
class Triangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("画一个三角形");
        base.Draw();
    }
}

class Program
{
    static void Main(string[] args)
    {
        // 创建一个 List<Shape> 对象，并向该对象添加 Circle、Triangle 和 Rectangle
        var shapes = new List<Shape>
        {
            new Rectangle(),
            new Triangle(),
            new Circle()
        };

        // 使用 foreach 循环对该列表的派生类进行循环访问，并对其中的每个 Shape 对象调用 Draw 方法
        foreach (var shape in shapes)
        {
            shape.Draw();
        }

        Console.WriteLine("按下任意键退出。");
        Console.ReadKey();
    }

}

//运行结果：
//画一个长方形
//执行基类的画图任务
//画一个三角形
//执行基类的画图任务
//画一个圆形
//执行基类的画图任务
//按下任意键退出。
```

#### 接口

在 C# 语言中，类之间的继承关系仅支持单重继承，而接口是为了实现多重继承关系设计的。

接口本身并不实现任何功能，它只是和声明实现该接口的对象订立一个必须实现哪些行为的契约。

抽象类不能直接实例化，但允许派生出具体的，具有实际功能的类。

接口定义

```C#
//接口使用 interface 关键字声明，它与类的声明类似。接口声明默认是 public 的。
//下面是一个接口声明的实例：
using System;
 
namespace app
{
    interface IBook
    {
        int Id { get; set; }
        string Name { get; set; }
        double Price { get; set; }
        double SalePrice(int discount);
        //值得注意的是，该方法并没有具体的实现。
    }
}
```

接口实现

```C#
using System;

interface IMyInterface
{
        // 接口成员
    void MethodToImplement();
}

class InterfaceImplementer : IMyInterface
{
    static void Main()
    {
        InterfaceImplementer iImp = new InterfaceImplementer();
        iImp.MethodToImplement();
    }

    public void MethodToImplement()
    {
        Console.WriteLine("MethodToImplement() called.");
    }
}

//继承接口后，我们需要实现接口的方法, 方法名必须与接口定义的方法名一致。
```

接口继承

如果一个接口继承其他接口，那么实现类或结构就需要实现所有接口的成员。

```C#
using System;

interface IParentInterface
{
    void ParentInterfaceMethod();
}

interface IMyInterface : IParentInterface
{
    void MethodToImplement();
}

class InterfaceImplementer : IMyInterface
{
    static void Main()
    {
        InterfaceImplementer iImp = new InterfaceImplementer();
        iImp.MethodToImplement();
        iImp.ParentInterfaceMethod();
    }

    public void MethodToImplement()
    {
        Console.WriteLine("MethodToImplement() called.");
    }

    public void ParentInterfaceMethod()
    {
        Console.WriteLine("ParentInterfaceMethod() called.");
    }
}
```



#### 抽象

#### 命名空间

**空间的设计目的是一种命名空间**与其他名称提供开放方式。在一个命名空间中声明的名称与另一个命名空间中声明的相同类别的名称不冲突。参考计算机中文件的设置

```C#
//命名空间用法
using System;
namespace first_space
{
   class namespace_cl
   {
      public void func()
      {
         Console.WriteLine("Inside first_space");
      }
   }
}
namespace second_space
{
   class namespace_cl
   {
      public void func()
      {
         Console.WriteLine("Inside second_space");
      }
   }
}  
class TestClass
{
   static void Main(string[] args)
   {
      first_space.namespace_cl fc = new first_space.namespace_cl();
      second_space.namespace_cl sc = new second_space.namespace_cl();
      fc.func();
      sc.func();
      Console.ReadKey();
   }
}
```

**using关键字**

**using** 关键字表明程序使用的是给定命名空间中的名称。例如，我们在程序中使用 **System** 命名空间，其中定义了类 Console。我们可以只写：

```C#
Console.WriteLine ("Hello there");
.WriteLine ("Hello there");
```

我们可以写完全限定名称，如下：

```C#
System.Console.WriteLine("Hello there");
.Console.WriteLine("Hello there");
```

也可以使用 **using** 命名空间指令，这样在使用的时候就不用在前面加上命名空间名称。该指令告诉编译器随后的代码使用了指定命名空间中的名称。下面的代码演示了命名空间的应用。

使用 using 指定重写上面的实例如下：

```C#
using System;
using first_space;
using second_space;

namespace first_space
{
   class abc
   {
      public void func()
      {
         Console.WriteLine("Inside first_space");
      }
   }
}
namespace second_space
{
   class efg
   {
      public void func()
      {
         Console.WriteLine("Inside second_space");
      }
   }
}  
class TestClass
{
   static void Main(string[] args)
   {
      abc fc = new abc();
      efg sc = new efg();
      fc.func();
      sc.func();
      Console.ReadKey();
   }
}


//执行结果如下
//Inside first_space
//Inside second_space
```

嵌套命名空间

命名空间可以被嵌套，即您可以在一个命名空间内定义另一个命名空间，如下所示：

```C#
namespace namespace_name1 
{
   // 代码声明
   namespace namespace_name2 
   {
     // 代码声明
   }
}
```

可以使用点（.）运算符访问嵌套的命名空间的成员，如下所示：

```c#
using System;
using SomeNameSpace;
using SomeNameSpace.Nested;

namespace SomeNameSpace
{
    public class MyClass
    {
        static void Main()
        {
            Console.WriteLine("In SomeNameSpace");
            Nested.NestedNameSpaceClass.SayHello();
        }
    }

    // 内嵌命名空间
    namespace Nested  
    {
        public class NestedNameSpaceClass
        {
            public static void SayHello()
            {
                Console.WriteLine("In Nested");
            }
        }
    }
}
```

