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

- 🔭 I’m currently working on CAD Cloud Service.
- 🌱 I’m currently learning Go gRPC service (functional tests & automatic deployment).
- 👯 I’m looking to collaborate on Telegram.
- 📫 How to reach me: Telegram - @snowwy_d.

## Stack:
<p>
 <img alt="Golang" src="https://img.shields.io/badge/Go-Basics-%233388FF" />
 <img alt="Gin" src="https://img.shields.io/badge/Gin-REST_Api-%230055EE" />
 <img alt="gRPC" src="https://img.shields.io/badge/Go-gRPC-%23AA88FF" />

</p>
<p>
  <img alt="Postgres" src="https://img.shields.io/badge/PostgreSQL-Basics-%230033CC" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-%2BDB-%230011AA" />
</p>
<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-Basics-yellow" />
  <img alt="Spring" src="https://img.shields.io/badge/Java-Spring-orange" />
</p>
