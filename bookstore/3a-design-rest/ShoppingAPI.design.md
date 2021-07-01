| Resource Path                      | Operation Name       | HTTP Method | Description                               | Request Details          | Response Details | Response Code(s) |
|------------------------------------|----------------------|-------------|-------------------------------------------|--------------------------|------------------|------------------|
| /books                             | listBooks()          | GET         | List books by category or release date    | categoryId   releaseDate | Books[]          | 200              |
| /books/search                      | searchBooks()        | POST        | Search for books by author, title         | searchQuery              | Books[]          | 200              |
| /carts/{cartId}                    | viewCart()           | GET         | View the current cart and total           | cartId                   | Cart             | 200, 404         |
| /carts/{cartId}                    | clearCart()          | DELETE      | Remove all books from the customer's cart | cartId                   | Cart             | 204, 404         |
| /carts/{cartId}/items              | addItemToCart()      | POST        | Add a book to the customer's cart         | cartId                   | Cart             | 201, 400         |
| /carts/{cartId}/items/{cartItemId} | removeItemFromCart() | DELETE      | Remove a book from the customer's cart    | cartId   cartItemId      | Cart             | 204, 404         |
| /authors                           | getAuthorDetails()   | GET         | Retrieve the details of an author         | authorId                 | BookAuthor       | 200, 404         |
