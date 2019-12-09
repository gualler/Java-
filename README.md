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


五，核心代码
package bs;
import javax.swing.JFrame;
import javax.swing.JScrollPane;
import javax.swing.JTable;
import javax.swing.table.TableColumn;
 
public class XueShengMingDanUI extends JFrame 
{ 
 
 public XueShengMingDanUI() 
 { 
  intiComponent(); 
 } 
 
  //初始化窗体组件 
 private void intiComponent() 
 { 
  // 设置JTable的列名 
  String[] columnNames = 
  { "学号","姓名", "专业", "班级"}; 
  Object[][] obj=new Object[7][7]; 
  for (int i=0;i<7;i++) 
  { 
   for(int j=0;j<7;j++) 
   { 
    switch (j) 
    { 
    case 0: 
     obj[0][0] = "  14140301";
     obj[0][1] = "    王小明"; 
     obj[0][2] = "   通信工程"; 
     obj[0][3] = "     2"; 
     break; 
    case 1: 
     obj[1][0] = "  14140302";
     obj[1][1] = "   王雷"; 
     obj[1][2] = "   通信工程"; 
     obj[1][3] = "     2"; 
     break; 
    case 2: 
     obj[2][0] = "  14140303";
     obj[2][1] = "   李芳"; 
     obj[2][2] = "   通信工程"; 
     obj[2][3] = "     2"; 
     break; 
    case 3: 
     obj[3][0] = "  14140304";
     obj[3][1] = "   张三"; 
     obj[3][2] = "   通信工程"; 
     obj[3][3] = "     2";     
     break; 
    case 4: 
     obj[4][0] = "  14140305";
     obj[4][1] = "   李四"; 
     obj[4][2] = "   通信工程"; 
     obj[4][3] = "     2"; 
     break; 
    case 5: 
     obj[5][0] = "  14140306";
     obj[5][1] = "   文宇"; 
     obj[5][2] = "   通信工程"; 
     obj[5][3] = "    2"; 
     break; 
    case 6: 
     obj[6][0] = "  14140307";
     obj[6][1] = "   王飞"; 
     obj[6][2] = "   通信工程"; 
     obj[6][3] = "     2";     
     break; 
 
    } 
   } 
  } 
 
  JTable table=new JTable(obj, columnNames); //JTable的其中一种构造方法 
  TableColumn column=null;     //设置JTable的列默认的宽度和高度 
  int colunms = table.getColumnCount(); 
  for(int i=0;i<colunms;i++) 
  { 
   column = table.getColumnModel().getColumn(i); 
   column.setPreferredWidth(100);   //将每一列的默认宽度设置为100
  } 
  table.setAutoResizeMode(JTable.AUTO_RESIZE_OFF); //设置JTable自动调整列表的状态，此处设置为关闭     
  JScrollPane scroll = new JScrollPane(table); //用JScrollPane装载JTable，这样超出范围的列就可以通过滚动条来查看 
  scroll.setSize(300, 50);   
 
  add(scroll); 
 
  this.setTitle("张健-学生成绩管理系统"); 
  this.setLocation(450, 200); 
  this.setVisible(true); 
  this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE); 
  this.pack(); 
 } 
 
 public static void main(String[] args) 
 { 
  new XueShengMingDanUI(); 
 } 
} 

六，编写感悟
这是这学期最后的一次实验，十分的折磨人，我感觉比较难！还是因为没学精吧。并且需要将前面所学的知识全部都用到。来来回回写了很多回，但是最终就是运行不出来！实在是没办法了。
