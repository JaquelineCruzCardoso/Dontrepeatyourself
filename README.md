# Dontrepeatyourself
First and second code
~~~c
#include <stdio.h>


/* Function declaration */
int sumOfNaturalNumbers(int start, int end);


int main()
{
    int start, end, sum;
    
    /* Input lower and upper limit from user */
    printf("Enter lower limit: ");
    scanf("%d", &start);
    printf("Enter upper limit: ");
    scanf("%d", &end);
    
    sum = sumOfNaturalNumbers(start, end);
    
    printf("Sum of natural numbers from %d to %d = %d", start, end, sum);
    
    return 0;
}


/**
 * Recursively find the sum of natural number
 */
int sumOfNaturalNumbers(int start, int end)
{
    if(start == end)
        return start;
    else
        return start + sumOfNaturalNumbers(start + 1, end); 
}


#include <stdio.h>


/* Function declaration */
void printEvenOdd(int cur, int limit);



int main()
{
    int lowerLimit, upperLimit;
    
    // Input lower and upper limit from user
    printf("Enter lower limit: ");
    scanf("%d", &lowerLimit);
    printf("Enter upper limit: ");
    scanf("%d", &upperLimit);
    
    printf("Even/odd Numbers from %d to %d are: ", lowerLimit, upperLimit);
    printEvenOdd(lowerLimit, upperLimit); 
    
    return 0;
}


/**
 * Recursive function to print even or odd numbers in a given range. 
 */
void printEvenOdd(int cur, int limit)
{
    if(cur > limit)
        return;
    
    printf("%d, ", cur);
    
    // Recursively call to printEvenOdd to get next value
    printEvenOdd(cur + 2, limit);
}
