Download Link: https://assignmentchef.com/product/solved-hw11-java-programming
<br>
1. Some of the number systems used frequently include binary, octal, decimal and hexadecimal systems. Some sample numbers:

base 10     base 2      base 8      base 16

0           0           0           0

1           1           1           1

2           10          2           2

7           111         7           7

8           1000        10          8

9           1001        11          9

10          1010        12          A

11          1011        13          B

15          1111        17          F

16          10000       20          10

Look up web sites like http://www.tutorialspoint.com/computer_fundamentals/computer_number_system.htm

for more information about these systems.

Write and implement the following Java methods:

bToD(String b) //convert binary string b to an equivalent decimal string.

bToO(String b) //convert binary string b to an equivalent octal string.

bToH(String b) //convert binary string b to an equivalent hexadecimal string.

dToB(String d) //convert decimal string d to an equivalent binary string.

oToB(String o) //convert octal string o to an equivalent binary string.

hToB(String h) //convert hexadecimal string h to an equivalent binary string.

convert(int baseFrom, int baseTo, String n) // method to convert n given in baseFrom system to an equivalent number in baseTo system calling two of the above methods needed for conversion. If baseFrom = 10 and baseTo = 16, for example, method convert() will call dToB() followed by bToH() . You may assume that variables baseFrom and baseTo hold 2,8,10, or 16 only, and string n holds a number written in baseFrom system.

* Call the following methods(done in Hw9) from bToD(String b) and dToB(String d) methods appropriately:

String multiply2(String n) { //return 2*n

String r = “”;

int c = 0;

for (int i = n.length()-1; i &gt;= 0; i–) {

int p = (n.charAt(i)-‘0’)*2+c;

c = p/10;

r = p%10+r;

}

if (c &gt; 0)

r = c+r;

return r;

}




String divide2(String n) { //return n/2

String r = “”;

int b = 0;

int i = 0;

if (n.charAt(0) &lt; ‘2’) {

b = 1;

i = 1;

}

for (; i &lt; n.length(); i++) {

int p = (n.charAt(i)-‘0’)+b*10;

b = p%2;

r += p/2;

}

if (r.length() == 0)

r = “0”;

return r;

}

The other four methods can be directly implemented manipulating input strings as illustrated in this example:

10110001101011<sub>2</sub> = 26153<sub>8</sub> = 2C6B<sub>16</sub>

* Note that input and output numbers can be very long and converting them to int or long type before base conversion will cause an overflow error.

* No built-in class or method is allowed to use in this project except:

.next(), .nextLine(), .nextInt(), .nextLong(), .nextDouble(), .nextFloat() in Scanner class;

.length(), .charAt(), .indexOf(), .substring(), .comparedTo(), .equals() in String class;

.max(), .min(), .pow(), .sqrt(), .round(), .floor(), .ceil() in Math class.

.parseInt(), .toString() in Integer class.

* Your main method should use an appropriate loop or menu to test the above methods repeatedly.