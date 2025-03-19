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
	UsecaseMock struct{}
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
- Messenger backend
- ConstructFlow backend and CI/CD pipelines

🧐 **Learning now**  
- gRPC streaming
- GitLab CI/CD
- Apache Kafka

📫 **Contact me**  
- Telegram: [@snowwy_d](https://t.me/snowwy_d)
<div align="center">
  <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHhnZmMyYXRoaGdnanMwN2VoYnl0NWFydHl4Mmg2eHJxcGY5bmd0YyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/BIis2ma7Or2wjQMoQL/giphy.gif"/>
</div>

---

<div align="center">
	
## 🛠 Tech Stack
</div>

<div align="center">
	
### Core Stack
</div>
<div align="center">
  <img alt="Golang" src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" />
  <img alt="Gin" src="https://img.shields.io/badge/Gin-1a4780?style=for-the-badge&logo=gin&logoColor=white" />
  <img alt="gRPC" src="https://img.shields.io/badge/gRPC-000000?style=for-the-badge&logo=grpc&logoColor=white"/>
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" />
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img alt="MongoDB Atlas" src="https://img.shields.io/badge/Atlas-388039?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</div>

<div align="center">
	
### API & DevOps
</div>
<div align="center">
  <img alt="Swagger" src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=white" />
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img alt="GitHub" src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
</div>

<div align="center">
	
### Tools & Secondary
</div>
<div align="center">
  <img alt="Jira" src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white" />
  <img alt="Miro" src="https://img.shields.io/badge/Miro-fced3f?style=for-the-badge&logo=miro&logoColor=black" />
  <img alt="Notion" src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white" />
  <img alt="Java" src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" />
  <img alt="Spring Boot" src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img alt="PyQt" src="https://img.shields.io/badge/PyQt-4584B6?style=for-the-badge&logo=pyqt&logoColor=white" />
</div>

---
<div align="center">

## 🚀 Learning Roadmap
</div>
<div align="center">
  <img alt="GitLab CI/CD" src="https://img.shields.io/badge/GitLab%20CI/CD-FCA121?style=for-the-badge&logo=gitlab&logoColor=white" />
  <img alt="Apache Kafka" src="https://img.shields.io/badge/Kafka-000000?style=for-the-badge&logo=apache-kafka&logoColor=white" />
  <img alt="Camunda BPMN" src="https://img.shields.io/badge/Camunda%20BPMN-ED1C24?style=for-the-badge&logo=camunda&logoColor=white" />
  <img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img alt="MinIO" src="https://img.shields.io/badge/MinIO-000000?style=for-the-badge&logo=minio&logoColor=white" />
  <img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
</div>
