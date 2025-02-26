## Hi, I'm Evteev Daniel! 👋

```go
package main

import (
	"errors"
	"fmt"
	"log/slog"
)

type Person struct {
	Name    string `json:"name"`
	Surname string `json:"surname"`
}

func sayHello(p Person) error {
	const op = "sayHello"
	if p.Name == "" || p.Surname == "" {
		slog.Warn("name or surname is empty", "op", op)

		return errors.New("name or surname cannot be empty")
	}

	slog.Info("printing greeting text", "op", op)

	fmt.Printf("Hi, I'm %s %s, nice to meet your eyes on this text yo!\n", p.Surname, p.Name)
	return nil
}

func main() {
	me := Person{
		Name:    "Daniel",
		Surname: "Evteev",
	}
	if err := sayHello(me); err != nil {
		fmt.Println(err)
	}
}
```

- 🔭 I’m currently working on Messenger Chat Service, strarting ConstructHub backend.
- 🌱 I’m currently learning Databases with Go(VK group course).
- 👯 I’m looking to collaborate on Telegram.
- 📫 How to reach me: Telegram - @snowwy_d.

## Stack:
<p>
 <img alt="Golang" src="https://img.shields.io/badge/Go-Intermediate-%233388FF" />
 <img alt="Gin" src="https://img.shields.io/badge/Gin-REST_Api-%230055EE" />
 <img alt="gRPC" src="https://img.shields.io/badge/Go-gRPC-%23AA88FF"/>

</p>
<p>
  <img alt="Postgres" src="https://img.shields.io/badge/PostgreSQL-Basics-%230033CC" />
  <img alt="Mongo" src="https://img.shields.io/badge/Mongo-DB-%23006600" />	
  <img alt="Docker" src="https://img.shields.io/badge/Docker-%2BDB-%230011AA"/>
</p>
<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-Basics-yellow" />
  <img alt="Spring" src="https://img.shields.io/badge/Java-Spring-orange" />
</p>

## TODO:
<p>
  <img alt="Redis" src="https://img.shields.io/badge/Redis-%23AA1111" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/K8S-%230011AA" />
  <img alt="CICD" src="https://img.shields.io/badge/Github-Actions%23111111" />
  <img alt="Camunda" src="https://img.shields.io/badge/Camunda-%23FF1155" />
</p>
