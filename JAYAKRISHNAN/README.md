### PROGRAM STATEMENT
  Given a signed 32-bit integer x, return x with its digits reversed. If reversing x causes the value to go outside the signed 32-bit integer range [-231, 231 - 1], then return 0.

### PROGRAM :
 ```java
import java.util.Scanner;
class Solution {
    public int reverse(int x) {
        long rev = 0;
        while (x != 0) {
            int rem = x % 10;
            rev = rev * 10 + rem;
            x /= 10;
        }
        if (rev > Integer.MAX_VALUE || rev < Integer.MIN_VALUE) {
            return 0;
        }
        return (int) rev;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an integer: ");
        int input = scanner.nextInt();
        Solution solution = new Solution();
        int result = solution.reverse(input);
        System.out.println("Reversed number: " + result);
        
    }
}

 ```  
### OUTPUT :

![alt text](image.png) 