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

5)Swap item names according to respective price:
This code snippet facilitates swapping the names of items in an array based on their respective prices. It employs a temporary variable, `tempName`, to store the name of one item temporarily. The names are swapped by copying them between array elements using `strcpy()`. This process ensures that the item names are rearranged according to their corresponding prices.

6) Swap item's prices:
This code snippet implements a sorting algorithm to arrange items based on their prices. It utilizes a temporary variable, `tempPrice`, to temporarily store the price of one item during swapping. The prices are swapped between array elements to ensure the items are arranged in ascending order of price. Finally, the sorted list of items along with their prices is printed to the console, providing users with an overview of available items sorted by price.

