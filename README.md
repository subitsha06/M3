# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <math.h>

void calculateEMI(double principal, double rate, int months) {
    double r = rate / (12 * 100);  // monthly interest rate
    double t = months;
    double emi;

   emi = (principal * r * pow(1 + r, t)) / (pow(1 + r, t) - 1);

   printf("The EMI is: %.2lf\n", emi);
}

int main() {
    double principal, rate;
    int months;

   printf("Enter principal amount: ");
    scanf("%lf", &principal);
    printf("Enter annual rate of interest (in %%): ");
    scanf("%lf", &rate);
    printf("Enter number of months: ");
    scanf("%d", &months);

   calculateEMI(principal, rate, months);
    return 0;
}

## OUTPUT
<img width="1668" height="758" alt="image" src="https://github.com/user-attachments/assets/d95cd3bb-0d9f-4832-a470-0a732c5a7d85" />

## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, first = 0, second = 1, next, i;

   printf("Enter number of terms: ");
    scanf("%d", &n);

   printf("Fibonacci series: ");

   for (i = 1; i <= n; i++) {
        if (i == 1) {
            printf("%d ", first);
            continue;
        }
        if (i == 2) {
            printf("%d ", second);
            continue;
        }
        next = first + second;
        printf("%d ", next);
        first = second;
        second = next;
    }

   printf("\n");

   return 0;
}


## OUTPUT


<img width="1657" height="703" alt="image" src="https://github.com/user-attachments/assets/b120c482-3ab0-40e4-87de-4553a6e1c747" />




## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, i;
    int arr[100];

   printf("Enter number of elements: ");
    scanf("%d", &n);

   printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }
    printf("The last element of the array is: %d\n", arr[n - 1]);
    return 0;
}

## OUTPUT
<img width="1673" height="483" alt="image" src="https://github.com/user-attachments/assets/f6a65709-0707-43f3-ad6e-d131c651398c" />









## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, i, count = 0;
    int arr[100];

   printf("Enter number of elements: ");
    scanf("%d", &n);

   printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
        if (arr[i] > 0)
            count++;
    }

   printf("Total number of positive elements: %d\n", count);

   return 0;
}


## OUTPUT

<img width="1664" height="565" alt="image" src="https://github.com/user-attachments/assets/32128940-e90b-49e8-8476-88be9d2c7eff" />




## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
#include <stdio.h>

int main() {
    int n, i;
    printf("Enter size of the array: ");
    scanf("%d", &n);

   int arr[n];
    char arr2[n]; // array to store updated values (int or 'E')

   printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        printf("Element %d: ", i + 1);
        scanf("%d", &arr[i]);
    }
    printf("\nUpdated array:\n");
    for (i = 0; i < n; i++) {
        if (arr[i] % 2 == 0)
            arr2[i] = 'E';
        else
            arr2[i] = arr[i]; // implicit conversion to char
        if (arr2[i] == 'E')
            printf("%c ", arr2[i]);
        else
            printf("%d ", arr2[i]);
    }
    printf("\n");
    return 0;
}

## Output:
 <img width="1673" height="769" alt="image" src="https://github.com/user-attachments/assets/48bef750-4262-4b2d-9020-14b09433f68f" />



## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



