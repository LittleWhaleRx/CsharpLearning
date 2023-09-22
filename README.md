# CsharpLearning
# C#学习笔记
## 字段
### 字段修饰符：readonly
功能：为实例或者类型保存一旦初始化后就不希望再次改变的值
#### 只读实例字段
例：  
&emsp;&emsp;class Myclass  
&emsp;&emsp;&emsp;&emsp;{   
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public int age;  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public stream name;  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public readonly int ID；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public Myclass(int id)  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;{  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;this.ID = id;  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;}  
&emsp;&emsp;&emsp;&emsp;}  
只读实例字段，一经设定就不能再次修改，在实例构造器中进行初始化；  
只读实例构造器，在创建对象的时候设置只读字段的值，设置之后则无法再次修改；  
#### 只读静态字段
例：  
&emsp;&emsp;struct Color  
&emsp;&emsp;&emsp;&emsp;{  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public int Red；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public int Green；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public int Blue；  
&emsp;&emsp;&emsp;&emsp;}  
&emsp;&emsp;class Brush  
&emsp;&emsp;&emsp;&emsp;{  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;public static readonly Color DefaultColor；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;staic Brush（）  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;{  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;Brush.DefaultColor = new Color(){Red = 0,Green = 0,Blue = 0};  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;}  
&emsp;&emsp;&emsp;&emsp;}  
  只读静态字段，与只读实例字段一样，一经设定就不能修改且在静态构造器中进行初始化；  
  只读静态字段，在创建对象的时候设置只读字段的值，设置之后无法再次修改；  
## 属性
- 属性（property）是一种用于**访问对象或类型的特征**的成员，**特征反映了状态**
- 属性是字段的自然扩展
  - 从命名上看，field更偏向于实例对象在内存中的布局，property更偏向于反应现实世界对象的特征
  - 对外：暴露数据，数据是可以储存在字段里面的，也可以是动态计算出来的
  - 对内：保护字段不被非法值“污染”
- 属性由Get/Set方法对 进化而来
- 又一个“语法糖”——属性背后的秘密
