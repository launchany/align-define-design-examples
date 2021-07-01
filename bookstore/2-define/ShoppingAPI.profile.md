# Shopping API

* Supports the book browsing experience and cart management
* Scope: Public

| Operation Name       | Description                               | Participants          | Resource(s)       | Emitted Events   | Operation Details                                                          | Traits                     |
|----------------------|-------------------------------------------|-----------------------|-------------------|------------------|----------------------------------------------------------------------------|----------------------------|
| listBooks()          | List books by category or release date    | Customer, Call Center | Book, Book Author | Books.Listed     | __Request Parameters:__ categoryId, releaseDate     __Returns:__   Books[] | safe   / synchronous       |
| searchBooks()        | Search   for books by author, title       | Customer, Call Center | Book              | Books.Searched   | __Request Parameters:__ searchQuery     __Returns:__   Books[]             | safe   / synchronous       |
| addItemToCart()      | Add a book to the customer's cart         | Customer, Call Center | Cart Item, Cart   | Cart.ItemAdded   | __Request Parameters:__ cartId, bookId,   quantity     __Returns:__   Cart | unsafe   / synchronous     |
| removeItemFromCart() | Remove a book from the customer's cart    | Customer, Call Center | Cart Item, Cart   | Cart.ItemRemoved | __Request Parameters:__ cartItemId     __Returns:__   Cart                 | idempotent   / synchronous |
| clearCart()          | Remove all books from the customer's cart | Customer, Call Center | Cart              | Cart.Cleared     | __Request Parameters:__ cartId     __Returns:__   Cart                     | safe / synchronous         |
| viewCart()           | View   the current cart and total         | Customer, Call Center | Cart              | Cart.Viewed      | __Request Parameters:__ cartId     __Returns:__   Cart                     | safe / synchronous         |
