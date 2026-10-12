Assignment 1
1. Armstrong Number (Digit Manipulation + Math): Write a program to check if a number is an Armstrong number (e.g., 153 = 1³ + 5³ + 3³).
#include <stdio.h>
#include <math.h>

int main() {
    int n, original, remainder, digits = 0;
    int sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    original = n;

    int temp = n;
    while (temp != 0) {
        digits++;
        temp /= 10;
    }

    temp = n;

    while (temp != 0) {
        remainder = temp % 10;
        sum += pow(remainder, digits);
        temp /= 10;
    }

    if (sum == original)
        printf("%d is an Armstrong number.\n", original);
    else
        printf("%d is not an Armstrong number.\n", original);

    return 0;
}
2. Perfect Number (Factors): Write a program to check if a number is a Perfect Number (a positive integer that is equal to the sum of its proper divisors, e.g., 6 = 1 + 2 + 3).
#include <stdio.h>

int main() {
    int n, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &n);

    for (int i = 1; i <= n / 2; i++) {
        if (n % i == 0) {
            sum += i;
        }
    }

    if (sum == n)
        printf("%d is a Perfect Number.\n", n);
    else
        printf("%d is not a Perfect Number.\n", n);

    return 0;
}
3. The FizzBuzz Logic Puzzle (Interview Classic): Print numbers from 1 to 100. If divisible by 3, print "Fizz". If divisible by 5, print "Buzz". If divisible by both, print "FizzBuzz".
#include <stdio.h>

int main() {

    for (int i = 1; i <= 100; i++) {

        if (i % 3 == 0 && i % 5 == 0)
            printf("FizzBuzz\n");

        else if (i % 3 == 0)
            printf("Fizz\n");

        else if (i % 5 == 0)
            printf("Buzz\n");

        else
            printf("%d\n", i);
    }

    return 0;
}

