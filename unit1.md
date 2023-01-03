# Unit 1

Java:
- code must be in main method, use System.out.print();
- comment code with //
 Hacks
public class Printing {
	public static void man(String[] args) {
		System.out.print(“Vaishavi”);
		System.out.println(“Team “JuiceWRLD);
        	System.out.println(“Rebecca, Lin, Divya”);
		}
	}
Printing.main(null);

Data Types:
* Integer (int): for whole numbers
* Double (double): for numbers with decimals
* Boolean (boolean): for true or false conditionals

Hack:

public class Biodata {

    public static void main(String[] args) {

	int age = 17;
        double height = 63.75;
        final boolean senior = true;
        String name = “Vaishavi is a senior”;

        System.out.println(age);
        System.out.println(height);
        System.out.println(name + senior);

    }
}

Biodata.main(null);

Operators:
Main ones are +, -, *, /
- Dividing integers, it always rounds down because output must be an integer
- Dividing by 0, will get the ArithemticException Error

Hack:

public class Operators {

    public static void main(String[] args) {
int number = 2;
        int number2 = 5;
        double number3 = 2.0;
        double number4 = 5.0;

        System.out.println(number+number2);
        System.out.println(number3+number4);
        System.out.println(number-number2);
        System.out.println(number3-number4);
        System.out.println(number * number2);
        System.out.println(number3 * number4);
        System.out.println(number/number2);
        System.out.println(number3/number4);
        System.out.println(number4 % number3);
        System.out.println(number2 % number);
    }
}

Operators.main(null);

Assignment operators (as per website, for notes/reference):
* += adds value of a variabe to another variable and assigns total value to first variable
* -= subtracts value of a variabe to another variable and assigns total value to first variable
* *= multiplies value of a variabe to another variable and assigns total value to first variable
* /= multiplies value of a variabe to another variable and assigns total value to first variable
* %= takes the remainder of a variable with a second variable and assigns remainder to first variable
* ++ increments a variable by 1, to incrememt by more change second plus to number which you want to incrememnt by
* -- subracts a variable by 1, to incrememt by more change second plus to number which you want to subtract by

