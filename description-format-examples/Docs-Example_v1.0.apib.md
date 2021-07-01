FORMAT: 1A
HOST: https://www.example.com

# Bookstore Shopping API Example
The Bookstore Example REST-based API supports the shopping experience of an online bookstore. The API includes the following capabilities and operations...

# Group Books

## Books [/books{?q,offset,limit}]

### ListBooks [GET]
Provides a paginated list of books based on the search criteria provided...
+ Parameters
    + q (string, optional)
        A query string to use for filtering books by title and description. If not provided, all available books will be listed...
    + offset (number, optional) -
        A offset from which the list of books are retrieved, where an offset of 0 means the first page of results...
        + Default: 0
    + limit (number, optional) -
        Number of records to be included in API call, defaulting to 25 records at a time if not provided...
        + Default: 25

+ Response 200 (application/json)
        Success
    + Attributes (ListBooksResponse)
+ Response 401 
        Request failed. Received when a request is made with invalid API credentials...
+ Response 403 
        Request failed. Received when a request is made with valid API credentials towards an API operation or resource you do not have access to.

# Data Structures

## ListBooksResponse (object)
A list of book summaries as a result of a list or filter request...

### Properties
+ `books` (array[BookSummary], optional) 

## BookSummary (object)
Summarizes a book that is stocked by the book store...

### Properties
+ `bookId` (string, optional) - An internal identifier, separate from the ISBN, that identifies the book within the inventory
+ `isbn` (string, optional) - The ISBN of the book
+ `title` (string, optional) - The book title, e.g. A Practical Approach to API Design
+ `authors` (array[BookAuthor], optional) 

## BookAuthor (object)
Represents a single author for a book. Since a book may have more than one author, ...

### Properties
+ `authorId` (string, optional) - An internal identifier that references the author
+ `fullName` (string, optional) - The full name of the author, e.g. D. Keith Casey

