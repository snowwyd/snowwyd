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

var (
	ErrEmptyFields = errors.New("name or surname cannot be empty")
	logger         = slog.Default()
)

func Hello(person Person) (string, error) {
	const op = "sayHello"
	if person.Name == "" || person.Surname == "" {
		logger.Warn("name or surname is empty", "op", op)
		return "", ErrEmptyFields
	}
	logger.Info("greeting text generated successfully", "op", op)
	return fmt.Sprintf("Hi, I'm %s %s, nice to meet your eyes on this text yo!\n", person.Name, person.Surname), nil
}

func main() {
	me := Person{
		Name:    "Daniel",
		Surname: "Evteev",
	}
	text, err := Hello(me)
	if err != nil {
		logger.Error("failed to generate greeting text", "error", err)
		return
	}
	fmt.Println(text)
}
```

- 🔭 I’m currently working on Messenger backend, ConstructFlow backend.
- 🌱 I’m currently learning OAuth and Web application architecture (VK group course), BPMN Camunda.
- 👯 I’m looking to collaborate on Telegram.
- 📫 How to reach me: Telegram - @snowwy_d.

## Stack:
<p>
 	<img alt="Golang" src="https://img.shields.io/badge/Go-Intermediate-%2300508A" />
 	<img alt="Gin" src="https://img.shields.io/badge/Gin-REST-%2300538A" />
 	<img alt="gRPC" src="https://img.shields.io/badge/Go-gRPC-%23003357"/>
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
	<img alt="Camunda" src="https://img.shields.io/badge/Camunda-BPMN-%23FF1155" />
	<img alt="Redis" src="https://img.shields.io/badge/Redis-%23AA1111" />
	<img alt="MinIO" src="https://img.shields.io/badge/MinIO-S3-%23c20020" />
  	<img alt="Kubernetes" src="https://img.shields.io/badge/K8S-%230011AA" />
  	<img alt="CICD" src="https://img.shields.io/badge/Github-Actions-%23111111" />
  	<img alt="Kafka" src="https://img.shields.io/badge/Apache-Kafka-%23FFFFFF" />
</p>
