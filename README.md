# go-orders-api-gorm
Simple REST service in Go with MySQL and GORM

***
### Setup and usage
```
cd to the project directory
```

```
go run orders.go
```

or

```go
go build go-orders-api-gorm
./go-orders-api-gorm
```

Create Order
```shell
curl -H 'Content-Type: application/json' -d '{"orderedAt":"2019-11-09T21:21:46+00:00","customerName":"Tom Jerry","items":[{"itemCode":"123","description":"IPhone 10X","quantity":1}]}' -X POST http://localhost:8080/orders
```

Get Orders
```shell
curl http://localhost:8080/orders
```

Update Order
```shell
curl -H 'Content-Type: application/json' -d '{"orderId":1,"customerName":"Spike Tyke","orderedAt":"2019-11-09T21:21:46Z","items":[{"lineItemId":1,"itemCode":"123","description":"IPhone 10X","quantity":10}]}' -X PUT http://localhost:8080/orders/1
```

Delete Order
```shell
curl -X DELETE http://localhost:8080/orders/1
```

***
### Tutorial

You can find the tutorial for this application at the [SoberKoder](https://www.soberkoder.com/) blog.

https://www.soberkoder.com/go-rest-api-mysql-gorm/
