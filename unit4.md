# Unit 4

### While Loops
* Repeats lines of code until a certain condition evaluates to false
* Boolean expression is checked before the loop is started and every time the loop ends and is about to start anew
    * Inside the loop something is done that slightly changes the conditions for the boolean expression until it reads false and ends

int x = 5;

// The boolean expression in this case is x > 0
while (x > 0) {
    System.out.println(x);
    x--;
}

    * In the example below, the condition is x > 0, meaning that x has to be changed for the loop to stop. Inside the loop, x is decremented by 1 every time, changing the conditions over and over again until it finally returns false and terminates the while loop

int[] array = {3, 7, 0, 2, 4, 5, 9, 1, 3, 6, 3};
int total = 0;
int i = 0;

while (i < array.length) {
    total += array[i];
    i++;
}

System.out.println(total);

- While loops lie in infinite while loops, loops that run over and over again permanently
    - Usually accomplished by setting the boolean condition to be true at all times
    - Only way to stop these loops are to use a break command, which ends the loop regardless of the conditions present

### For Loops
Three Parts of a For Loop
* Initialization of a variable
* Test condition
* The code in the initialization area is executed only one time before the loop begins
* the test condition is checked each time through the loop and the loop continues as long as the condition is true
* the loop control variable change is done at the end of each execution of the body of the loop
* When the loop condition is false, execution will continue at the next statement after the body of the loop

### Loops and Strings
String name = "CodeCodeCode";

for (int i = 0; i < name.length(); i+=2) {
    System.out.println(name.substring(i,i+2));
}

### Nested Iteration
- “Loop within loop”

for (int row = 0; row < 5; row ++) {
    for (int column = 0; column < 4; column++) {
        System.out.print('*');
    }
    System.out.println();
}

—— 
import java.util.ArrayList;

/*
 * Creator: Nighthawk Coding Society
 * Mini Lab Name: Hello Series,featuring Monkey Jumpers
 */

/**
 * Class for Monkey: a 2D array of Monkey
 * As well as method to print the Poem
 */
class Monkey {
    //The area between class definition and the 1st method is where we keep data for object in Java
    private static ArrayList<String[]> monkeyList = new ArrayList<String[]>();    //2D Array: AP CSA Unit 8: 2D array of strings
    private String[] monkeyASCII;

    /**
     * Constructor initializes a 2D array of Monkey
     */
    public Monkey(String[] monkeyASCII) {
        this.monkeyASCII = monkeyASCII;
        monkeyList.add(monkeyASCII);
    }

    /**
     * Loop and print monkey in array
     * ... repeat until you reach zero  ...
     */
    public static void printPoem() {
        //begin the poem
        System.out.println();
        System.out.println("Monkey Jumpers Poem in Java with Objects!!!");

        // monkey (non-primitive) defined in constructor knows its length
        int monkeyCount = monkeyList.size();
        for (int i = 1; i <= monkeyCount; i++)  //loops through 2D array length forwards
        {

            //this print statement shows current count of Monkey
            //  concatenation (+) of the loop variable and string to form a countdown message
            System.out.println(i + " little monkey jumping on the bed...");

            //how many separate parts are there in a monkey monkey?
            for (int row = 0; row < i; row++) {  //cycles through "cells" of 2d array

                /*cycles through columns to print
                each monkey part by part, will eventually print entire column*/
                for (int col = 0; col < monkeyList.get(row).length; col++) {

                    // prints specific part of the monkey from the column
                    System.out.print(monkeyList.get(row)[col] + " ");

                    //this is new line between separate parts
                    System.out.println();
                }
                
                //this new line gives separation between stanza of poem
                System.out.println();
            }

            //countdown for poem, decrementing monkeyCount variable by 1
            monkeyCount -= 1;
        }

        //out of all the loops, prints finishing messages
        System.out.println("Too many monkeys jumping on the bed");
        System.out.println("0000000000000000000000000000000000");
        System.out.println("             THE END              ");
    }

   
    /**
    * A Java Driver/Test method that is the entry point for execution
    */
    public static void main(String[] args)  {
        Monkey monkey0 = new Monkey(new String[]{
            "ʕง ͠° ͟ل͜ ͡°)ʔ ",      //[0][0] eyes
            "  \\_⏄_/  ",      //[0][1] chin
            "  --0--   ",       //[0][2] body
            "  ⎛   ⎞   "        //[0][3] legs
        });
        Monkey monkey1 = new Monkey(new String[]{
            " ʕ༼ ◕_◕ ༽ʔ",       //[1][0]
            "  \\_⎏_/  ",
            "  ++1++  ",
            "   ⌋ ⌊   "
        });
        Monkey monkey2 = new Monkey(new String[]{
            " ʕ(▀ ⍡ ▀)ʔ",       //[2][0]
            "  \\_⎐_/ ",
            "  <-2->  ",
            "  〈  〉 "
        });
        Monkey monkey3 = new Monkey(new String[]{
            "ʕ ͡° ͜ʖ ° ͡ʔ",        //[3][0]
            "  \\_⍾_/  ",
            "  ==3==  ",
            "  _/ \\_  "
        });
        Monkey monkey4 = new Monkey(new String[]{
            "  (◕‿◕✿) ",          //[4][0]
            "  \\_⍾_/ ",          //[4][1]
            "  ==4==  ",          //[4][2]
            "  _/ \\_ "           //[4][3]
        });

        
        Monkey.printPoem();   //a new monkey list and output in one step
    }

}

Monkey.main(null);

