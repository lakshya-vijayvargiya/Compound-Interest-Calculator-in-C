# Compound-Interest-Calculator-in-C
This program calculates compound interest based on user input for principal, rate, and time. It uses the formula  𝐶 𝐼 = 𝑃 × ( ( 1 + 𝑅 / 100 ) 𝑇 − 1 )  with the pow() function from &lt;math.h>. The result is displayed neatly with two decimal precision for clarity.


#include <stdio.h>
#include <math.h>   // Needed for pow() function

int main() {
    float principal, rate, time, compound_interest;  // Variables for input and result

    // Take principal amount from user
    printf("Enter principal amount: ");
    scanf("%f", &principal);

    // Take rate of interest from user
    printf("Enter rate of interest: ");
    scanf("%f", &rate);

    // Take time period from user
    printf("Enter time period: ");
    scanf("%f", &time);

    // Calculate compound interest using formula: P * ( (1 + R/100)^T - 1 )
    compound_interest = principal * (pow(1 + rate / 100, time) - 1);

    // Display the result with two decimal places
    printf("Compound Interest = %.2f\n", compound_interest);

    return 0;  // End of program
}
