# SalesCommission
/*
 * Sales Commission Calculator
 */
import java.util.Scanner;

public class SalesCommission {
   public static void main(String[] args) {
      // Declare variables
      double sales, salary;    // These are double!
      double baseSalary = 200.0;
      double commissionRate = 0.09;
      int sentinel = -1;  // Terminating value for input
      Scanner in = new Scanner(System.in);

      // Read the first input, so as to compare with the sentinel value
      System.out.print("Enter sales in dollars (-1 to end): " );
      sales = in.nextDouble();   // Read double

      while (sales != sentinel) {
         // Compute the salary
         salary = baseSalary + sales*commissionRate;

         // Print results via printf()
         System.out.printf("Salary is: $" + String.format("%.2f", salary));

         // Read the next input
         // Repeat the loop, if input is not the sentinel value.
         // Take note that you need to repeat these two statements!
         System.out.printf("\n\nEnter sales in dollars (-1 to end): " );
         sales = in.nextDouble();
      }
      System.out.printf("bye");
      in.close();
   }
}
