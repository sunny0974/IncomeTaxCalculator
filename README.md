# IncomeTaxCalculator
This is a calculator for calculating income tax to pay government by the users.

#include <stdio.h>

int main() {
    double income, tax = 0;

    // Input the annual income
    printf("Enter your annual income: ");
    scanf("%lf", &income);

    // Tax slabs based on income
    if (income <= 250000) {
        tax = 0;
    } 
    else if (income <= 500000) {
        tax = (income - 250000) * 0.05;
    } 
    else if (income <= 1000000) {
        tax = (income - 500000) * 0.2 + (500000 - 250000) * 0.05;
    } 
    else {
        tax = (income - 1000000) * 0.3 + (1000000 - 500000) * 0.2 + (500000 - 250000) * 0.05;
    }

    // Output the calculated tax
    printf("Income Tax Payable: ₹%.2f\n", tax);

    return 0;
}


