<h1>Normal Mode</h1>
<p>
  <ol>
    <p>There are fifty users. I used "SELECT COUNT(*) FROM users;" to get this info.</p>
    <p>I found the most expensive items by typing "SELECT title, price FROM items ORDER BY price;" The 5 most expensive items are:
      <ol>
        <p>Small Cotton Gloves (9984)</p>
        <p>Small Wooden Computer (9859)</p>
        <p>Awesome Granite Pants (9790)</p>
        <p>Sleek Wooden Hat (9390)</p>
        <p>Ergonomic Steel Car (9341)</p>
      </ol></p>
    <p>The cheapest book is "Ergonomic Granite Chair" (1496). When I typed in
    ```
    SELECT title, price, category FROM items WHERE category = 'books' ORDER BY price;
    ```
     it returned nothing, but I got more responses when I changed it to
    ```
     ...WHERE category LIKE 'book%'...
    ```
      </p>
    <p>Corrine Little lives at 6439 Zetta Hills, Willmouth, WY 15029. She also lives at 54369 Wolff Forges, Lake Bryon, CA 31587. I found this by first typing "SELECT user_id FROM addresses WHERE street LIKE '6439 zetta hills';" This returned the user_id of 40, so I then searched "SELECT first_name,last_name FROM users WHERE id = 40;" and that gave me her name. </p>
    <p>To change Virginie Mitchell's address, I first typed "SELECT user_id FROM users WHERE last_name LIKE 'Mitchell' AND first_name LIKE 'Viriginie'". This returned the user_id of 39, so then I typed "SELECT city, state, zip FROM addresses WHERE user_id = 39;" After that, I noticed that she had two addresses, so to only update her NY address, I typed "UPDATE addresses SET city = 'NY', zip = 10108 WHERE user_id = 39 AND state LIKE 'NY';"</p>
    <p>To buy one of each tool, it would cost 46477. I found this info by typing "SELECT sum(price) FROM items WHERE category LIKE '%tool%';"</p>
    <p>We sold 2125 total items. I found this info by typing "SELECT sum(quantity) FROM orders;"</p>
    <p>The total amount spent on books was 503,761. I found this info by typing "SELECT sum(price * quantity) FROM orders JOIN items ON items.id = orders.item_id AND category LIKE 'book%';"</p>
    <p>I created an entry for myself in the "users" table by typing "INSERT INTO users (id, first_name, last_name, email) VALUES (51, 'Matthew', 'Giardina', 'mlgiardina@me.com');" Then I created an order for myself by typing "INSERT INTO orders (id, user_id, item_id, quantity, created_at) VALUES (378, 51, 1, 10, datetime('now'));"</p>
  </ol>
</p>


