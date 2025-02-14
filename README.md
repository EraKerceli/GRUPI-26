Flower Shop Program
This C++ program simulates a flower shop where customers can browse flower types, create their own bouquet, choose from special offers, and calculate the final price based on their choices. The program also includes special Valentine's offers, discounts for new customers, and free delivery for orders over 20 EUR.

Features
Flower Types: Displays a list of available flowers with their prices.
Bouquet Creation: Allows users to choose flowers and create their own bouquet, with the option of a 10% discount for new customers.
Special Offers:
Valentine's Day Offer: Buy a bouquet and receive a free card and bracelet.
2+2 Offer: Buy one rose and one tulip, and get two additional flowers for free.
Free Delivery: Free delivery on orders over 20 EUR.
User Interaction: The program prompts users for input, guiding them through the selection process and ensuring a smooth experience.
How It Works
Welcome Message: When the program starts, users are greeted and shown the available flower types along with their prices.
Create Bouquet: Users can choose flowers to add to their bouquet. They can specify how many flowers of each type they want.
Discount for New Customers: If the user is a first-time customer, they receive a 10% discount on their bouquet.
Special Offers:
If the user selects the Valentine's offer, they can choose from two pre-made bouquets.
If they opt for the 2+2 offer, they buy a rose and tulip and can select two more flowers for free.
Price Calculation: The program calculates the total price based on the user’s selections and applies any relevant discounts.
Free Delivery: If the total price exceeds 20 EUR, free delivery is included.
Code Breakdown
miresevini(): Greets the user and welcomes them to the store.
paraqitLule(): Displays the list of flower types and their prices.
formoBuqete(): Allows the user to create a custom bouquet.
ofertaShenValentin(): Displays the special Valentine's Day offer.
zgjedhLuleFalas(): Allows the user to select free flowers as part of the 2+2 offer.
oferta2plus2(): Handles the 2+2 offer, allowing the user to pick free flowers when purchasing certain items.
main(): The main function that controls the flow of the program, guiding the user through all the options.
Compilation
To compile and run the program, use a C++ compiler. If you're using g++, you can run the following commands in your terminal:

bash
Copy
g++ -o flower_shop flower_shop.cpp
./flower_shop
Sample Output
sql
Copy
Miresevini ne dyqanin tone te luleve!

Llojet e luleve dhe cmimet per cope:
1. Trendafil - 3 EUR
2. Tulipan - 2 EUR
3. Orkide - 5 EUR
4. Zambak - 4 EUR

A jeni klient per here te pare? (po/jo): po
Si klient per here te pare, mund te formoni nje buqete dhe fitoni 10% zbritje!
Zgjidhni lule per te formuar buqeten tuaj. Kur te perfundoni, shtypni 0.
...

Cmimi total: 15 EUR
Transporti nuk eshte falas per blerje nen 20 EUR.
Faleminderit qe zgjodhet dyqanin tone te luleve!
License
This project is open-source and available under the MIT License.



