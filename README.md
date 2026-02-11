# Hi, I'm Evteev Daniel!

```go
package main

import (
	"fmt"
	"net/http"

	"github.com/gin-gonic/gin"
)

type greeter interface {
	greet() string
}

func newGreeter(isForStudent bool) greeter {
	if isForStudent {
		return &mentor{firstName: "Daniel", lastName: "Evteev"}
	}
	return &gitHubUser{nickname: "qyteboii a.k.a snowwyd"}
}

type mentor struct {
	firstName, lastName string
}

func (m *mentor) greet() string {
	return fmt.Sprintf("Hi, I'm %s %s - your Golang mentor!", m.firstName, m.lastName)
}

type gitHubUser struct {
	nickname string
}

func (ghu *gitHubUser) greet() string {
	return fmt.Sprintf("Hi, I'm %s, nice to meet your eyes on this text yo!", ghu.nickname)
}

type greetRequest struct {
	IsStudent bool `json:"is_student"`
}

func greet(c *gin.Context) {
	var req greetRequest
	c.ShouldBindJSON(&req)

	greeter := newGreeter(req.IsStudent)
	c.JSON(http.StatusOK, gin.H{"greeting_text": greeter.greet()})
}

func main() {
	router := gin.Default()
	router.POST("/greet", greet)

	if err := router.Run("localhost:809"); err != nil {
		panic(err)
	}
}
```

## Activity

**I'm currently working on**  
- Huge mastery project
- Go mentorship site
- Go interviews roadmap

**Learning now**  
- Huge Go expert roadmap
- Obsidian features
- GitHub Pages syntax

**Contact me**  
- Telegram: [@qyteboii](https://t.me/qyteboii)

---

<div align="center">
	<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeXp4MnJsZTY1cTB2NHdyaHRnd3hrZW1rbGJpeGZzYmNtcWZlaGtneSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Q5tuyfHOQd18Hq49Vp/giphy.gif" width="400" height="300"/>
   	<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHhnZmMyYXRoaGdnanMwN2VoYnl0NWFydHl4Mmg2eHJxcGY5bmd0YyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/BIis2ma7Or2wjQMoQL/giphy.gif" width="400" height="300"/>
</div>
