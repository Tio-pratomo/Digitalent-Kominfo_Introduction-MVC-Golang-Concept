# Digitalent Kominfo - Pengenalan Konsep MVC Golang

## Development Tutorial

### 1. Install Gin Package
To see the complete documentation of Gin, you can visit the Gin official [repository][gin-repository].
```
go get github.com/gin-gonic/gin
```
### 2. Install Firebase Admin SDK 
```
go get firebase.google.com/go
```

[gin-repository]: <https://github.com/gin-gonic/gin>

###2. Initialize Gin Router
Create the first route path using Gin using this code below.
```
package main

import (
	"github.com/gin-gonic/gin"
	"net/http"
)

func main(){
	router := gin.Default()
	router.GET("/", getSomething)
	router.Run(":8080")
}

func getSomething(c *gin.Context){

	c.JSON(http.StatusOK,map[string]interface{}{
		"body1":"Get Something Success",
	})

	return
}
```
To build this, run this command below
```
go build 
```