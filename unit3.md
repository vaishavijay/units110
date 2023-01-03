# Unit 3

### Boolean Expressions: def: represent logic and tell whether something is true or false
Operators used to create Booleans:
                    - == (same value/equals to)
                    - != (checks for inequality)
                    - < (less than)
                    - <= (less than or equal to)
                    - > (greater than)
                    - >= (greater than or equal to)

Example: (a%2) == 0
Is the variable "a" even?


### If Statements and Control Flow
Conditional Statements: perform computations depending on whether a Boolean condition evaluates to true or false
If Statements: if statement occurs if a block of code is run only if the condition is true

public static boolean isEven(int number) }
if (number % 2 == 0) {
return true;
}
return false
}

### If-Else Statements: statement to run a block of code among more than one alternative

public static void main(String[] args) {
int user = 17;
if (user <= 18) {
System.out.println(“User is 18 or younger”);
}
else {
System.out.println(“User is older than 18);
}
}

### Else-if Statements: statement to run a condition if the original condition was false

int time = 15;
if (time > 21) { // 9 PM to 4 AM
System.out.println("Good night");
7
else if (time > 17) {// 5 PM to 9 PM
System.out.println("Good evening");
}
else if (time > 12) { // 12 PM to 5 PM
System.out.println("Good afternoon");
1
else if (time > 4) {// 4 AM to 12 PM
System.out.println("Good morning");
1
else { // 12 AM to 4 AM
System.out.println("Good night");
}


### Compound Boolean Expressions
Nested if statements: If-statements within if-statements
Note: If the outer if-statement evaluates to false, the inner if-statements are not evaluated.
Logical operators: Used to combine Boolean expressions
&&: and
|| : or
! : not 
Short-circuited evaluation: The result of a compound Boolean expression can be determined just by looking at a few expressions

boolean cloudy = true;
boolean rainy = false;

if (!cloudy && !rainy) {
System.out.println(“Don’t forget to bring a hat!”);
}

### Compound Boolean Expressions
De Morgan's laws: Help simplify Boolean expressions
!(a&&b) = (!a || !b)
!(a || b) = (!a && !b)

Truth tables are a good way to visualize Boolean identities

### Comparing Objects
Use '==' to see if two object references are aliases for the same object or to see if an object is null
Use '.equals()' to see if the attributes of two objects are the same

Vehicle car = new Vehicle("blue", 4);
Vehicle car2 = new Vehicle("blue", 4); 
Vehicle bluecar = car;

car == car2     False
car == bluecar   True
car.equals(car2)  True

