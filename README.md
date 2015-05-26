<h1>Normal Mode</h1>
<p>
  <ol>
    <li>There are fifty users. I used "SELECT COUNT(*) FROM users;" to get this info.</li>
    <li>I found the most expensive items by typing "SELECT title, price FROM items ORDER BY price;" The 5 most expensive items are:
      <ol>
        <li>Small Cotton Gloves (9984)</li>
        <li>Small Wooden Computer (9859)</li>
        <li>Awesome Granite Pants (9790)</li>
        <li>Sleek Wooden Hat (9390)</li>
        <li>Ergonomic Steel Car (9341)</li>
      </ol></li>
    <li>The cheapest book is "Ergonomic Granite Chair" (1496). When I typed in "SELECT title, price, category FROM items WHERE category = 'books' ORDER BY price;," it returned nothing, but when I changed it to "...WHERE category LIKE 'book%'...," I got more responses.</li>
    <li>Corrine Little lives at 6439 Zetta Hills, Willmouth, WY 15029. She also lives at 54369 Wolff Forges, Lake Bryon, CA 31587. I found this by first typing "SELECT user_id FROM addresses WHERE street LIKE '6439 zetta hills';" This returned the user_id of 40, so I then searched "SELECT first_name,last_name FROM users WHERE id = 40;" and that gave me her name. </li>
    <li>To change Virginie Mitchell's address, I first typed "SELECT user_id FROM users WHERE last_name LIKE 'Mitchell' AND first_name LIKE 'Viriginie'". This returned the user_id of 39, so then I typed "SELECT city, state, zip FROM addresses WHERE user_id = 39;" After that, I noticed that she had two addresses, so to only update her NY address, I typed "UPDATE addresses SET city = 'NY', zip = 10108 WHERE user_id = 39 AND state LIKE 'NY';"</li>
    <li>To buy one of each tool, it would cost 46477. I found this info by typing "SELECT sum(price) FROM items WHERE category LIKE '%tool%';"</li>
    <li>We sold 2125 total items. I found this info by typing "SELECT sum(quantity) FROM orders;"</li>
    <li>The total amount spent on books was 503,761. I found this info by typing "SELECT sum(price * quantity) FROM orders JOIN items ON items.id = orders.item_id AND category LIKE 'book%';"</li>
    <li>I created an entry for myself in the "users" table by typing "INSERT INTO users (id, first_name, last_name, email) VALUES (51, 'Matthew', 'Giardina', 'mlgiardina@me.com');" Then I created an order for myself by typing "INSERT INTO orders (id, user_id, item_id, quantity, created_at) VALUES (378, 51, 1, 10, datetime('now'));"</li>
  </ol>
</p>


