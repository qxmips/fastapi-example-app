curl -X 'GET' \
  'http://127.0.0.1:8000/todo' \
  -H 'accept: application/json'


curl -X 'POST' \
  'http://127.0.0.1:8000/todo' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 1,
  "item": "First Todo is to finish this book!"
}'


# invalid
curl -X 'POST' \
  'http://127.0.0.1:8000/todo' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
}'

curl -X 'GET' \
  'http://127.0.0.1:8000/todo/1' \
  -H 'accept: application/json'



# POST, PUT

curl -X 'POST' \
  'http://127.0.0.1:8000/todo' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 1,
  "item": "Example Schema!"
}'


curl -X 'PUT' \
  'http://127.0.0.1:8000/todo/1' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "item": "Read the next chapter of the book."
}'

# DELETE 
curl -X 'POST' \

  'http://127.0.0.1:8000/todo' \

  -H 'accept: application/json' \

  -H 'Content-Type: application/json' \

  -d '{

  "id": 1,

  "item": "Example Schema!"

}'

curl -X 'DELETE' \

  'http://127.0.0.1:8000/todo/1' \

  -H 'accept: application/json