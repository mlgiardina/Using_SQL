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
      </ol>
    <li>The cheapest book is "Ergonomic Granite Chair" (1496). When I typed in "SELECT title, price, category FROM items WHERE category = 'books' ORDER BY price;," it returned nothing, but when I changed it to "...WHERE category LIKE 'book%'...," I got more responses.</li>
    <li>Corrine Little lives at 6439 Zetta Hills, Willmouth, WY 15029. She also lives at 54369 Wolff Forges, Lake Bryon, CA 31587. I found this by first typing "SELECT user_id FROM addresses WHERE street LIKE '6439 zetta hills';" This returned the user_is of 40, so I then searched "SELECT first_name,last_name FROM users WHERE id = 40;" and that gave me her name. </li>


