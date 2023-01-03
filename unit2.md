# Unit 2
### Notes:
Vocab: 
- programming paradigm that organizes software design around objects
- compartmentalize data and functions in such a way that data and the functions that operate on the data are bound together
- Classes: template or blueprint from which objects are created
    - initialized by calling class conductor
- Objects: created under the same class will share common methods and attributes.

Ex:
// TO DO #1: Instigate a Painter object called myPainter
Painter myPainter = new Painter();


Method declaration:
Access modifier: Public, protected, private, or default (lack of modifier)
Return type: The data type returned by the method. If there is no return value, this will be “void.”
Method name: The name of the method
Parameter list: The list of variables the method will operate on, enclosed in parentheses
Exception list: List of exceptions you expect during program runtime (i.e. exceptions the method should throw)
Method body: The code the method will run on execution, enclosed in curly brackets

Calling a method looks something like the below:
	methodName(parameter1, parameter2);

Alternatively, to call an object’s method:
	objectReference.methodName(parameter1, parameter2);

