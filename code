#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_ITEMS 10
#define MAX_NAME_LENGTH 50
#define NUM_DEFAULT_ITEMS 10

char defaultItems[NUM_DEFAULT_ITEMS][MAX_NAME_LENGTH] = {
    "Milk","Juice","Eggs","Cheese","Toothpaste","Brush","Mobile",
    "Laptop","Coconut oil","Deodorant"};

float defaultPrices[NUM_DEFAULT_ITEMS] = {
   49.0,40.0,23.0,25.0,20.0,10.0,20000.0,40000.0,43.0,78.0
};

//Where user's items are stored
char cart[MAX_ITEMS][MAX_NAME_LENGTH];
float cartPrices[MAX_ITEMS];
int numItems = 0;

// Accept details
void printUserDetails(char name[], char address[]) {
    printf("User Details:\n");
    printf("Name: %s\n", name);
    printf("Address: %s\n", address);
}

void displayDefaultItems() {
// Sort default items by price
    for (int i = 0; i < NUM_DEFAULT_ITEMS - 1; i++) {
        for (int j =i+1; j < NUM_DEFAULT_ITEMS - 1; j++) {
            if (defaultPrices[j] > defaultPrices[j + 1]) {
// Swap item names according to respective price
                char tempName[MAX_NAME_LENGTH];
                strcpy(tempName, defaultItems[j]);
                strcpy(defaultItems[j], defaultItems[j + 1]);
                strcpy(defaultItems[j + 1], tempName);

// Swap item's prices
                float tempPrice = defaultPrices[j];
                defaultPrices[j] = defaultPrices[j + 1];
                defaultPrices[j + 1] = tempPrice;
            }
        }
    }

    printf("Available items (sorted by price):\n");
    for (int i = 0; i < NUM_DEFAULT_ITEMS; i++) {
        printf("%d. %s - Rs %.2f\n", i + 1, defaultItems[i], defaultPrices[i]);
    }
}
//search items
int searchItem(char itemName[]) {
    for (int i = 0; i < NUM_DEFAULT_ITEMS; i++) {
        if (strcmp(defaultItems[i], itemName) == 0) {
            return i;
        }
    }
    return -1;
}
//Display cart
void displayCart() {
    if (numItems == 0) {
        printf("Cart is empty\n");
        return;
    }

    printf("Items in cart:\n");
    for (int i = 0; i < numItems; i++) {
        printf("%d. %s - Rs %.2f\n", i + 1, cart[i], cartPrices[i]);
    }
}
//editing cart
void removeFromCart(int index) {
    if (index < 0 || index >= numItems) {
        printf("Invalid index\n");
        return;
    }

    for (int i = index; i < numItems - 1; i++) {
        strcpy(cart[i], cart[i + 1]);
        cartPrices[i] = cartPrices[i + 1];
    }

    numItems--;
}
//Calculating bill
float calculateTotal() {
    float total = 0.0;
    for (int i = 0; i < numItems; i++) {
        total += cartPrices[i];
    }
    return total;
}

int main() {
    char name[MAX_NAME_LENGTH], address[MAX_NAME_LENGTH];

    printf("Enter your name: ");
    scanf("%s", name);

    printf("Enter your address: ");
    scanf("%s", address);

    printUserDetails(name,address);

    int choice;
    do {
        printf("\n1. Search for item\n");
        printf("2. Display available items\n");
        printf("3. Display cart\n");
        printf("4. Sort items by price and display\n");
        printf("5. Remove item from cart\n");
        printf("6. Calculate total amount\n");
        printf("7. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        if(choice==1)
             {
                char itemName[MAX_NAME_LENGTH];
                printf("Enter item name to search: ");
                scanf("%s", itemName);
                int index = searchItem(itemName);
                if (index != -1) {
                    strcpy(cart[numItems], defaultItems[index]);
                    cartPrices[numItems] = defaultPrices[index];
                    numItems++;
                    printf("Item added to cart\n");
                } else {
                    printf("Item not available\n");}}
        if(choice==2){
                displayDefaultItems();}
        if (choice==3){
                displayCart();}
        if (choice==4){
                displayDefaultItems();}
        if (choice==5){
                int index;
                printf("Enter index of item to remove: ");
                scanf("%d", &index);
                removeFromCart(index - 1);
                printf("Item removed from cart\n");}
        if (choice==6){
                printf("Total amount: Rs %.2f\n", calculateTotal());}
        if (choice==7){
                printf("Exiting...\n");
                exit(0);}
       }
        while (1);
        return 0;
}
