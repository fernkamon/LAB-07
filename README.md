#ใบงานที่ 7
##เรื่อง  พื้นฐานภาษา C#
##วัตถุประสงค์
1). เพื่อให้นักศึกษาสามารถใช้งานภาษา C# ขั้นพื้นฐานได้
##ลำดับขั้นการทดลอง
1).	การตั้งชื่อตัวแปรในภาษา C# 
	ให้นักศึกษาพิจารณาชื่อตัวแปรตามตารางต่อไปนี้ ว่าสามารถใช้ได้หรือไม่ พร้อมบอกเหตุผล

 ชื่อตัวแปร | ใช้ได้/ไม่ได้ | เหตุผล
:--------- | ----------- | -------- 
xxx	|ใช้ได้	|ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ
null	|ใช้ไม่ได้	|เป็นคำสงวนในภาษา C#
_value	| ใช้ได้ |	สามารถใช้สัญลักษ์ _ ได้
First-name | ใช่ไม่ได้| มีเครื่องหมายทางคณิตศาสตร์อยู่ในชื่อ			
Hello!	| ใช้ไม่ได้| มีเครื่องหมายตัวอักษรพิเศษอยู่ในชื่อ	
w*h 	| ใช้ไม่ได้| มีเครื่องหมายทางคณิตศาสตร์อยู่ในชื่อ			
time	|ใชได้ | 	ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ		
do	|ใช้ไม่ได้ |	เป็นคำสงวนในภาษา C#		
Do	| ใช้ได้| เป็นตัวพิมพ์ใหญ่ ซึ่งจะมีความหมายที่แตกต่างจากคำว่า do			
21November	|ใช้ไม่ได้ |	คำขึ้นต้นไม่สามารถขึ้นต้นด้วยตัวเลขได้		
ladkrabang	| ใช้ได้|	ไม่มีตัวอักษรที่ละเมิดกฎการตั้งชื่อ		
Student ID	|ใช้ไม่ได้ | ไม่สามารถเว้นวรรคในชื่อได้			

##2). ชนิดข้อมูลภายในภาษา C# 
  2.1).	Property ของชนิดข้อมูล
ในภาษา C# มีชนิดข้อมูลต่างๆ ได้แก่ ```byte```, ```char```, ```bool```, ```sbyte```, ```short```, ```ushort```, ```int``` , ```uint```, ```float```, ```double```, ```decimal```, ```long```, ```ulong``` โดยแต่ละชนิด มีคุณสมบัติที่สำคัญได้แก่ ขนาด (เป็นไบต์) ค่าต่ำสุด ค่าสูงสุด ที่เก็บในตัวแปรชนิดนั้นๆ ได้ ซึ่งมีฟังก์ชันในภาษา C# ที่ช่วยให้เราทราบคุณสมบัติเหล่านั้น ได้แก่คำสั่ง ```sizeof()```,  ```MinValue()``` และ ```MaxValue()```
การแสดงค่าคุณสมบัติต่างๆ ของตัวแปร สามารถทำได้โดยใช้ฟังก์ชั่นเหล่านั้น ดังตัวอย่าง

**ตัวอย่างที่ 1** โปรแกรมแสดงคุณสมบัติ ```size```, ```MinValue``` และ ```MaxValue``` ของชนิดข้อมูล

```csharp
using System;
namespace variableProperties
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Data type : int");
            Console.WriteLine("Size :" + sizeof(int));
            Console.WriteLine("Minimum Value :" + int.MinValue);
            Console.WriteLine("Maximum Value :" + int.MaxValue);
        }
    }
}

```
ผลที่ได้จากโปรแกรม
```
Data type : int
Size :4
Minimum Value :-2147483648
Maximum Value :2147483647
```


คำสั่งสำหรับการทดลอง
ให้นักศึกษา เขียนโปรแกรมคล้ายกับตัวอย่างที่ 1 โดยมีชนิดข้อมูลเป็น byte, char, bool, sbyte, short, ushort, uint, float, double, decimal, long และ ulong
   
   CODE PROGRAM
   
  ```  
   using System;
namespace variableProperties
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Data type : byte");
            Console.WriteLine("Size :" + sizeof(byte));
            Console.WriteLine("Minimum Value :" + byte.MinValue);
            Console.WriteLine("Maximum Value :" + byte.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : char");
            Console.WriteLine("Size :" + sizeof(char));
            Console.WriteLine("Minimum Value :" + (int)char.MinValue);
            Console.WriteLine("Maximum Value :" + (int)char.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            bool a = 4 > 5;
            Console.WriteLine("Data type : bool");
            Console.WriteLine("4 > 5 then True/False");
            Console.WriteLine("{0}", a);
            bool b = 10 < 20;
            Console.WriteLine("10 < 20 then True/False");
            Console.WriteLine("{0}", b);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : sbyte");
            Console.WriteLine("Size :" + sizeof(sbyte));
            Console.WriteLine("Minimum Value :" + sbyte.MinValue);
            Console.WriteLine("Maximum Value :" + sbyte.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : short");
            Console.WriteLine("Size :" + sizeof(short));
            Console.WriteLine("Minimum Value :" + short.MinValue);
            Console.WriteLine("Maximum Value :" + short.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : ushort");
            Console.WriteLine("Size :" + sizeof(ushort));
            Console.WriteLine("Minimum Value :" + ushort.MinValue);
            Console.WriteLine("Maximum Value :" + ushort.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : uint");
            Console.WriteLine("Size :" + sizeof(uint));
            Console.WriteLine("Minimum Value :" + uint.MinValue);
            Console.WriteLine("Maximum Value :" + uint.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : float");
            Console.WriteLine("Size :" + sizeof(float));
            Console.WriteLine("Minimum Value :" + float.MinValue);
            Console.WriteLine("Maximum Value :" + float.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : double");
            Console.WriteLine("Size :" + sizeof(double));
            Console.WriteLine("Minimum Value :" + double.MinValue);
            Console.WriteLine("Maximum Value :" + double.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : decimal");
            Console.WriteLine("Size :" + sizeof(decimal));
            Console.WriteLine("Minimum Value :" + decimal.MinValue);
            Console.WriteLine("Maximum Value :" + decimal.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : long");
            Console.WriteLine("Size :" + sizeof(long));
            Console.WriteLine("Minimum Value :" + long.MinValue);
            Console.WriteLine("Maximum Value :" + long.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
            Console.WriteLine("Data type : ulong");
            Console.WriteLine("Size :" + sizeof(ulong));
            Console.WriteLine("Minimum Value :" + ulong.MinValue);
            Console.WriteLine("Maximum Value :" + ulong.MaxValue);
            Console.WriteLine("---------------------------------");
            Console.WriteLine("");
        }
    }
}
```
  
  จะได้ผลลัพธ์ดังนี้
    
  ![](https://github.com/fernkamon/LAB-07/blob/master/type1.JPG)
  
  ![](https://github.com/fernkamon/LAB-07/blob/master/type2.JPG)


**หมายเหตุ**
 
ชนิดข้อมูล ```bool``` เก็บข้อมูลได้เฉพาะ ```true``` และ ```false``` ไม่ต้องหา ```MinValue``` และ ```MaxValue```

ชนิดข้อมูล ```char``` จะต้องมีการ cast ค่า ```MinValue``` และ ```MaxValue``` ไปยัง int ก่อน ดังนี้
```csharp
            Console.WriteLine("Minimum Value :" + (int) char.MinValue);
            Console.WriteLine("Maximum Value :" + (int) char.MaxValue);
```
 2.2).	การใช้งานข้อมูลชนิดต่างๆ
 2.2.1).	ข้อมูลชนิดตรรกะ The Boolean Type

ข้อมูลชนิดตรรกะ (boolean) มีค่าที่เป็นไปได้เพียง 2 ค่าเท่านั้นคือ ```true``` และ ```false``` ในภาษา C# จะไม่สามารถกำหนดค่าตัวเลขลงไปในตัวแปร boolean ได้ ส่วนใหญ่ตัวแปร boolean มักใช้เพื่อการตัดสินใจและมีที่มาจากการประเมินค่าสมการต่างๆ ตัวอย่างต่อไปนี้เป็นการใช้ตัวแปร boolean กับการเปรียบเทียบด้วยตัวดำเนินการ “>”
**ตัวอย่าง**
```csharp
using System;

class Operators {
    static void Main() {
        bool a = 4 > 5;
        Console.WriteLine("{0}", a);
    }
}
```
##สนุกกับการสร้างตัวเลขสุ่ม
 ในภาษา C# มีวิธีการสร้างตัวเลขสุ่ม (random number) โดยใช้คลาส Random มาสร้างเป็นตัวแปรโดยมีรูปแบบดังนี้
```csharp
		Random random = new Random();
```
เมื่อสร้างแล้ว เราสามารถนำมาหาค่าตัวเลขสุ่มจากตัวแปรดังกล่าว ซึ่งมักจะกำหนดค่าสูงสุดและต่ำสุดในการสุ่มลงไปด้วย ดังนี้
```csharp
		int randomNumber = random.Next(0, 100);
```
โปรแกรมด้านล่างนี้เป็นตัวอย่างการสุ่มเลข 0 – 100
```csharp
using System;
namespace RandomNumber
{
    class Program
    {
        static void Main(string[] args)
        {
            Random random = new Random();
            int randomNumber = random.Next(0, 100);
            Console.WriteLine(randomNumber);
        }
    }
}

```
##การทดลอง การใช้งานข้อมูลชนิด boolean (1)

ให้เขียนโปรแกรมโดยมีข้อกำหนดดังนี้

1. สร้างตัวแปร Random โดยการมีสุ่มเลข 1 หลัก (0 – 9 )

1. สร้างตัวแปรชนิด integer สำหรับรับค่าจากผู้ใช้

1. สร้างตัวแปร boolean โดยเก็บค่าที่ได้จากการเปรียบเทียบตัวเลขในข้อ 1 และ 2

```
using System;
namespace RandomNumber
{
    class Program
    {
        static void Main(string[] args)
        {
            Random random1 = new Random();
            int randomNumber1 = random1.Next(0, 9);
            Console.WriteLine("1. Random 0 - 9");
            Console.WriteLine("    Random1 = {0} ", randomNumber1);
            Console.WriteLine("---------------------------");
            Console.WriteLine("");
            Console.WriteLine("2. Pleace Input First and Second");
            Console.Write("First : ");
            int a = Convert.ToInt32(Console.ReadLine());
            Console.Write("Second : ");
            int b = Convert.ToInt32(Console.ReadLine());
            Random random2 = new Random();
            int randomNumber2 = random2.Next(a, b);
            Console.WriteLine("     Random2 = {0} ", randomNumber2);
            Console.WriteLine("---------------------------");
            Console.WriteLine("");
            bool c = randomNumber1 < randomNumber2;
            Console.WriteLine("3. Boolean Operators");
            Console.WriteLine("     {0} < {1}", randomNumber1, randomNumber2);
            Console.WriteLine("     {0}", c);
        }
    }
}
```

1. ให้พิมพ์ค่าตัวแปร boolean ในข้อ 3 ออกทางหน้าจอ

![](https://github.com/fernkamon/LAB-07/blob/master/random.JPG)

##การเขียนโปรแกรมด้วยตัวดำเนินการทางตรรกะ

ตัวแปรชนิด boolean มักจะถูกใช้เป็นที่เก็บผลที่เกิดจากการดำเนินการทางตรรกะ เช่น AND, OR, NOT เป็นต้น ซึ่งการดำเนินการทางตรรกะจะมีตารางความจริง เป็นตัวบอกผลในการดำเนินการของตัวดำเนินการต่างๆ ดังตัวย่าง

**Y = A AND B**

A|	B|	Y
:----:|:-----:|:-----:
0	|0	|0
0	|1	|0
1	|0	|0
1	|1	|1


**Y = A OR B**

A|	B|	Y
:-----:|:-----:|:-----:
0 | 0 |	0
0 | 1 |	1
1 | 0 |	1
1 | 1 | 1
	
**Y = NOT A**

A | Y
:---:|:---:
0 | 1
1 | 0


##ตัวดำเนินการในภาษา C# ใช้เครื่องหมายต่างๆ ดังต่อไปนี้

การดำเนินการ | เครื่องหมาย
-----------|:------------:
Logical AND |	&
Logical XOR |	^
Logical OR |	\|

ตัวอย่างภาษา C# ต่อไปนี้เป็นการพิมพ์ตารางความจริงออกทางหน้าจอ
```csharp
using System;
namespace thruthTable
{
    class Program
    {
        static void Main(string[] args)
        {
            bool A, B,Y;
            Console.WriteLine("      Y = A AND B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A,B,Y);
            A = false; B = true; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
        }
    }
}
```

ผลที่ได้คือ 
```
      Y = A AND B
-----------------------
   A      B     |  Y
-----------------------
 False  False   | False
 False  True    | False
 True   False   | False
 True   True    | True
-----------------------
```

##การทดลอง การใช้งานข้อมูลชนิด boolean (2)
ให้เขียนโปรแกรมเพื่อสร้างตารางความจริงของลอจิกดังต่อไปนี้
```
1. AND
2. OR
3. NOT
4. NAND
5. NOR
6. Exclusive OR
```

CODE Program
```
using System;
namespace thruthTable
{
    class Program
    {
        static void Main(string[] args)
        {
            bool A, B,Y;
            Console.WriteLine("      Y = A AND B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A,B,Y);
            A = false; B = true; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = A & B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
            Console.WriteLine("");
            Console.WriteLine("      Y = A OR B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = A | B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = false; B = true; Y = A | B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = A | B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = A | B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
            Console.WriteLine("");
            Console.WriteLine("    Y = NOT A");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A   |  Y");
            Console.WriteLine("-----------------------");
            A = false; Y = !A;
            Console.WriteLine(" {0} | {1}", A, Y);
            A = false; Y = !A;
            Console.WriteLine(" {0} | {1}", A, Y);
            Console.WriteLine("-----------------------");
            Console.WriteLine("");
            Console.WriteLine("      Y = A NAND B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = !(A & B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = false; B = true; Y = !(A & B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = !(A & B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = !(A & B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
            Console.WriteLine("");
            Console.WriteLine("      Y = A NOR B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = !(A | B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = false; B = true; Y = !(A | B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = !(A | B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = !(A | B);
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
            Console.WriteLine("");
            Console.WriteLine("   Y = A Exclusive OR B");
            Console.WriteLine("-----------------------");
            Console.WriteLine("   A      B\t|  Y");
            Console.WriteLine("-----------------------");
            A = false; B = false; Y = A ^ B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = false; B = true; Y = A ^ B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = false; Y = A ^ B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            A = true; B = true; Y = A ^ B;
            Console.WriteLine(" {0}\t{1}\t| {2}", A, B, Y);
            Console.WriteLine("-----------------------");
        }
    }
}
```

![](https://github.com/fernkamon/LAB-07/blob/master/CODE.JPG)


  2.2.2.	ชนิดข้อมูลตัวเลขจำนวนเต็ม (Integer Types)
ข้อมูลชนิดตัวเลข สามารถนำไปใช้งานได้หลากหลาย เช่น การนับหรือแสดงจำนวน การกำหนดลำดับที่ การจัดลำดับ เป็นต้น ค่าที่ใส่ลงในตัวแปร เป็นได้ทั้งค่าบวก ค่าศูนย์ และค่าลบ (มีตัวแปรบางชนิดที่เก็บเฉพาะค่าบวกเพียงอย่างเดียว) การกำหนดค่าใดๆ ให้กับตัวแปร ทำได้โดยการใช้เครื่องหมาย =

การใช้เครื่องหมายคณิตศาสตร์กับตัวแปรจำนวนเต็ม สามารถใช้ได้ทุกเครื่องหมาย ได้แก่ +, -, *, / และ %

**ตัวอย่าง** การใช้เครื่องหมายทางคณิตศาสตร์กับตัวแปรชนิดจำนวนเต็ม
```csharp
using System;
public class intergerTest
{
    static void Main(string[] args)
    {
        int a, b, c, d, e, f;
        a = 1;
        b = a + 6;
        c = b - 3;
        d = c * 2;
        e = d / 2;
        f = e % 2;
    }
}
```

##การทดลอง หาค่าจากสมการทางคณิตศาสตร์

กำหนด ```a = 10, b = 20, x = 5, y = 2`` 
ให้เขียนโปรแกรมเพื่อหาผลลัพธ์ของสมการต่อไปนี้
```
1.	a+b
2.	x-b
3.	x*b
4.	y/a
5.	b%y
6.	y+10%x
7.	a/3*5
8.	9/2*a
9.	y%8
10.	100*x+y%2-a
```
Code Program

```
using System;
public class intergerTest
{
    static void Main(string[] args)
    {
        double a = 10, b = 20, x = 5, y = 2, ans;
          
        ans = a + b;
        Console.WriteLine("With a = 10, b = 20, x = 5, y = 2");
        Console.WriteLine("");
        Console.WriteLine("1. a + b");
        Console.WriteLine("   {1} + {2} = {0} ", ans, a, b);
        Console.WriteLine("");
        ans = x - b;
        Console.WriteLine("2. x - b");
        Console.WriteLine("  {1} - {2} = {0}", ans, x, b);
        Console.WriteLine("");
        ans = x * b;
        Console.WriteLine("3. x * b");
        Console.WriteLine("   {1} * {2} = {0}", ans, x, b);
        Console.WriteLine("");
        ans = y / a;
        Console.WriteLine("4. y / a");
        Console.WriteLine("   {1} / {2} = {0}", ans, y, a);
        Console.WriteLine("");
        ans = b % y;
        Console.WriteLine("5. b % y");
        Console.WriteLine("   {1} % {2} = {0}", ans, b, y);
        Console.WriteLine("");
        ans = y + 10 % x;
        Console.WriteLine("6. y + 10 % x");
        Console.WriteLine("   {1} + 10 % {2} = {0}", ans, y, x);
        Console.WriteLine("");
        ans = a / 3 * 5;
        Console.WriteLine("7. a / 3 * 5");
        Console.WriteLine("   {1} / 3 * 5 = {0}", ans, a);
        Console.WriteLine("");
        ans = 9 / 2 * a;
        Console.WriteLine("8. 9 / 2 * a");
        Console.WriteLine("   9 / 2 * {1}  = {0}", ans, a);
        Console.WriteLine("");
        ans = y % 8;
        Console.WriteLine("9. y % 8");
        Console.WriteLine("   {1} % 8 = {0}", ans, y);
        Console.WriteLine("");
        ans = 100 * x + y % 2 - a;
        Console.WriteLine("10. 100 * x + y % 2 - a");
        Console.WriteLine("   100 * {1} + {2} % 2 - {3} = {0}", ans, x, y, a);
    }
}
```

![](https://github.com/fernkamon/LAB-07/blob/master/math.JPG)

##2.2.3. ชนิดข้อมูลเลขทศนิยม (Floating Point and Decimal Types)
ตัวเลขจำนวนทศนิยม มักจะใช้ในการคำนวณทางวิทยาศาสตร์ เนื่องจากค่าในวิทยาศาสตร์ต้องการความละเอียดสูง หรือมีค่าสูงมากกว่าที่เลขจำนวนเต็มจะเก็บได้

**ตัวอย่างการแก้ปัญหาทางวิทยาศาสตร์**

ระยะทางจากดาวอาทิตย์ถึงโลกคือ 93,000,000 ไมล์ เรียกว่า 1 A.U. (Astronomical Unit)

ความเร็วในการเดินทางของแสงคือ 186,000 ไมล์ต่อวินาที

ระยะทาง 1 ไมล์ คิดเป็น 1.609344 กิโลเมตร

ให้เขียนโปรแกรมหาระยะทางในการเดินทางของแสง ในหน่วยกิโลเมตรต่อวินาทีและเวลาในการเดินทางของแสงจากดวงอาทิตย์มายังโลก

##ตัวอย่าง โปรแกรมคำนวณระยะทางและเวลาของแสงจากดวงอาทิตย์ถึงโลก
```csharp
using System;
namespace variableProperties
{
    class Program
    {
        static void Main(string[] args)
        {
            const double lightSpeed = 186000d;   // miles per second
            Console.WriteLine("Light speed = {0} Mile Per second", lightSpeed);
            const double mileTokm = 1.609344;
            Console.WriteLine("Light speed = {0} km Per second", lightSpeed*mileTokm);
            const double SunToEarthDistance =  93000000d ;  // miles
            Console.WriteLine("SunToEarthDistance = {0} km", SunToEarthDistance * mileTokm);
            double SunToEarthTimeOfLight = SunToEarthDistance / lightSpeed;  // miles
            Console.WriteLine("SunToEarthTimeOfLight = {0} seconds", SunToEarthTimeOfLight);
            Console.WriteLine("SunToEarthTimeOfLight = {0} minutes", SunToEarthTimeOfLight/60d);
        }
    }
}
```
ผลที่ได้จากโปรแกรม
```
Light speed = 186000 Mile Per second
Light speed = 299337.984 km Per second
SunToEarthDistance = 149668992 km
SunToEarthTimeOfLight = 500 seconds
SunToEarthTimeOfLight = 8.33333333333333 minutes
```
##คำสั่ง ให้เขียนโปรแกรมคำนวณค่าเพื่อเติมลงในช่องว่างในตาราง
**ตารางที่ 1** ระยะทางจากดวงอาทิตย์ถึงดาวเคราะห์ต่างๆ

ดาวเคราะห์ | ระยะทางจากดวงอาทิตย์ | ระยะทางในหน่วย A.U. | เวลาของแสง (นาที)
:----:|:----:|:----:|:----: 
Mercury |	57,910,000 km	| 0.386920491854452 |	3.22433743212043
Venus |	108,200,000 km	| 0.722928634409457	| 6.02440528674548
Earth |	149,600,000 km	|	0.999539036115109 | 8.32949196762591
Mars |	227,940,000 km	| 1.5229607479417	| 12.6913395661808
Jupiter |	778,330,000 km  | 5.20034236617295	| 43.3361863847746	
Uranus |	2,873,550,000 km | 19.1993676285332	| 43.3361863847746	
Neptune |	4,501,000,000 km | 30.0730294221531	| 250.608578517943	
Pluto |	5,945,900,000 km	| 39.7269996981071	| 331.058330817559

   CODE PROGRAM

```
   using System;
namespace variableProperties
{
    class Program
    {
        static void Main(string[] args)
        {
            const double lightSpeed = 186000d;   // miles per second
            Console.WriteLine("Light speed = {0} Mile Per second", lightSpeed);
            const double mileTokm = 1.609344;
            Console.WriteLine("Light speed = {0} km Per second", lightSpeed * mileTokm);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double au = 93000000d;
            const double SunToMercuryDistance = 57910000 / mileTokm;  // miles
            Console.WriteLine("             Mercury");
            Console.WriteLine("SunToMercuryDistance = {0} A.U.", SunToMercuryDistance / au);
            double SunToMercuryTimeOfLight = SunToMercuryDistance / lightSpeed;  // miles
            Console.WriteLine("SunToMercuryTimeOfLight = {0} minutes", SunToMercuryTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToVenusDistance = 108200000 / mileTokm;  // miles
            Console.WriteLine("             Venus");
            Console.WriteLine("SunToVenusDistance = {0} A.U.", SunToVenusDistance / au);
            double SunToVenusTimeOfLight = SunToVenusDistance / lightSpeed;  // miles
            Console.WriteLine("SunToMercuryTimeOfLight = {0} minutes", SunToVenusTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToEarthDistance = 149600000 / mileTokm;  // miles
            Console.WriteLine("             Earth");
            Console.WriteLine("SunToEarthDistance = {0} A.U.", SunToEarthDistance / au);
            double SunToEarthTimeOfLight = SunToEarthDistance / lightSpeed;  // miles
            Console.WriteLine("SunToEarthTimeOfLight = {0} minutes", SunToEarthTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToMarsDistance = 227940000 / mileTokm;  // miles
            Console.WriteLine("             Mars");
            Console.WriteLine("SunToMarsDistance = {0} A.U.", SunToMarsDistance / au);
            double SunToMarsTimeOfLight = SunToMarsDistance / lightSpeed;  // miles
            Console.WriteLine("SunToMarsTimeOfLight = {0} minutes", SunToMarsTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToJupiterDistance = 778330000 / mileTokm;  // miles
            Console.WriteLine("             Jupiter");
            Console.WriteLine("SunToJupiterDistance = {0} A.U.", SunToJupiterDistance / au);
            double SunToJupiterTimeOfLight = SunToJupiterDistance / lightSpeed;  // miles
            Console.WriteLine("SunToJupiterTimeOfLight = {0} minutes", SunToJupiterTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToUranusDistance = 2873550000 / mileTokm;  // miles
            Console.WriteLine("             Uranus");
            Console.WriteLine("SunToUranusDistance = {0} A.U.", SunToUranusDistance / au);
            double SunToUranusTimeOfLight = SunToJupiterDistance / lightSpeed;  // miles
            Console.WriteLine("SunToUranusTimeOfLight = {0} minutes", SunToUranusTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToNeptuneDistance = 4501000000 / mileTokm;  // miles
            Console.WriteLine("             Neptune");
            Console.WriteLine("SunToNeptuneDistance = {0} A.U.", SunToNeptuneDistance / au);
            double SunToNeptuneTimeOfLight = SunToNeptuneDistance / lightSpeed;  // miles
            Console.WriteLine("SunToNeptuneTimeOfLight = {0} minutes", SunToNeptuneTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");
            const double SunToPlutoDistance = 5945900000 / mileTokm;  // miles
            Console.WriteLine("             Pluto");
            Console.WriteLine("SunToPlutoDistance = {0} A.U.", SunToPlutoDistance / au);
            double SunToPlutoTimeOfLight = SunToPlutoDistance / lightSpeed;  // miles
            Console.WriteLine("SunToPlutoTimeOfLight = {0} minutes", SunToPlutoTimeOfLight / 60d);
            Console.WriteLine("---------------------------------------------------------");
            Console.WriteLine("");

        }
    }
}
```
   ผลลัพธ์ที่ได้ 
   
  ![](https://github.com/fernkamon/LAB-07/blob/master/star.JPG)
  
##คลาส Math 
ในภาษา C# มีคลาสที่เป็นตัวช่วยคำนวณทางคณิตศาสตร์ ที่ช่วยให้เราสามารถคำนวณฟังก์ชันพื้นฐานได้ อย่างรวดเร็ว ไม่ต้องพัฒนาโปรแกรมเพิ่มเติมด้วยเอง นั่นคือคลาส Math  ฟังก์ชันทางคณิตศาสตร์ที่ใช้บ่อยๆ สามารถดูรายละเอียดทั้งหมดได้จาก 
[system.math](http://msdn.microsoft.com/en-us/library/system.math%28v=vs.110%29.aspx) 

##ตัวอย่าง โปรแกรมพล็อตรูป sine wave บนหน้าจอ
```csharp
using System;
public class MathTest
{
    static void Main(string[] args)
    {
        for (float i = 0; i < Math.PI * 2.0F; i += 0.3F)
        {
            Console.WriteLine("The sine of {0,10:F} = {1,-10:F6}" + spaces(Math.Sin(i)) + "*", i, Math.Sin(i));
        }

    }
    private static string spaces(double val)
    {
        string SpaceString = new String(' ', ((int)(val * 10.0)) + 10);
        return SpaceString;
    }
}
```

ผลที่ได้

```
The sine of       0.00 = 0.000000            *
The sine of       0.30 = 0.295520              *
The sine of       0.60 = 0.564642                 *
The sine of       0.90 = 0.783327                   *
The sine of       1.20 = 0.932039                     *
The sine of       1.50 = 0.997495                     *
The sine of       1.80 = 0.973848                     *
The sine of       2.10 = 0.863209                    *
The sine of       2.40 = 0.675463                  *
The sine of       2.70 = 0.427380                *
The sine of       3.00 = 0.141120             *
The sine of       3.30 = -0.157745          *
The sine of       3.60 = -0.442520       *
The sine of       3.90 = -0.687766     *
The sine of       4.20 = -0.871576   *
The sine of       4.50 = -0.977530  *
The sine of       4.80 = -0.996165  *
The sine of       5.10 = -0.925815  *
The sine of       5.40 = -0.772764    *
The sine of       5.70 = -0.550685      *
The sine of       6.00 = -0.279415         *
```

##การทดลอง พล็อตรูปคลื่นทางคณิตศาสตร์
จากโปรแกรมตัวอย่าง ให้ดัดแปลงโปรแกรมเพื่อวาดรูปคลื่นดังต่อไปนี้
```
1.	y = x2
2.	y = cos(x)
3.	y = tan(x)
```
  
  1. y = x^2
  
  ```
  using System;
public class MathTest
{
    static void Main(string[] args)
    {
        for (float i = 0; i < Math.PI * 2.0F; i += 0.3F)
        {
            Console.WriteLine("The sine of {0,10:F} = {1,-10:F6}" + spaces((i*i)) + "*", i , (i*i));
        }

    }
    private static string spaces(double val)
    {
        string SpaceString = new String(' ', (int)val);
        return SpaceString;
    }
}
  ```
  
 ![](https://github.com/fernkamon/LAB-07/blob/master/x%5E2.JPG)
 
  2. y = cos x
  
   ```
   using System;
public class MathTest
{
    static void Main(string[] args)
    {
        for (float i = 0; i < Math.PI * 2.0F; i += 0.3F)
        {
            Console.WriteLine("y = Cos x {0,10:F} = {1,-10:F6}" + spaces(Math.Cos(i)) + "*", i , Math.Cos(i));
        }

    }
    private static string spaces(double val)
    {
        string SpaceString = new String(' ', ((int)(val * 10.0)) + 10);
        return SpaceString;
    }
}
     ```
     
     ![](https://github.com/fernkamon/LAB-07/blob/master/COS.JPG)

3.	y = tan(x)

 ```
 using System;
public class MathTest
{
    static void Main(string[] args)
    {
        for (float i = 0; i < Math.PI * 2.0F; i += 0.3F)
        {
            Console.WriteLine("y = Tan x {0,10:F} = {1,-10:F6}" + spaces(Math.Tan(i)) + "*", i , Math.Tan(i));
        }

    }
    private static string spaces(double val)
    {
        string SpaceString = new String(' ', (int)val+100);
        return SpaceString;
    }
}
  ```
  
  ![](https://github.com/fernkamon/LAB-07/blob/master/tan.JPG)
