#include <stdio.h>
#include <string.h>

int main() {
    // Variables to store item details and total bill
    char itemName[20];
    float itemPrice;
    int itemQuantity;
    float totalBill = 0.0;
    char choice;

    printf("***************** Welcome to the Grocery Shop *****************\n");

    // Loop to continuously add items until the user decides to stop
    do {
        // Prompt for item details
        printf("\nEnter item name: ");
        // Use scanf to read a single word name. For names with spaces, use gets() after clearing input buffer.
        scanf("%s", itemName); 

        printf("Enter price of %s: ", itemName);
        scanf("%f", &itemPrice);

        printf("Enter quantity of %s: ", itemName);
        scanf("%d", &itemQuantity);

        // Calculate and add to the total bill
        totalBill += (itemPrice * itemQuantity);

        // Ask the user if they want to add another item
        printf("\nDo you want to add another item? (y/n): ");
        // Clear the input buffer to prevent issues with the next scanf/gets call
        fflush(stdin); 
        scanf(" %c", &choice); // Note the space before %c to consume any leading whitespace/newline characters

    } while (choice == 'y' || choice == 'Y'); // Continue the loop if choice is 'y' or 'Y'

    // Print the final total bill
    printf("\n************************ Bill Details *************************\n");
    printf("Total bill amount: $%.2f\n", totalBill);
    printf("****************** Thank you for visiting! ******************\n");

    return 0;
}
# c-program
