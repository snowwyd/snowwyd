# 👋 Hi, I'm Evteev Daniel!

```go
package main

import (
	"fmt"
	"net/http"

	"github.com/gin-gonic/gin"
)

type PersonRequest struct {
	Name    string `json:"name" binding:"required"`
	Surname string `json:"surname" binding:"required"`
}

type Handler struct {
	UsecaseMock struct{ RepositoryMock struct{} }
}

func (h Handler) Greet(c *gin.Context) {
	var req PersonRequest

	c.ShouldBindJSON(&req)
	if req.Name == "" || req.Surname == "" {
		c.JSON(http.StatusBadRequest, gin.H{"message": "name and surname are required"})
		return
	}

	greetingText := fmt.Sprintf("Hi, %s %s, I'm Evteev Daniel a.k.a snowwy, nice to meet your eyes on this text yo!", req.Name, req.Surname)
	c.JSON(http.StatusOK, gin.H{"greeting_text": greetingText})
}

func main() {
	var handler Handler

	router := gin.Default()
	router.POST("/greet", handler.Greet)
	
	if err := router.Run("localhost:809"); err != nil {
		panic(err)
	}
}
```

🚀 **I'm currently working on**  
- Huge mastery project
- Security Signature Utility

🧐 **Learning now**  
- Golang deep dive

📫 **Contact me**  
- Telegram: [@qyteboii](https://t.me/qyteboii)

---

<div align="center">
	<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExeXp4MnJsZTY1cTB2NHdyaHRnd3hrZW1rbGJpeGZzYmNtcWZlaGtneSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Q5tuyfHOQd18Hq49Vp/giphy.gif" width="400" height="300"/>
   	<img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHhnZmMyYXRoaGdnanMwN2VoYnl0NWFydHl4Mmg2eHJxcGY5bmd0YyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/BIis2ma7Or2wjQMoQL/giphy.gif" width="400" height="300"/>
</div>
