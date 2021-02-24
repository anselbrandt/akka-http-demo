# Akka HTTP Demo

### Scafolded with:

```
sbt new akka/akka-http-quickstart-scala.g8
```

### Run

```
sbt run
```

### Guide

[Akka HTTP Quickstart for Scala](https://developer.lightbend.com/guides/akka-http-quickstart-scala/#example-app-overview)

### Routes

```
localhost:8080

GET/users
GET/users/<id>
POST/users
DELETE/users/<id>
```

## Excercise

### cURL

```
curl -H "Content-type: application/json" -X POST -d '{"name": "MrX", "age": 31, "countryOfResidence": "Canada"}' http://localhost:8080/users

curl -H "Content-type: application/json" -X POST -d '{"name": "Anonymous", "age": 55, "countryOfResidence": "Iceland"}' http://localhost:8080/users

curl -H "Content-type: application/json" -X POST -d '{"name": "Bill", "age": 67, "countryOfResidence": "USA"}' http://localhost:8080/users
```

To retrieve all users, enter the following command:

```
curl http://localhost:8080/users
```

To retrieve a specific user, enter the following command:

```
curl http://localhost:8080/users/Bill
```

Finally, it is possible to delete users:

```
curl -X DELETE http://localhost:8080/users/Bill
```

### Browser-based clients

Using Postman or similar, `Post` the following (sending each payload separately):

```
{"name": "MrX", "age": 31, "countryOfResidence": "Canada"}

{"name": "Anonymous", "age": 55, "countryOfResidence": "Iceland"}

{"name": "Bill", "age": 67, "countryOfResidence": "USA"}
```

To retrieve all users:

```
GET

http://localhost:8080/users
```

## Continue with [Backend Actor logic](https://developer.lightbend.com/guides/akka-http-quickstart-scala/backend-actor.html)