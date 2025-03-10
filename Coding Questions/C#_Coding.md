# Program for beginners

### 1 . Area of rectangle

- Area of Rectangle == length \* breadth
  > Logic to Calculate the Area of Rectangle in C#
- First We will define the length and breadth of the rectangle.
- Then we will define the area of rectangle A.
- Then calculate the area of the rectangle by multiplying the length(L) and breadth(B).
- After multiplying result will assign in A and show the output.

```C#
using System;
namespace Code_Practise
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Enter the length of the Rectangle");
            double length = double.Parse(Console.ReadLine());
            Console.WriteLine("Enter the breadth of the Rectangle");
            double Breadth = double.Parse(Console.ReadLine());
            double Area = length * Breadth;
            Console.WriteLine($"The area of the rectangle is: {Area}");
        }
    }
}
//Enter the length of the Rectangle
//12
//Enter the breadth of the Rectangle
//15
//The area of the rectangle is: 180
```

### 2 . Area of Triangle

- Area of Triangle == 1/2 _ base _ height : This id for right angle triangle.
- first we have to calculate the value of s = (Side a + Side b + Side c) / 2
- Area of triangle = Square root of (s _ (s - Side a) _ (s - Side b) \* (s - Side c))

```C#
using System;
namespace Code_Practise
{
    internal class Program
    {
        static void Main(string[] args)
        {
            double s;
            double side1 = 1.2;
            double side2 = 2.2;
            double side3 = 2.5;
            s = (side1 + side2 + side3) / 2;
            Double areaTriangle = Math.Sqrt(s * (s - side1) * (s - side2) * (s - side3));
            Console.WriteLine(areaTriangle);
            Console.Read();
        }
    }
}
// Output : 1.3199786930098534
```

### 3. Area of circle

- Area of circle == pi _ radius _ radius
- First we have to calculate the value of pi.
- Area of circle = pi _ radius _ radius

```C#
using System;
namespace Code_Practise
{
    internal class Program
    {
        static void Main(string[] args)
        {
            double radius = 5;
            double areaCircle = Math.PI * radius * radius;
            Console.WriteLine(areaCircle);
            Console.Read();
        }
    }
}
// Output : 78.53981633974483
```

### 4. Swapping of two numbers

```C#
using System;
using System.ComponentModel.Design;
namespace Code_Practise
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int firstNumber = 10;
            int lastNumber = 20;
            int temp = 0;
            temp = firstNumber; ;
            firstNumber = lastNumber;
            lastNumber = temp;
            Console.WriteLine($"Swapped first number : {firstNumber} , Swapped second number : {lastNumber}");
            method2();
        }
         static void method2()
        {
            int number1 = 10, number2 = 20;
            Console.WriteLine($"Before SWapping number1= {number1}, number2 = {number2}");
            number1 = number1 * number2; //number1=200 (10*20)
            number2 = number1 / number2; //number2=10 (200/20)
            number1 = number1 / number2; //number1=20 (200/10)
            Console.WriteLine($"After swapping number1= {number1}, number2 = {number2}");
            Console.ReadKey();
        }
    }
}
// Output : Swapped first number : 20 , Swapped second number : 10
// Before SWapping number1= 10, number2 = 20
// After swapping number1= 20, number2 = 10
```

- you can use subtraction and addition to swap the numbers.

### 5. Fibonacci Series

- Definition : Sequence of numbers where each number is the sum of the two previous numbers. 0, 1, 1, 2, 3, 5, 8, 13 -----.

```C#
using System;
namespace Code_Practise
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int firstNumber = 0; int SecondNumber = 1; int numberOfElements = 7,nextNumber;
            if(numberOfElements <2)
            {
                Console.WriteLine("fibonacci series 0, 1");
            }
            else
            {
                Console.Write(firstNumber + " " + SecondNumber + " ");
                for (int i = 2; i < numberOfElements; i++)
                {
                    nextNumber = firstNumber + SecondNumber;
                    Console.Write(nextNumber + " ");
                    firstNumber = SecondNumber;
                    SecondNumber = nextNumber;
                }
            }
        }
    }
}
// Output : 0 1 1 2 3 5 8
```

### 6. Prime No

```C#
static void Main(string[] args)
{
    int checkNumber = 10;
    for(int i = 2; i < checkNumber; i++)
    {
        int result = checkNumber % i;
        if(result == 0)
        {
            Console.WriteLine($"{checkNumber} is not a Prime number");
            return;
        }
    }
    Console.WriteLine($"{checkNumber} is a Prime number");
}
// 10 is not a Prime number
```

### 7. Palindrome Number:

> In case of Numerical values, a number is said to be a palindrome number if the reverse of that number is the same as the original number.

```C#
static void Main(string[] args)
{
    int checkNumber = 121;
    int reverseNumber = 0;
    int remainder;
    int originalNumber = checkNumber;
    while (checkNumber != 0)
    {
        remainder = checkNumber % 10;
        reverseNumber = reverseNumber * 10 + remainder;
        checkNumber /= 10;
    }
    if (originalNumber == reverseNumber)
    {
        Console.WriteLine($"{originalNumber} is a Palindrome number");
    }
    else
    {
        Console.WriteLine($"{originalNumber} is not a Palindrome number");
    }
}
// 121 is a Palindrome number
```

```C#
static void Main(string[] args)
{
    int sum = 0;
    int checkNumber = int.Parse(Console.ReadLine());
    int checkNumber2 = checkNumber;
    int numberLength = checkNumber.ToString().Length;
    for(int i= 0; i < numberLength; i++)
    {
        int alternateNumber = checkNumber % 10;
        checkNumber = checkNumber / 10;
        sum = (sum * 10 ) + alternateNumber;
    }
    if (sum == checkNumber2)
    {
        Console.WriteLine($"{checkNumber2} is a palindrome");
    }
    else { Console.WriteLine($"{checkNumber2} is not a Plinndrome"); }
}
// 1234321 is a palindrome
```

> In case of String values, a string is said to be a palindrome if the reverse of that string is the same as the original string.

```C#
static void Main(string[] args)
{
    string checkString = "madam";
    string reverseString = "";
    for (int i = checkString.Length - 1; i >= 0; i--)
    {
        reverseString += checkString[i];
    }
    if (checkString == reverseString)
    {
        Console.WriteLine($"{checkString} is a Palindrome");
    }
    else { Console.WriteLine($"{checkString} is not a Palindrome"); }
}
```

### 8. Armstrong Number

- An Armstrong Number is a number that is equal to the sum of, power of each digit by the total number of digits. For example, the numbers such as 0, 1, 153, 370, 371, and 407, 1634, 8208, 9474 are Armstrong numbers.

```C#
static void Main(string[] args)
{
    Console.WriteLine("Enter a Number");
    int number = int.Parse(Console.ReadLine());
    int checkNumber = number;
    int length = checkNumber.ToString().Length;
    int sum = 0;
    while (number > 0)
        {
            int newNumber = (int)Math.Pow(number % 10 , length);
            sum = sum + newNumber;
            number = number / 10;
        }
    if(checkNumber == sum)
    {
        Console.WriteLine($"{checkNumber} is armstrong no ");
    }
    else { Console.WriteLine($"{checkNumber} is not a armstrong no ");}
}
// 153 is armstrong no
```

### 9. Factorial Number

> Using For loop

```C#
static void Main(string[] args)
{
    Console.WriteLine("Please enter a no for factorial");
    int factorial = 1;
    int checkNumber = int.Parse(Console.ReadLine());
    for (int i = 1; i <= checkNumber; i++)
    {
        factorial = factorial * i;
    }
    Console.WriteLine($"factorial of no {checkNumber} : {factorial}");
}
// Please enter a no for factorial
// 5
// factorial of no 5 : 120
```

> Using While loop

```C#
static void Main(string[] args)
{
    Console.Write("Enter a Number : ");
    int number = int.Parse(Console.ReadLine());
    long factorial = 1;
    while (number >= 1)
    {
        factorial = factorial * number;
        number = number - 1;
    }
    Console.Write($"Factorial is: {factorial}");
    Console.ReadLine();
}
// Enter a Number : 5
// Factorial is: 120
```

### 10. Sum of digits in a number

> Using For loop

```C#
static void Main(string[] args)
{
    Console.Write("Enter a Number : ");
    int number = int.Parse(Console.ReadLine());
    int length = number.ToString().Length;
    int sum = 0;
    for (int i = 0; i < length; i++)
    {
        int remainder = number % 10;
        sum = sum + remainder;
        number = number / 10;
    }
    Console.WriteLine($"sum of all number : {sum}");
}
```

> using while loop

```C#
static void Main(string[] args)
{
    Console.Write("Enter a Number : ");
    int number = int.Parse(Console.ReadLine());
    int sum = 0;
    while (number > 0)
    {
        int remainder = number % 10;
        sum = sum + remainder;
        number = number / 10;
    }
    Console.WriteLine($"sum of all number : {sum}");
}
```

### 11. Decimal to binary conversion

> What are Decimal Numbers?

- The Decimal numbers are the numbers whose base is 10. That means the decimal numbers are range from 0 to 9. Any combination of such digits (digits from 0 to 9) is a decimal number such as 2238, 1585, 227, 0, 71, etc.

> What are Binary Numbers?

- The Binary numbers are the numbers whose base is 2. That means the binary numbers can be represent using only two digits i.e. 0 and 1. So, any combination of these two numbers (i.e. 0 and 1) is a binary number such as 101, 10o1, 111111, 10101, etc.
  > Algorithm: Decimal to Binary Conversion
- Step1: First, divide the number by 2 through the modulus (%) operator and store the remainder in an array
- Step2: Divide the number by 2 through the division (/) operator.
- Step3: Repeat step 2 until the number is greater than zero.

```C#
static void Main(string[] args)
{
    Console.WriteLine("Enter a no to convert into decimal");
    int number = int.Parse(Console.ReadLine());
    string result = string.Empty;
    for (int i = 0; number > 0 ; i++)
    {
        result = number % 2 + result;
        number = number / 2;
    }
    Console.WriteLine($"converted binary no : {result}");
}
// Enter a no to convert into decimal
// 5
// converted binary no : 101
```

### 12. Binary to decimal conversion
- first, we extract the digits of a given binary number starting from the rightmost digits using the modulus operator. Once we extract the number, then we multiply the digit with the proper base i.e. power of 2 and add the result into the decimal value variable. In the end, the decimal value variable will hole the required decimal number.
```C#
static void Main(string[] args)
{
    Console.WriteLine("Enter a binary no to convert into decimal");
    int number = int.Parse(Console.ReadLine());
    int result = 0;
    int power = 0;
    for (int i = number.ToString().Length - 1; i >= 0; i--)
    {
        int binary = number % 10;
        result = result + binary * (int)Math.Pow(2, power);
        number = number / 10;
        power++;
    }
    Console.WriteLine($"converted decimal no : {result}");
}
// Enter a binary no to convert into decimal
// 101
// converted decimal no : 5
```
> With the help of inbuilt methods
```C#
static void Main(string[] args)
{
    Console.Write("Enter the Binary Number : ");
    int binaryNumber = int.Parse(Console.ReadLine());
    int decimalValue = Convert.ToInt32(binaryNumber.ToString(), 2);
    Console.Write($"Decimal Value : {decimalValue} ");
    Console.ReadKey();
}
```
### 13. Character Occurrence in a String
- Check the length of the input message and if it is greater than 0, then using for loop we calculate the number of occurrences of each character.
```Csharp
public static void characterOccuranceString()
{
    Console.WriteLine("Please enter a string to check occurance");
    string valueString = Console.ReadLine();
    int countChar  = 0;
    for (int i = 0; i < valueString.Length; i++)
    {
        countChar += 1;
    }
    Console.WriteLine($"{countChar} is the count of given value!");
}
```


### 16.	How to reverse the order of words in a given string.
```Csharp
public static void ReverseOrderofWords()
{
    string input = "Hello World from C#";
    string reversedString = "";
    int end = input.Length;

    for (int i = input.Length - 1; i >= 0; i--)
    {
        if (input[i] == ' ' || i == 0)
        {
            int start = (i == 0) ? i : i + 1;
            for (int j = start; j < end; j++)
            {
                reversedString += input[j];
            }
            if (i > 0)
            {
                reversedString += " ";
            }
            end = i;
        }
    }

    Console.WriteLine(reversedString);
}
// C# from World Hello
```
### 17.	How to reverse each word in a given string.
```CSharp
public static void reverseEachWord()
{
    string valueString = "Hello from C# ";
    string reversedValueString = "";
    int start = 0;
    for (int i =0 ; i < valueString.Length; i++)
    {
        if (valueString[i] == ' ' )
        {
            int end = i;
            for (int j = end  -1; j >= start; j --)
            {
                reversedValueString += valueString[j];
            }
            reversedValueString += " ";
            start = end  + 1;
        }
    }
    Console.WriteLine(reversedValueString);
}
// olleH morf #C
```
### 18.	How to count the occurrence of each character in a string.
```CSharp
public static void countEachWord()
{
    string valueString = "Hello from C# ";
    int start = 0;
    for (int i =0 ; i < valueString.Length; i++)
    {
        if (valueString[i] == ' ' )
        {
            int count = i - start; 
            Console.Write(count + ",");
            start = i + 1; 
        }
    }
}
// 5,4,2
```
### 19.	How to remove duplicate character from a string.
### 20.	How to find all possible substring of a given string.
### 21.	How to perform left circular rotation of an array.
### 22.	How to perform right circular rotation of an array.
### 23.	How to find if a positive no is a prime no or not.
### 24.	How to find sum digit of a positive integer.
### 25.	How to find second largest integer in an array using only one loop.
### 26.	How to find third largest integer in an array using only one loop.
### 27.	How to convert a two-dimensional array into a one-dimensional array.
### 28.	How to convert one-dimensional array into a two-dimensional array.
### 29.	How to find the angle between hour and minute hands of a clock at any given time.