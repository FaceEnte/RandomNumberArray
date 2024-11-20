# Random Numbers

This project involves creating a Java program that generates an array of random integers. The program will fill an integer array with random numbers between 1 and 100, with a specified size \( N \) (where \( N \leq 100 \)).

## Objective

Create a Java program that:

- Defines a class named `RandomNumbers` with a `main` method.
- Prompts the user to enter the size of the array \( N \).
- Validates that \( N \) is less than or equal to 100.
- Fills the integer array with random numbers between 1 and 100.
- Outputs the contents of the array.

### Example Implementation

```java
import java.util.Random;
import java.util.Scanner;

public class RandomNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        System.out.print("Enter the size of the array (N <= 100): ");
        int size = scanner.nextInt();

        // Validate the size
        if (size <= 0 || size > 100) {
            System.out.println("Invalid size. Please enter a number between 1 and 100.");
            scanner.close();
            return;
        }

        int[] numbers = new int[size];

        // Fill the array with random numbers between 1 and 100
        for (int i = 0; i < size; i++) {
            numbers[i] = random.nextInt(100) + 1; // random number between 1 and 100
        }

        // Output the contents of the array
        System.out.println("Random numbers array:");
        for (int number : numbers) {
            System.out.print(number + " ");
        }
        System.out.println();

        scanner.close();
    }
}
```

### Example Output

```
Enter the size of the array (N <= 100): 10
Random numbers array:
23 45 67 12 89 34 56 78 90 11
```

## Hints

- Use the `Random` class to generate random numbers.
- Use a loop to fill the array with random numbers.
- Ensure to validate the input size to prevent errors.

## Notes

- Document your code with comments to explain the logic behind filling the array and generating random numbers.
- Test the program with various inputs to ensure it behaves as expected.

Happy coding! 🎉