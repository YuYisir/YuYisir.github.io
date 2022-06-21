# 运算符
## 赋值运算符

```java
package com.itheima.hello.BiliVideo.Yunsuanfu;
//赋值运算符
public class FuZhi {
    public static void main(String[] args) {
        // = += -= *= /= %=
        int a = 10;
        int b = 200;
        //a = a + b
        a += b;  //a = (int)(a+b)
        System.out.println(a);

        byte i =10;
        byte j = 20;
        //i = (byte) (i+j);
        i += j;
        System.out.println(i);

        int m = 10;
        int n = 5;
        m -= n;
        System.out.println(m);
    }

}
```
### 详解
a+b 可简写为 a+=b
System.out.println(a+b);-----(未定义a += b)

或者

System.out.println(a);-----(定义了a += b)



## 关系运算符

```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;
//关系运算符
/*
    逻辑与 &   必须都是true，结果才是true；只要有一个是false，结果一定是false
    逻辑或 |   只要有一个为true，结果就是true
    逻辑非 !   你真我假，你假我真。!true=false  !false=true
    逻辑异或 ^  如果两个条件都是false或者都是true 则结果是false。两个条件不同结果是true
* */
public class GuanXi {
    public static void main(String[] args) {
        int a = 10;
        int b = 10;
        boolean rs = a == b;
        System.out.println(rs);

        System.out.println(a == b);
        System.out.println(a != b);
        System.out.println(a > b);
        System.out.println(a >= b);
        System.out.println(a < b);
        System.out.println(a <= b);
        System.out.println("---------------------");
        int i = 10;
        int j = 5;
        System.out.println(i == j);
        System.out.println(i != j);
        System.out.println(i > j);
        System.out.println(i >= j);
        System.out.println(i < j);
        System.out.println(i <= j);
        System.out.println(i = j);//相等判断必须是==  如果是=是在进行赋值运算。

    }
}
```

### 详解
关系运算符（relational operators）也可以称为“比较运算符”，用于用来比较判断两个变量或常量的大小。关系运算符是二元运算符，运算结果是 boolean 型。当运算符对应的关系成立时，运算结果是 true，否则是 false。

关系表达式是由关系运算符连接起来的表达式。关系运算符中“关系”二字的含义是指一个数据与另一个数据之间的关系，这种关系只有成立与不成立两种可能情况，可以用逻辑值来表示，逻辑上的 true 与 false 用数字 1 与 0 来表示。关系成立时表达式的结果为 true（或 1），否则表达式的结果为 false（或 0）。表 1 给出了比较运算符的含义及其实例应用。

<table border="1"><caption>表1比较运算符的含义及其实例应用</caption><tbody><tr><th>运算符</th><th>含义</th><th>说明</th><th>实例</th><th>结果</th></tr><tr><td>&gt;</td><td>大于运算符</td><td>只支持左右两边操作数是数值类型。如果前面变量的值大于后面变量的值，则返回true。</td><td>2&gt;3</td><td>false</td></tr><tr><td>&gt;=</td><td>大于或等于运算符</td><td>只支持左右两边操作数是数值类型。如果前面变量的值大于等于后面变量的值，则返回true。</td><td>4&gt;=2</td><td>true</td></tr><tr><td>&lt;</td><td>小于运算符</td><td>只支持左右两边操作数是数值类型。如果前面变量的值小于后面变量的值，则返回true。</td><td>2&lt;3</td><td>true</td></tr><tr><td>&lt;=</td><td>小于或等于运算符</td><td>只支持左右两边操作数是数值类型。如果前面变量的值小于等于后面变量的值，则返回true。</td><td>4&lt;=2</td><td>false</td></tr><tr><td>==</td><td>相等运算符</td><td>如果进行比较的两个操作数都是数值类型，无论它们的数据类型是否相同，只要它们的值相等，也都将返回true。<br>如果两个操作数都是引用类型，只有当两个引用变量的类型具有父子关系时才可以比较，只要两个引用指向的不是同一个对象就会返回true。<br><a href="/java/"target="_blank">Java</a>也支持两个boolean类型的值进行比较。</td><td>4==4<br>97=='a'<br>5.0==5<br>true==false</td><td>true<br>true<br>true<br>false</td></tr><tr><td>!=</td><td>不相等运算符</td><td>如果进行比较的两个操作数都是数值类型，无论它们的数据类型是否相同，只要它们的值不相等，也都将返回true。<br>如果两个操作数都是引用类型，只有当两个引用变量的类型具有父子关系时才可以比较，只要两个引用指向的不是同一个对象就会返回true。</td><td>4!=2</td><td>true</td></tr></tbody></table>


<br>

关系运算符的优先级为：>、<、>=、<= 具有相同的优先级，并且高于具有相同优先级的 !=、==。关系运算符的优先级高于赋值运算符而低于算术运算符，结合方向是自左向右。

不要将“==”写成“=”。


## +符号做连接符
