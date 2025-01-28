### Hi, I'm Evteev Daniel! 👋

```go
package main

import (
	"errors"
	"fmt"
)

type Person struct {
	Name    string
	Surname string
}

func sayHello(p Person) error {
	if p.Name == "" || p.Surname == "" {
		return errors.New("Name or Surname cannot be empty")
	}
	fmt.Printf("Hi, I'm %s %s, nice to meet your eyes on this text yo!\n", p.Surname, p.Name)
	return nil
}

func main() {
	me := Person{
		Name:    "Daniel",
		Surname: "Evteev",
	}
	err := sayHello(me)
	if err != nil {
		fmt.Println(err)
	}
}
```

- 🔭 I’m currently working on CAD Cloud Service.
- 🌱 I’m currently learning Go REST API & gRPC.
- 👯 I’m looking to collaborate on Telegram.
- 📫 How to reach me: Telegram - @snowwy_d.

### Stack:
<p>
 <img alt="Golang" src="https://img.shields.io/badge/Go-Basics-%233388FF" />
 <img alt="Gin" src="https://img.shields.io/badge/Gin-Api-%230055EE" />
</p>
<p>
  <img alt="Postgres" src="https://img.shields.io/badge/PostgreSQL-Basics-%230033CC" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-%2BDB-%230011AA" />
</p>
<p>
  <img alt="Python" src="https://img.shields.io/badge/Python-Basics-yellow" />
  <img alt="Spring" src="https://img.shields.io/badge/Java-Spring-orange" />
</p>
