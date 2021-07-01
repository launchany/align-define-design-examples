# Modeled Resources

## Book

| Property Name | Description                   |
|---------------|-------------------------------|
| title         | The book title                |
| isbn          | The unique ISBN of the book   |
| authors       | List of Book Author resources |

## Book Author

| Property Name | Description                 |
|---------------|-----------------------------|
| fullName      | The full name of the author |

## Cart

| Property Name | Description                                  |
|---------------|----------------------------------------------|
| cartItems     | The items currently in the cart for purchase |
| subtotal      | The total cost of all books in the cart      |
| salesTax      | The sales tax to be applied                  |
| vatTax        | Any VAT tax to be applied                    |
| cartTotal     | The total cost of the cart                   |


## Cart Item

| Property Name | Description                                                                       |
|---------------|-----------------------------------------------------------------------------------|
| book          | The books currently in the cart for purchase                                      |
| qty           | The quantity of the item in the cart (default 1)                                  |
| unitPrice     | The unit price represented as a whole number. For example, $1.99 USD would be 199 |
|               |                                                                                   |

