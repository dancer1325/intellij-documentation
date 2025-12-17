[//]: # (Source: https://www.jetbrains.com/help/idea/surrounding-blocks-of-code-with-language-constructs.html)
[//]: # (Downloaded: 2025-12-17 20:03:40)

## Example

In the following example, we select the `int number = scanner.nextInt();` Java statement and apply the try / catch surround statement to it. 

import java.util.Scanner; public class Main { public static void main(String[] args) { Scanner scanner = new Scanner(System.in); System.out.print("Enter a number: "); int number = scanner.nextInt(); System.out.println("You entered: " + number); } } 

import java.util.Scanner; public class Main { public static void main(String[] args) { Scanner scanner = new Scanner(System.in); System.out.print("Enter a number: "); int number = 0; try { number = scanner.nextInt(); } catch (Exception e) { throw new RuntimeException(e); } System.out.println("You entered: " + number); } } 
