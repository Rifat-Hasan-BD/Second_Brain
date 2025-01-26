1. Resource [Youtube](https://youtu.be/PaPN51Mm5qQ?si=CuTLLJfSioPT7LBU)
2. Website [Link](www.cc4e.com)

* C programming language is inspired by a language called "B"
* Whitespace ignored
* Not object oriented at all
* Manual memory management
* 1970's

* Boolean operators
  * &&(double ampersand), !(bang), || (and, not, or)
* C for loops are indeterminant (i.e. no "for...in" exist in C)
* C has no pre defined True or False
* None and Null are similar concepts in python and C but quite different
* String and character arrays are sinilar concepts in python and C but **very** different
* C has no list, or dict like python
* Python has no struct, float in python is a C double
* There is a major difference between single quote and double quote
  * Single quote's are single character
  * Double quote's are array of characters with terminating 0 at the end. (not string)
    * So "Banana" is not 6 but 7 character with a 0 at the end.
* In python new line added automatically but in C new line need to added manually.

## Print Hello World
```
#include<stdio.h>

int main() {
    printf("Hello world");
}
```
If you want new line after Hello World, you simply need to add **\n** inside the string like this,
```
#include<stdio.h>

int main() {
    printf("Hello world\n");
}
```

## Argument "%d"
If you want to concatenate integer into a string and print it, you can use **%d** like this,
```
#include<stdio.h>

int main() {
    printf("Hello world in %d Year.",2025);
}
```
Output
> Hello world in 2025 Year.

So, mainly **%d** is saying "There is a integer value after coma, convert the integer value into string and concatenate it here."

## Argument "%s"
If we need to concatenate a string into another string then we use **%s** like this,
```
#include<stdio.h>

int main() {
    printf("Happy %s Year.","New");
}
```
Output
> Happy New Year.

So %s says my parameter need's to be a array of character properly terminated by 0 (means string).

## Argument "%.nf"
For concatenating flooting number we have **%.nf** where n is the length of flooting number. Let's see an example,
```
#include<stdio.h>

int main() {
    printf("The price is %.1f doller.",5.789);
}
```
Output
> The price is 5.8 doller.

Although we have (5.789) three flooting number after 5, but **%.1f** round up the flooting number in one digit precision and conver into string and concatinate it.
We can take two or more flooting number by changing the value like this **%.2f**.
Example,
```
#include<stdio.h>

int main() {
    printf("The price is %.2f doller.",5.789);
}
```
Output
> The price is 5.79 doller.

You use multiple percent thing like this,
```
#include<stdio.h>

int main() {
    printf("The price of %s in %d is %.2f $","Banana",2025,5.789);
}
```
Output
> The price of Banana in 2025 is 5.79 $

## Function
```
#include<stdio.h>

int main() {
    int multVal();
    int retVal;

    retVal=multVal(2,31);
    printf("Answer: %d .",retVal);
}

int multVal(a,b)
    int a,b;
{
    int c = a * b;
    return c;
}
```
