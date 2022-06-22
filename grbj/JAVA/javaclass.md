# 运算符

## +符号做连接符

```java
package com.itheima.hello.BiliVideo.Yunsuanfu;

public class jiahao {
    public static void main(String[] args) {
        //目标：+符号做连接符的识别

        //能算则算，不能算就在一起。
        int a = 5;
        System.out.println("abc" + 'a');//abca
        System.out.println("abc" + a);//abc5
        System.out.println(5 + a);//10
        System.out.println("abc" + 5 + 'a');//abc5a
        System.out.println(15+"abc" +15);//15abc15
        System.out.println(a + 'a');//102
        System.out.println(a + "" + 'a');//5a
        System.out.println(a + 'a' + "itheima");//102itheima
        System.out.println("itheima" + a + 'a');//itheima5a
        System.out.println("itheima" + (a + 'a'));//itheima102
    }
}
```


## 自增自减运算符

```java
package com.itheima.hello.BiliVideo.Yunsuanfu;
//自增自减运算符(单独使用)
public class ZizengZijian {
    //++ 自增      --自减
    //若是单独使用，没有区别
    public static void main(String[] args) {
        int a = 10;
        a++;//a = a+1
        //或者++a也可以，都一样
        System.out.println(a);

        int b = 10; //b = b - 1;
        --b;
        //或者--b也可以，都一样
        System.out.println(b);
    }
}
```

### 若不是单独使用：

不单独使用（如在表达式中、或者同时有其他操作），放在变量前后会存在明显区别
1. 放在变量的**前面**，先对变量进行+1、-1操作，再拿变量的值运算
```JAVA
int a = 10;
int rs = ++a;
```
2. 放在变量的**后面**，先拿变量的值进行运算，再对变量的值进行+1、-1

```java
int b = 10;
int rs = +b++;
```

```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;
//自增自减运算符
public class ZizengZijian {
        System.out.println("---------------------------");
        //在表达式中或者不是单独操作情况，++ -- 在变量中存在区别
        //++ -- 在变量前面 先+1 -1 再使用
        int i = 10;
        int j = ++i;
        System.out.println(i);
        System.out.println(j);

        //++ -- 在变量后面 先使用  再+1 -1
        int m = 10;
        int n = m++;
        System.out.println(m);
        System.out.println(n);
    }
}

```

### 详解

* ++ 和 -- 既可以放在变量的后边，也可以是前边
* ++、--只能操作变量，不能操作字面量

<font color="brown">字面量</font>：比如说 2++、++2 ......

### 扩展案例
(！还未学成！)
```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;
//自增自减运算符
public class ZizengZijian {
    //++ 自增      --自减
    //若是单独使用，没有区别
    public static void main(String[] args) {
        System.out.println("----------------扩展案例----------------");
        int k = 3;
        int p = 5;
        //K 3 4 5 4
        //p 5 4 3 4
        //rs 3 + 5 - 4 - 4 - 5 + 4 + 2
        int rs = k++ + ++k - --p + p-- - k-- + ++p + 2;
        System.out.println(k);
        System.out.println(p);
        System.out.println(rs);
    }
}
```


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

+=还可以实现数据的累加，把别人的数据加给自己


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
        //结果为布尔值（boolean）
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


## (位)逻辑运算符

```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;

public class LuoJi {
/*
    逻辑与 &   必须都是true，结果才是true；只要有一个是false，结果一定是false
    逻辑或 |   只要有一个为true，结果就是true
    逻辑非 !   你真我假，你假我真。!true=false  !false=true
    逻辑异或 ^  如果两个条件都是false或者都是true 则结果是false。两个条件不同结果是true
* */

    public static void main(String[] args) {
        double size = 9.8;
        double storage = 16;
        //需求：尺寸大于等于6.95  内存大于等于8GB
        //必须前后都是true 才是true
        System.out.println(size >= 9.8 & storage >= 8);

        //需求：要么内存大于等于8  要么尺寸大于等于6.95
        //只要有一个是true 结果一定是true
        System.out.println(size >= 9.8 | storage >= 8);

        //逻辑异或  必须两个不同才是true
        System.out.println(false ^ true);
        System.out.println(false ^ false);


        // && 短路与---判断结果与 & 一样。过程是左边为false 右边则不执行
        // || 短路或---判断结果与 | 一样。过程是左边为true  右边则不执行
        System.out.println("---------------短路逻辑运算符---------------");
        int a = 10;
        int b = 20;
        System.out.println(a >100 && ++b >10);
        System.out.println(b);

        int i = 10;
        int j = 20;
        System.out.println(i > 2 || ++j > 10);
        System.out.println(j);
    }
}
```
### 详解
实际开发中常用逻辑运算符还是  &&  ||  ！

<table border="1"><caption>表1逻辑运算符的用法、含义及实例</caption><tbody><tr><th style="text-align: left;">运算符</th><th style="text-align: left;">用法</th><th style="text-align: left;">含义</th><th style="text-align: left;">说明</th><th style="text-align: left;">实例</th><th style="text-align: left;">结果</th></tr><tr><td>&amp;&amp;</td><td>a&amp;&amp;b</td><td>短路与</td><td>ab全为true时，计算结果为true，否则为false。</td><td>2&gt;1&amp;&amp;3&lt;4</td><td>true</td></tr><tr><td>||</td><td>a||b</td><td>短路或</td><td>ab全为false时，计算结果为false，否则为true。</td><td>2&lt;1||3&gt;4</td><td>false</td></tr><tr><td>!</td><td>!a</td><td>逻辑非</td><td>a为true时，值为false，a为false时，值为true</td><td>!(2&gt;4)</td><td>true</td></tr><tr><td>|</td><td>a|b</td><td>逻辑或</td><td>ab全为false时，计算结果为false，否则为true</td><td>1&gt;2|3&gt;5</td><td>false</td></tr><tr><td>&amp;</td><td>a&amp;b</td><td>逻辑与</td><td>ab全为true&nbsp;时，计算结果为true，否则为false</td><td>1&lt;2&amp;3&lt;5</td><td>true</td></tr></tbody></table>



## 三元运算符(条件运算符)

```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;
//三元运算符
public class SanYuan {
    public static void main(String[] args) {
        double score = 68;
        String rs = score >= 60 ? "考试通过" : "挂科";
        System.out.println(rs);

//        需求：需要从两个整数中找出较大值
        int a = 10000;
        int b = 2000;
        int max = a >= b ? a : b;
        System.out.println(max);
    }
}

```


### 详解

执行流程：首先计算**关系变大时的值**，如果值为true，返回值1，如果值为false，返回值2。

判断符号：XX ? XX : XX


### 扩展案例

#### 求三个整数的最大值

>需求：定义三个整数，找出最大值并打印在控制台

分析：

1. 用三元运算符获取前两个整数的最大值，并用临时变量保存起来。
    * num1 > num2 ? num1 : num2;
2. 用三元运算符，让临时最大值，和第三个整数进行比较，并记录结果。
    * temp > num3 ? temp : num3;

<br>

```JAVA
package com.itheima.hello.BiliVideo.Yunsuanfu;
//三元运算符
public class SanYuan {
    public static void main(String[] args) {
        System.out.println("---------------案例----------------");
        int i = 10;
        int j = 30;
        int k = 50;
        //1.找出两个整数较大值
        int temp = i > j ? i : j;
        //2.拿出临时变量比较第三个
        int rsMax = temp > k ? temp : k;
        System.out.println(rsMax);

        System.out.println("---------扩展--------");
        int rsMax1 = i > j ? (i > k ? i: k) : (j > k ? j : k);
        System.out.println(rsMax1);
    }
}
```


## 运算符优先级问题

所有的数学运算都认为是从左向右运算的，Java 语言中大部分运算符也是从左向右结合的，只有单目运算符、赋值运算符和三目运算符例外，其中，单目运算符、赋值运算符和三目运算符是从右向左结合的，也就是从右向左运算。

乘法和加法是两个可结合的运算，也就是说，这两个运算符左右两边的操作数可以互换位置而不会影响结果。运算符有不同的优先级，所谓优先级就是在表达式运算中的运算顺序。

一般而言，单目运算符优先级较高，赋值运算符优先级较低。算术运算符优先级较高，关系和逻辑运算符优先级较低。多数运算符具有左结合性，单目运算符、三目运算符、赋值运算符具有右结合性。

Java 语言中运算符的优先级共分为 14 级，其中 1 级最高，14 级最低。在同一个表达式中运算符优先级高的先执行。表 1 列出了所有的运算符的优先级以及结合性。

<table border="1"><caption>表1运算符的优先级</caption><tbody><tr><th>优先级</th><th>运算符</th><th>结合性</th></tr><tr><th>1</th><td>()、[]、{}</td><td>从左向右</td></tr><tr><th>2</th><td>!、+、-、~、++、--</td><td>从右向左</td></tr><tr><th>3</th><td>*、/、%</td><td>从左向右</td></tr><tr><th>4</th><td>+、-</td><td>从左向右</td></tr><tr><th>5</th><td>«、»、&gt;&gt;&gt;</td><td>从左向右</td></tr><tr><th>6</th><td>&lt;、&lt;=、&gt;、&gt;=、instanceof</td><td>从左向右</td></tr><tr><th>7</th><td><sub>==、!=</sub></td><td>从左向右</td></tr><tr><th>8</th><td>&amp;</td><td>从左向右</td></tr><tr><th>9</th><td>^</td><td>从左向右</td></tr><tr><th>10</th><td>|</td><td>从左向右</td></tr><tr><th>11</th><td>&amp;&amp;</td><td>从左向右</td></tr><tr><th>12</th><td>||</td><td>从左向右</td></tr><tr><th>13</th><td>?:</td><td>从右向左</td></tr><tr><th>14</th><td>=、+=、-=、*=、/=、&amp;=、|=、^=、~=、«=、»=、&gt;&gt;&gt;=</td><td>从右向左</td></tr></tbody></table>


使用优先级为 1 的小括号可以改变其他运算符的优先级，即如果需要将具有较低优先级的运算符先运算，则可以使用小括号将该运算符和操作符括起来。例如下面的表达式：

`(x-y)*z/5`

在这个表达式中先进行括号内的减法运算，再将结果与 z 相乘，最后将积除以 5 得出结果。整个表达式的顺序按照从左向右执行，比较容易理解。


再来看一个复杂的表达式，如下所示:

`--y || ++x && ++z;`

这个表达式中包含了算术运算符和逻辑运算符。根据表中列出的优先级，可以确定它的执行顺序如下：
1. 先计算 y 的自减运算符，即 --y。
2. 再计算 x 的自增运算符，即 ++x。
3. 接着计算 z 的自增运算符，即 ++z。
4. 由于逻辑与比逻辑或的优先级高，这里将 ② 和 ③ 的结果进行逻辑与运算，即 ++x && ++z。
5. 最后将 ④ 的结果与 ① 进行逻辑或运算，即 --y||++x&&++z。

如果没有上述对该表达式执行顺序的说明，第一眼看到它时将很难识别优先级。对于这类问题，可以通过添加小括号使表达的顺序更加清晰，而不用去查优先级表。如下所示为改进后的表达式。

`(--y)||((++x)&&(++z));`

<font color="blown">技巧</font>：记住这么多运算符的优先级是比较困难的，因此读者应该在实际应用中多多练习。


因为 Java 运算符存在这种优先级的关系，因此在做 SCJP 的时候或者某些公司的面试题，有如下 Java 代码：
```java
int a = 5;
int b = 4;
int c = a++- --b*++a/b-- >>2%a--;
```
问 c 的值是多少？这样的语句实在太恐怖了，即使多年的老程序员看到这样的语句也会眩晕。这样的代码只能在考试中出现，作为一个程序员如果写这样的代码，恐怕他马上就得走人了，因为他完全不懂程序开发。

源代码就是一份文档，源代码的可读性比代码运行效率更重要。 因此在这里要提醒大家：
* 不要把一个表达式写得过于复杂，如果一个表达式过于复杂，则把它分成几步来完成。
* 不要过多地依赖运算符的优先级来控制表达式的执行顺序，这样可读性太差，尽量使用()来控制表达式的执行顺序。


## 拆分三位数

```java
package com.itheima.hello.BiliVideo.Yunsuanfu;

public class OperatorTest2 {
    public static void main(String[] args) {
        //需求：拆分3位数

        int date = 589;

        //个位
        int ge = date % 10;
        System.out.println(ge);

        //十位
        int shi = date / 10 % 10;
        System.out.println(shi);

        //百位
        int bai = date / 100;
        System.out.println(bai);
    }
}
```