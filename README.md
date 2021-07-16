# Video: https://www.youtube.com/watch?v=bQPk4S_W-pc
# Link: http://localhost:3000/graphql
---------------------
CreateBook mutation:
mutation createBook($input: CreateBookInput!){
  createBook(input: $input){
    id
    isbn
    title
  }
}
Query variables:
{
  "input": {
    "title": "My new book",
    "id": "4220",
    "isbn": "4220",
    "author": 1
  }
}
---------------------
Book query:
query book($input: FindBookInput!) {
  book(input: $input) {
    id
    title
    isbn
    author {
      id
      name
    }
  }
}
Query variables:
{
  "input": {
    "id": 1
  }
}

