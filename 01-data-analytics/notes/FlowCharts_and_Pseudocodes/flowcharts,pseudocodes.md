Subtopic 1 — Lesson Overview: Flowcharts and Pseudocode
1. What is an algorithm?

An algorithm is a step-by-step set of instructions for solving a problem or completing a task.

Example: Making tea:

1. Boil water
2. Put tea in cup
3. Pour hot water
4. Add milk/sugar
5. Stir

In programming, algorithms tell the computer what steps to perform and in what order.

2. What is programmatic thinking?

Programmatic thinking means approaching a problem in a way that can be translated into instructions a computer can execute.

You generally need to:

Problem
   ↓
Break it into steps
   ↓
Identify decisions
   ↓
Identify inputs and outputs
   ↓
Create an algorithm
   ↓
Implement it in code
3. What is a flowchart?

A flowchart is a visual representation of an algorithm.

Instead of writing:

Get number
Check if number > 0
If yes → positive
If no → not positive

you represent the logic using symbols and arrows.

Common flowchart symbols
Symbol	Meaning
Oval	Start / End
Rectangle	Process / Action
Diamond	Decision
Parallelogram	Input / Output
Arrow	Direction of flow

The diamond is especially important because it represents a decision.

Example:

        START
          ↓
     Enter number
          ↓
    Is number > 0?
       ↙       ↘
     YES        NO
      ↓          ↓
  "Positive"  "Not positive"
       ↘       ↙
          END
4. What is pseudocode?

Pseudocode is a way of writing an algorithm using simple, human-readable language that resembles programming logic.

Example:

START
INPUT age

IF age >= 18 THEN
    DISPLAY "Adult"
ELSE
    DISPLAY "Minor"
END IF

END

It is not actual programming code.

Its purpose is to help you design the logic before writing the real code.

5. Flowchart vs Pseudocode
Flowchart	Pseudocode
Visual	Text-based
Uses symbols	Uses structured statements
Shows flow using arrows	Shows logic using words
Easy to visualize	Easy to convert into code

Think:

Flowchart = draw the algorithm

Pseudocode = write the algorithm in structured English

6. Why use them?

They help you:

Understand a problem before coding
Organize your logic
Identify missing steps
Find logical errors
Communicate your solution
Convert a problem into actual code more easily


Subtopic 3 — Flowcharts and Pseudocode

This topic builds directly on what you've already learned. The goal is to be able to take a problem, design the logic, represent it visually with a flowchart, and write it as pseudocode.

1. Flowcharts

A flowchart is a graphical representation of an algorithm.

It shows:

What happens first
What happens next
Where decisions occur
What happens when a condition is true or false
Where the algorithm starts and ends
Basic flow
START
  ↓
INPUT
  ↓
PROCESS
  ↓
OUTPUT
  ↓
END
2. Important Flowchart Symbols
Start / End — Oval
   ┌─────────┐
  (  START   )
   └─────────┘

Used to indicate where an algorithm begins or ends.

Process — Rectangle

Used for an action or calculation.

┌─────────────────┐
│ total = price*x │
└─────────────────┘

Examples:

Calculate total
Add two numbers
Update a variable
Calculate average
Input / Output — Parallelogram

Used when the program receives or displays information.

  ╱────────────────╱
 ╱  INPUT: age    ╱
╱────────────────╱

Examples:

INPUT age
DISPLAY result
Decision — Diamond

Used when the algorithm needs to make a decision.

       /─────────\
      < age >=18? >
       \─────────/

A decision normally creates different paths such as:

        Decision
        /      \
      YES       NO
       ↓         ↓
    Process    Process
3. Arrows

Arrows show the direction of the algorithm.

For example:

START
  ↓
INPUT age
  ↓
age >= 18?
 ↙       ↘
YES      NO
 ↓        ↓
Adult   Minor
  ↘      ↙
    END

Without arrows, it would be unclear which step comes next.

4. Pseudocode

Pseudocode is a structured way of writing an algorithm using plain language.

It isn't tied to a particular programming language.

Example:

START

INPUT age

IF age >= 18 THEN
    DISPLAY "Adult"
ELSE
    DISPLAY "Minor"
END IF

END

Notice that this isn't Python, Java, or JavaScript.

It describes the logic that could later be converted into actual code.

5. Pseudocode Keywords

You will commonly see words such as:

START
END
INPUT
OUTPUT / DISPLAY
IF
ELSE
ELSE IF
END IF
WHILE
FOR

For example:

INPUT number
DISPLAY number

means:

Get a value from the user and then display it.

6. Turning a Problem into Pseudocode

Suppose the problem is:

Ask the user for two numbers and display their sum.

First identify:

Inputs:

number1
number2

Process:

sum = number1 + number2

Output:

Display sum

Pseudocode:

START

INPUT number1
INPUT number2

sum = number1 + number2

DISPLAY sum

END
7. Turning Pseudocode into a Flowchart

The same problem could become:

       START
         ↓
   INPUT number1
         ↓
   INPUT number2
         ↓
 sum = number1 + number2
         ↓
    DISPLAY sum
         ↓
        END

So:

Pseudocode and flowcharts can represent the same algorithm in different ways.

8. Decisions in Flowcharts

Consider:

If a student's mark is 50 or higher, display "Pass"; otherwise display "Fail."

Pseudocode
START

INPUT mark

IF mark >= 50 THEN
    DISPLAY "Pass"
ELSE
    DISPLAY "Fail"
END IF

END
Flowchart
             START
               ↓
          INPUT mark
               ↓
          ┌──────────┐
         < mark >= 50? >
          └──────────┘
            ↙      ↘
          YES       NO
           ↓         ↓
      DISPLAY      DISPLAY
       "Pass"       "Fail"
           ↘         ↙
              END

The diamond represents the condition.

9. Sequence, Selection and Iteration

These are three fundamental structures you'll encounter in programmatic thinking.

1. Sequence

Instructions happen one after another.

INPUT age
CALCULATE age + 1
DISPLAY result
A
↓
B
↓
C
2. Selection

The program chooses between alternatives based on a condition.

IF condition THEN
    action A
ELSE
    action B
END IF

Example:

IF age >= 18
    DISPLAY "Adult"
ELSE
    DISPLAY "Minor"
END IF
3. Iteration

A set of instructions is repeated.

For example:

FOR each student
    calculate average
END FOR

You'll learn more about loops later.

10. Flowchart vs Pseudocode

Remember this distinction:

Flowchart	Pseudocode
Visual	Written
Uses symbols	Uses structured words
Uses arrows	Uses indentation/structure
Shows flow visually	Describes logic in text
Easy to visualize	Easy to convert into code
The big idea
Problem
   ↓
Algorithm
   ↓
 ┌──────────────┐
 ↓              ↓
Flowchart    Pseudocode
 ↓              ↓
 └──────┬───────┘
        ↓
   Actual Code