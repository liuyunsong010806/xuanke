
# 阅读程序

## 一、实验目的<br></br>
### 基本要求
  - 初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
  + 掌握面向对象的类设计方法（属性、方法）；
  * 掌握类的继承用法，通过构造方法实例化对象；
  + 学会使用super()，用于实例化子类；
  - 掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。

### 附加要求：
1. 在测试主类中，实例化多个类实体，模拟学生选课操作、打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课教师 等）
2. 模拟学生退课操作，再打印课程信息。

## 二、实验过程
1. 首先创建四个类和一个主类
2. 将四个主类名字分别命名为People，然后用另外两个类Student，Teacher分别设置为People的子类，并用super（）将父类People中的编号、姓名、性别继承。在输出语句中用toString（）方法。
3. 随后在Test主类里面设置了教师信息、学生信息、课程信息。
4. 利用循环和import java.util.Scanner设置一个后台输入系统。通过识别输入的数字来确定学生所对应的授课课程和该课程的老师。
5. 在设计一些细节上的调整。比如没有该编号会输出未找到该课程；当学生选好课会将学生信息，授课老师信息，课程信息一起打印出来；退课必须确认之前选课编号才可以退课……



## 三、核心方法
> 将四个主类名字分别命名为People，然后用另外两个类Student，Teacher分别设置为People的子类，并用super（）将父类People中的编号、姓名、性别继承。在输出语句中用toString（）方法。
>>这是选课的一个小循环语句，将wuli，shuxue，yingyu的1，2，3选项来选择这三个。

```
int y = in.nextInt();        // Scanner 类来获取用户的输入
        System.out.println("请输入1,2,3进行选课: ");
        if (y == 1) {
            a = wuli;
            System.out.println("已选课: " + wuli);
            System.out.println(zhang);
        } else if (y == 2) {
            a = shuxue;
            System.out.println("已选课: " + shuxue);
            System.out.println(li);
        } else if (y == 3) {
            a = yingyu;
            System.out.println("已选课: " + yingyu);
            System.out.println(wang);
        } else {
            System.out.println("不含该课程");
        }

```
>>这一部分我用了toString（）的方法

```
 int course;
    Teacher (int number,String name,String sex,int course){
        super(number,name,sex);
        this.course=course;
    }
        public String toString (){
            return "教师号:"+number+"\t老师姓名："+name+"\t性别"+sex+"\t 所教课程："+course;
        }
```
## 四、流程图
![%E5%9B%BE%E7%89%871.png](https://github.com/liuyunsong010806/java-/blob/main/%E5%9B%BE%E7%89%871.png)

## 五、实验结果
![%E5%9B%BE%E7%89%872.png](https://github.com/liuyunsong010806/java-/blob/main/%E5%9B%BE%E7%89%872.png)

## 六、实验感想
作为第三次做的java实验，我已经学会类、方法的构建。不同函数的构建和引用没，体会到了修饰符super（）的用法。我还学会了如何从简化文本扫描、获取控制台输入。通过循环语句来进行选择和取消该课程。另外我在中途还出现了个错误，用System.out.print（）在子类里面，可是输出却是乱码，后来改用toString（）完美的解决了这个问题。
