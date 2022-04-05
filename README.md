# Write-a-program-to-solve-quadratic-equation-2-ax2-bx-c-0.
Write a program to solve quadratic equation 2: ax2 + bx + c = 0.
package vn.viettuts.baitap;
  
import java.util.Scanner;
  
/**
 * The quadratic equation 2
 *
 * @author viettuts.vn
 */
public class PhuongTrinhBac2 {
    private static Scanner scanner = new Scanner(System.in);
    /**
     * main
     *
     * @param args
     */
    public static void main(String[] args) {
        System.out.print("Enter the quadratic coefficient, a = ");
        float a = scanner.nextFloat();
        System.out.print("Enter the coefficient of order 1, b = ");
        float b = scanner.nextFloat();
        System.out.print("Enter a free constant, c = ");
        float c = scanner.nextFloat();
        stagePTBac2(a, b, c);
    }
      
    /**
     * Solve quadratic equation 2: ax2 + bx + c = 0
     *
     * @param a: coefficient of order 2
     * @param b: coefficient of order 1
     * @param c: free term
     */
    public static void periodPTBac2(float a, float b, float c) {
        // check the coefficients
        if (a == 0) {
            if (b == 0) {
                System.out.println("Equation has no solution!");
            } else {
                System.out.println("Equation has one solution: "
                        + "x = " + (-c / b));
            }
            return;
        }
        // calculate delta
        float delta = b*b - 4*a*c;
        float x1;
        float x2;
        // calculate test
        if (delta > 0) {
            x1 = (float) ((-b + Math.sqrt(delta)) / (2*a));
            x2 = (float) ((-b - Math.sqrt(delta)) / (2*a));
            System.out.println("Equation with 2 solutions is: "
                    + "x1 = " + x1 + " and x2 = " + x2);
        } else if (delta == 0) {
            x1 = (-b / (2 * a));
            System.out.println("Equation with double solutions: "
                    + "x1 = x2 = " + x1);
        } else {
            System.out.println("Equation has no solution!");
        }
    }
}
