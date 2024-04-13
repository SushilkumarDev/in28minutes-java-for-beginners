<!---
Current Directory : /in28Minutes/git/java-a-course-for-beginners/6-PrimitiveDataTypesAndAlternatives
-->

## Complete Code Example


### /src/com/in28minutes/primitive/datatypes/BiNumber.java

```java
package com.in28minutes.primitive.datatypes;

public class BiNumber {
	private int number1;
	private int number2;

	public int getNumber1() {
		return number1;
	}

	public void setNumber1(int number1) {
		this.number1 = number1;
	}

	public int getNumber2() {
		return number2;
	}

	public void setNumber2(int number2) {
		this.number2 = number2;
	}

	public BiNumber(int number1, int number2) {
		this.number1 = number1;
		this.number2 = number2;
	}

	public int add() {
		return number1 + number2;
	}

	public int multiply() {
		return number1 * number2;
	}

	public void doubleValue() {
		this.number1 *= 2;
		this.number2 *= 2;
	}

}
```
---
### /src/com/in28minutes/primitive/datatypes/BiNumberRunner.java

```java
package com.in28minutes.primitive.datatypes;

public class BiNumberRunner {

	public static void main(String[] args) {
		BiNumber numbers = new BiNumber(2, 3);
		
		System.out.println(numbers.add());//2+3
		System.out.println(numbers.multiply());//2*3
		
		numbers.doubleValue();//Double both numbers 
		
		System.out.println(numbers.getNumber1());//4
		System.out.println(numbers.getNumber2());//6
	}

}
```
---
### /src/com/in28minutes/primitive/datatypes/MyChar.java

```java
package com.in28minutes.primitive.datatypes;

public class MyChar {

	private char ch;

	public MyChar(char ch) {
		this.ch = ch;
	}

	public boolean isVowel() {
		//'a' e i o u or A E I O U
		if(ch == 'a' || ch == 'A')
			return true;

		if(ch == 'e' || ch == 'E')
			return true;
		
		if(ch == 'i' || ch == 'E')
			return true;
		
		if(ch == 'o' || ch == 'O')
			return true;
		
		if(ch == 'u' || ch == 'U')
			return true;
		
		return false;
	}

	public boolean isDigit() {
		if(ch >= 48 && ch <=57) //between '0' and '9'  
		  return true;
		
		return false;
	}

	public boolean isAlphabet() {
		if(ch >= 97 && ch <=122) //between 'a' and 'z'  
		  return true;

		if(ch >= 65 && ch <=90) //between 'A' and 'Z'  
			  return true;

		return false;
	}

	public boolean isConsonant() {
		//Alphabet and it is not VOWEL
		//! [a , e, i ,o , u]
		if(isAlphabet() && !isVowel()) 
			return true;
		
		return false;
		
	}

	public static void printLowerCaseAlphabets() {
		//'a' to 'z'
		for (char ch = 'a'; ch <= 'z'; ch++) {
			System.out.println(ch);
		}
	}

	public static void printUpperCaseAlphabets() {
		for (char ch = 'A'; ch <= 'Z'; ch++) {
			System.out.println(ch);
		}
		
	}
}
```
---