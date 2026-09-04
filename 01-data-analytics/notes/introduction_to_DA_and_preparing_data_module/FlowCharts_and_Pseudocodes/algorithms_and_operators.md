Subtopic 2 — Algorithms and Operators
1. What is an Algorithm?

An algorithm is a finite, step-by-step set of instructions used to solve a problem or perform a task.

For example, an algorithm to determine whether a number is positive:

START
   ↓
INPUT number
   ↓
Is number > 0?
   ↓
YES → Display "Positive"
   ↓
NO → Display "Not positive"
   ↓
END

An algorithm should generally be:

Clear — each step is understandable.
Ordered — steps occur in the correct sequence.
Finite — it eventually ends.
Unambiguous — each step has a clear meaning.
Effective — it actually solves the intended problem.
2. What Are Operators?

Operators are symbols or keywords used to perform operations on values.

For example:

10 + 5

Here:

10 and 5 are operands
+ is the operator

The result is:

15
3. Arithmetic Operators

Arithmetic operators perform mathematical calculations.

Operator	Meaning	Example	Result
+	Addition	10 + 3	13
-	Subtraction	10 - 3	7
*	Multiplication	10 * 3	30
/	Division	10 / 3	3.333...
//	Floor division	10 // 3	3
%	Modulus/remainder	10 % 3	1
**	Exponentiation	2 ** 3	8
Important: %

The modulus operator gives you the remainder.

10 % 3

3 goes into 10 three times, with 1 left over.

Therefore:

10 % 3 = 1

This is very useful for checking whether a number is even or odd:

number % 2 == 0

If true → even.

4. Comparison Operators

Comparison operators compare two values.

They produce a Boolean result:

True

or

False
Operator	Meaning	Example
==	Equal to	5 == 5 → True
!=	Not equal to	5 != 3 → True
>	Greater than	5 > 3 → True
<	Less than	3 < 5 → True
>=	Greater than or equal to	5 >= 5 → True
<=	Less than or equal to	3 <= 5 → True
Important distinction
=

means assignment.

x = 10

means:

Put 10 into x.

But:

==

means comparison.

x == 10

means:

Is x equal to 10?

This distinction is extremely important in programming.

5. Logical Operators

Logical operators combine or modify conditions.

The three major logical operators in Python are:

and
or
not
AND

Both conditions must be true.

age >= 18 and age <= 35

This is true only if both conditions are true.

OR

At least one condition must be true.

age < 18 or age > 65
NOT

Reverses a Boolean value.

not True

becomes:

False
6. Operators in Algorithms

Operators allow algorithms to make calculations and decisions.

Example:

Determine whether a student passed.

INPUT marks

IF marks >= 50
    DISPLAY "Pass"
ELSE
    DISPLAY "Fail"

Here:

>=

is a comparison operator.

The algorithm uses it to make a decision.

7. Operator Precedence

When an expression contains multiple operators, some operations happen before others.

For example:

2 + 3 * 4

Multiplication happens first:

2 + 12

Therefore:

14

not 20.

A simplified order to remember is:

()
↓
**
↓
*, /, //, %
↓
+, -
↓
comparisons
↓
not
↓
and
↓
or

Parentheses can be used to control the order:

(2 + 3) * 4

Result:

20
8. Operators + Conditions

This is where operators become especially important for conditional statements, which you'll study next.

Example:

temperature = 35

temperature > 30

Result:

True

The comparison operator > creates a condition that can be used by an if statement.