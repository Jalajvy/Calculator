# Calculator
import java.util.Scanner;

public class BasicCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

   System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();

  System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();

   System.out.print("Enter the operation (+, -, *, /): ");
        char operation = scanner.next().charAt(0);

   double result = 0;

  switch (operation) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error: Cannot divide by zero.");
                    return;
                }
                break;
            default:
                System.out.println("Error: Invalid operation");
                return;
        }

   System.out.println("Result: " + result);
    }
}
```

Copy and paste this code into a Java file (e.g., `BasicCalculator.java`) and run it. The program will prompt you to enter two numbers and the operation you want to perform (+, -, *, /). It will then display the result of the calculation. Note that division by zero is handled to avoid errors.
