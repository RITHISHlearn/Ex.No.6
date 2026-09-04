# Ex.No.6 AI-Assisted Programming and Debugging



# Aim

To use AI tools for generating, debugging, optimizing, and testing computer programs in Python, C, and Java, and to evaluate the effectiveness of AI-assisted programming.

# AI Tools Required

ChatGPT

# Explanation

AI coding assistants can help programmers generate source code, detect errors, improve program efficiency, explain algorithm complexity, and create test cases.

In this experiment, AI is used to solve different programming problems using Python, C, and Java. The generated programs are executed and evaluated for correctness. AI is also used for debugging, optimization, complexity analysis, and unit-test generation.

Finally, manual programming and AI-assisted programming are compared based on development time, correctness, readability, debugging, and productivity.

# AI-Assisted Programming and Debugging

## Objective

The main objective of this experiment is to understand how AI can support programmers during different stages of software development.

The experiment includes:

* Program generation
* Error identification
* Debugging
* Code optimization
* Complexity analysis
* Unit-test generation
* Comparison of manual and AI-assisted programming

---

# 1. Python Programming

### Prompt

```text
Write a Python program to calculate the average of numbers in a list.
Handle an empty list and explain the time and space complexity.
```

### AI-Generated Code

```python
def calculate_average(numbers):
    if not numbers:
        return None

    return sum(numbers) / len(numbers)


numbers = [10, 20, 30, 40, 50]

result = calculate_average(numbers)

if result is not None:
    print("Average:", result)
else:
    print("List is empty")
```

### Output

```text
Average: 30.0
```

### Complexity Analysis

* Time Complexity: `O(n)`
* Space Complexity: `O(1)` auxiliary space

The program processes all elements in the list to calculate the sum.

### Result

The AI successfully generated a Python program that calculates the average and handles an empty list safely.

---

# 2. C Programming

### Prompt

```text
Write a C program to reverse an integer number.
Handle negative numbers and explain the time and space complexity.
```

### AI-Generated Code

```c
#include <stdio.h>

int main() {
    int n, reverse = 0, remainder;

    printf("Enter a number: ");
    scanf("%d", &n);

    while (n != 0) {
        remainder = n % 10;
        reverse = reverse * 10 + remainder;
        n = n / 10;
    }

    printf("Reversed number: %d\n", reverse);

    return 0;
}
```

### Output

```text
Enter a number: 12345
Reversed number: 54321
```

### Complexity Analysis

* Time Complexity: `O(log n)`
* Space Complexity: `O(1)`

### Observation

The AI-generated program uses a loop to extract each digit and construct the reversed number.

---

# 3. Java Programming

### Prompt

```text
Write a Java program to count the number of vowels in a string.
Use an efficient approach and explain the time and space complexity.
```

### AI-Generated Code

```java
public class VowelCount {

    public static void main(String[] args) {

        String text = "Artificial Intelligence";
        int count = 0;

        for (int i = 0; i < text.length(); i++) {
            char ch = Character.toLowerCase(text.charAt(i));

            if (ch == 'a' || ch == 'e' || ch == 'i' ||
                ch == 'o' || ch == 'u') {
                count++;
            }
        }

        System.out.println("Number of vowels: " + count);
    }
}
```

### Output

```text
Number of vowels: 9
```

### Complexity Analysis

* Time Complexity: `O(n)`
* Space Complexity: `O(1)`

### Result

The AI generated a simple Java program that scans each character and counts the vowels.

---

# 4. Bug Identification and Debugging

### Prompt

```text
Find the error in the following C program.
Explain the reason for the error and provide the corrected code.

int a = 10;
int b = 0;
printf("%d", a / b);
```

### AI-Generated Analysis

The error occurs because the program attempts to divide a number by zero.

```text
a / b
```

Here:

```text
a = 10
b = 0
```

Division by zero is invalid and can cause undefined behaviour.

### Corrected Code

```c
#include <stdio.h>

int main() {

    int a = 10;
    int b = 0;

    if (b != 0)
        printf("%d", a / b);
    else
        printf("Cannot divide by zero");

    return 0;
}
```

### Output

```text
Cannot divide by zero
```

### Result

The AI correctly identified the division-by-zero problem and added a condition to prevent the invalid operation.

---

# 5. Code Optimization

### Original Code

```python
numbers = [2, 4, 6, 8, 10]

total = 0

for i in range(len(numbers)):
    total = total + numbers[i]

print("Sum:", total)
```

### Prompt

```text
Optimize the following Python code for better readability while
maintaining the same output.
```

### AI-Optimized Code

```python
numbers = [2, 4, 6, 8, 10]

total = sum(numbers)

print("Sum:", total)
```

### Output

```text
Sum: 30
```

### Analysis

The optimized version uses Python's built-in `sum()` function instead of manually iterating through the list.

The code becomes:

* Shorter
* Easier to understand
* More readable

### Complexity

* Time Complexity: `O(n)`
* Space Complexity: `O(1)` auxiliary space

---

# 6. Unit Test Generation

### Prompt

```text
Generate test cases for the Python function calculate_average().
Include normal values, an empty list, negative numbers,
a single value, and decimal values.
```

### Function

```python
def calculate_average(numbers):
    if not numbers:
        return None

    return sum(numbers) / len(numbers)
```

### AI-Generated Test Cases

```python
assert calculate_average([10, 20, 30]) == 20
assert calculate_average([5]) == 5
assert calculate_average([]) is None
assert calculate_average([-10, -20, -30]) == -20
assert calculate_average([1.5, 2.5, 3.5]) == 2.5

print("All test cases passed")
```

### Test Case Table

| Test Case       | Input           | Expected Output |
| --------------- | --------------- | --------------- |
| Normal values   | `[10,20,30]`    | `20`            |
| Single value    | `[5]`           | `5`             |
| Empty list      | `[]`            | `None`          |
| Negative values | `[-10,-20,-30]` | `-20`           |
| Decimal values  | `[1.5,2.5,3.5]` | `2.5`           |

### Output

```text
All test cases passed
```



# 7. Manual Coding vs AI-Assisted Coding

| Criteria            | Manual Coding           | AI-Assisted Coding          |
| ------------------- | ----------------------- | --------------------------- |
| Development Time    | Higher                  | Lower                       |
| Code Generation     | Manual                  | AI-supported                |
| Bug Detection       | Manual effort           | Faster assistance           |
| Optimization        | Programmer dependent    | AI suggestions              |
| Complexity Analysis | Requires knowledge      | Quickly explained           |
| Unit Testing        | Manually created        | Can be generated            |
| Readability         | Depends on programmer   | Usually good                |
| Learning            | Strong through practice | Faster through explanations |
| Accuracy            | Depends on programmer   | Must be verified            |
| Productivity        | Moderate                | Higher                      |

---

# Result

The experiment successfully demonstrated how AI tools can assist in programming and debugging activities.

Python, C, and Java programs were generated using suitable prompts. AI was also used to identify programming errors, correct faulty code, optimize existing programs, explain computational complexity, and generate unit tests.

The comparison showed that AI-assisted programming can reduce development time and provide useful support during debugging and testing. However, the generated code must always be compiled, tested, and reviewed by the programmer before use.

# Conclusion

AI-assisted programming provides valuable support throughout the software development process. It can help programmers generate code, locate bugs, improve existing solutions, understand complexity, and create test cases.

Therefore, AI should be considered a **programming assistant rather than a complete replacement for the programmer**. Human verification is necessary to ensure correctness, security, efficiency, and reliability.



