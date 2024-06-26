#  Abstract:

The project is a command-line shopping application implemented in the C programming language. It serves as a basic platform for users to perform various shopping-related tasks, offering functionalities such as searching for items, managing a cart, and calculating the total bill. 

The application begins by prompting users to input their name and address, after which they are presented with a menu-driven interface. Users can search for items by name, add them to their cart, and remove items if needed. Additionally, they can view the available items sorted by price for easier browsing. The cart is maintained using arrays to store item names and their corresponding prices.

One notable feature is the sorting of available items by price, providing users with a sorted list for more convenient selection. This sorting algorithm enhances user experience by presenting items in a logical order based on price.

Furthermore, the application ensures robustness by handling invalid inputs and errors gracefully, thereby improving user interaction and overall usability.

Overall, this project serves as a foundational example of a shopping application, demonstrating core concepts such as input handling, array manipulation, and menu-driven interfaces in the C programming language.

FEATURES AVAILABLE :
1) Items Available :
This code snippet initializes two arrays, `defaultItems` and `defaultPrices`, representing a list of default items available for purchase and their corresponding prices. The `defaultItems` array stores the names of various items such as "Milk," "Juice," "Eggs," etc., while the `defaultPrices` array holds their respective prices. This code provides a foundation for managing an inventory system or a shopping application by defining the available items and their prices for further processing or display to users.

2) Where user's items are stored :
   This code snippet declares three variables: `cart`, `cartPrices`, and `numItems`.
   1. `cart` is a two-dimensional array to store the names of items added to a shopping cart.
   2. `cartPrices` is an array to store the prices corresponding to the items in the cart.
   3. `numItems` is an integer variable to keep track of the number of items currently in the cart. 
Together, these variables serve as the foundation for managing a shopping cart in a program or application.

3) Accepting details:
   This function, `printUserDetails`, prints user details to the console. It takes two parameters: `name`, a character array representing the user's name, and `address`, a character array representing the user's address. The function first prints a header indicating "User Details:", followed by the user's name and address.

4) Sort the items :
   This nested loop iterates through the `defaultPrices` array to perform a bubble sort algorithm. It compares adjacent elements and swaps them if they are in the wrong order, ensuring that the array is sorted in ascending order of prices. This sorting process helps arrange the items in the list based on their prices, facilitating tasks such as displaying items in order of increasing price or finding the cheapest item.

5) Swap item names according to respective price:
This code snippet facilitates swapping the names of items in an array based on their respective prices. It employs a temporary variable, `tempName`, to store the name of one item temporarily. The names are swapped by copying them between array elements using `strcpy()`. This process ensures that the item names are rearranged according to their corresponding prices.

6) Swap item's prices:
This code snippet implements a sorting algorithm to arrange items based on their prices. It utilizes a temporary variable, `tempPrice`, to temporarily store the price of one item during swapping. The prices are swapped between array elements to ensure the items are arranged in ascending order of price. Finally, the sorted list of items along with their prices is printed to the console, providing users with an overview of available items sorted by price.

7) Search the items :
   This function, `searchItem`, iterates through the `defaultItems` array to find a match for the given `itemName`. If a match is found, it returns the index of the item in the array. If no match is found, it returns -1. This function essentially searches for an item in the list of default items and returns its index if found, otherwise indicating that the item is not present in the list.

8) Display cart:
This function, `displayCart()`, is designed to present the contents of a shopping cart to the user. It begins by checking if the cart is empty, in which case it prints a message indicating so and exits the function. If the cart contains items, it iterates through each item in the cart, displaying its index, name, and price formatted to two decimal places. This abstraction outlines the function's purpose and behavior, offering a concise understanding of its functionality.

9) Editing the cart:
   This function, `removeFromCart`, removes an item from the shopping cart based on the provided index. It first checks if the index is valid, ensuring it falls within the range of items currently in the cart. If the index is valid, it shifts the elements in the `cart` array and `cartPrices` array to the left to fill the gap left by the removed item. Finally, it decrements the `numItems` variable to reflect the removal of the item from the cart.
10) Calculating bill:
   This code consists of two main functions: `calculateTotal()` and `main()`. 

 1. `calculateTotal()` computes the total cost of items in the shopping cart by iterating through the array of item prices and summing them up. It initializes a variable `total` to store the sum of prices, iterates through the items in the cart, and adds each item's price to the total. Finally, it returns the total cost.

 2. In `main()`, the user is prompted to enter their name and address. After receiving the input, it calls the `printUserDetails()` function to print the user's details. This function takes the entered name and address as parameters and prints them to the console.

This abstract provides an overview of the main functionality of the code, focusing on user interaction and calculation of the total cost of items in the shopping cart.

11) Menu :
    This code presents a menu to the user, allowing them to interact with a program. The user is prompted to enter a choice, and based on their selection, different actions are performed. Here's a breakdown of the menu options:

1. **Search for item**: Prompts the user to enter an item name to search for in the available items list. If the item is found, it adds it to the shopping cart.
2. **Display available items**: Shows the list of available items with their respective prices.
3. **Display cart**: Displays the items currently in the shopping cart along with their prices.
4. **Sort items by price and display**: Sorts the available items by price and displays them.
5. **Remove item from cart**: Allows the user to remove an item from the shopping cart.
6. **Calculate total amount**: Calculates and displays the total amount of items in the shopping cart.
7. **Exit**: Exits the program.

The menu continues to loop until the user chooses to exit by entering '7'.
