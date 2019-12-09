大数据181-2018310996-张健
Java最后一次实验，完善学生选课系统。
一、实验目的

分析学生选课系统的数据结构并且将文件中的数据以字符串形式读出；使用GUI窗体及其组件设计窗体界面让数据可视性更强同时完成读取和写入的功能；完成学生选课过程业务逻辑编程，实现选课退课开课的功能；基于文件保存并读取数据，新建文本文件，将文本文件中的数据在GUI中显示；处理异常，防止文件中出现空白字符。

二、实验要求

1，内容：设计GUI架构，支持学生注册，课程新加，学生选课，学生退课，打印学生选课列表等操作。2，基于事件模型对业务逻辑编程，实现在界面上支持上述操作。3，针对操作过程中可能会出现的各种异常，做异常处理4，基于输入/输出编程，支持学生，课程，教师等数据的读写操作。5，基于Github.com提交实验，包括实验SRC源文件夹程序，README.MD实验报告文档。

三，实验过程
调用之前的学生选课系统的源代码和选课系统GUI的代码，在此基础上添加文件读取和写入操作。新建New Exception类用于排除文本文件空字符异常。在Gui类中将需要的文本读取和写入代码加入其中，在实例化Majorattribute类的参数时，通过文本读取的方法，转化为字符串，以“,”分隔后按顺序写入Majorattribute类的实例化中，在Gui类执行时调用，用以替代在代码内实例化的操作。在设置学生姓名、学号以及各个数据后，单击“确定”键，在GUI中的文本框得到数据的实例化体现，同时应用文件写入代码，将字符串写入文本文件中。

四，流程图
![流程图](https://github.com/gualler/Java-/blob/master/798bf3889c9979ee6362052948ce06d.png)
