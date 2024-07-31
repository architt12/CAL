function documentation:
printf("Enter calculation:\n\n");:

Purpose: Prompts the user to enter a calculation in the form of valueOne operator valueTwo.
scanf("%f %c %f", &valueOne, &operator, &valueTwo);:

Purpose: Reads the user input. The format string "%f %c %f" specifies that valueOne and valueTwo are floating-point numbers, and operator is a character.
switch(operator):

Purpose: Handles different types of calculations based on the input operator.

case '/':

Operation: Division.
Code: answer = valueOne / valueTwo;
Purpose: Computes the result of dividing valueOne by valueTwo.
case '*':

Operation: Multiplication.
Code: answer = valueOne * valueTwo;
Purpose: Computes the result of multiplying valueOne by valueTwo.
case '+':

Operation: Addition.
Code: answer = valueOne + valueTwo;
Purpose: Computes the result of adding valueOne to valueTwo.
case '-':

Operation: Subtraction.
Code: answer = valueOne - valueTwo;
Purpose: Computes the result of subtracting valueTwo from valueOne.
case '^':

Operation: Exponentiation.
Code: answer = pow(valueOne, valueTwo);
Purpose: Computes the result of raising valueOne to the power of valueTwo using the pow function from <math.h>.
case ' ':

Operation: Square root of valueTwo.
Code: answer = sqrt(valueTwo);
Purpose: Computes the square root of valueTwo using the sqrt function from <math.h>. Note that this case is unusual because it does not use valueOne.
default:

Purpose: Handles invalid operators.
Code: goto fail;
Behavior: Jumps to the fail label if the operator is not recognized.
printf("%.9g%c%.9g = %.6g\n\n", valueOne, operator, valueTwo, answer);:

Purpose: Prints the result of the calculation.
Format Specifiers:
%.9g prints floating-point numbers with up to 9 significant digits.
%.6g prints the result with up to 6 significant digits.
goto fail;:

Purpose: Jumps to the fail label in case of an invalid operator.
fail:

Purpose: Handles errors and invalid input.
Code: printf("Fail.\n");
Behavior: Prints an error message if the operator is not valid.
exit:

Purpose: Terminates the program.
Code: return 0;
Behavior: Ends the program and returns a success status.
