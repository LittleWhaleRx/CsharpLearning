# CsharpLearning
# C#学习笔记
## 字段
### 字段修饰符：readonly
功能：为实例或者类型保存一旦初始化后就不希望再次改变的值
#### 只读实例字段
例：  
class Myclass  
  {   
    public int age;  
    public stream name;  
    public readonly int ID；  
    public Myclass(int id)  
    {  
      this.ID = id;  
    }  
  }  
只读实例字段，一经设定就不能再次修改，在实例构造器中进行初始化；  
只读实例构造器，在创建对象的时候设置只读字段的值，设置之后则无法再次修改；  
#### 只读静态字段
例：  
  struct Color  
  {  
    public int Red；  
    public int Green；  
    public int Blue；  
  }  
  class Brush  
  {  
    public static readonly Color DefaultColor；  
    staic Brush（）  
    {  
      Brush.DefaultColor = new Color(){Red = 0,Green = 0,Blue = 0};  
    }  
  }  
  只读静态字段，与只读实例字段一样，一经设定就不能修改且在静态构造器中进行初始化；  
  只读静态字段，在创建对象的时候设置只读字段的值，设置之后无法再次修改；  
