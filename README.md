# Spring Boot Demo – HelloController

Detta är ett enkelt Spring Boot-projekt containeriserat med Docker och Docker Compose.
Projektet innehåller en REST-endpoint som returnerar en hälsning.

## ✅ Funktionalitet

Projektet har en enkel REST-endpoint:
GET /hello

Den returnerar följande svar i webbläsaren eller via API-anrop:
"Hej från Spring Boot!"


---

🚀 Installation & körning

1️⃣ Kloning av repository
För att komma igång, klona projektet från GitHub:
git clone https://github.com/QULLi/springboot-demo-hellocontroller.git
cd springboot-demo-hellocontroller

2️⃣ Köra applikationen lokalt med Maven
Om du vill köra applikationen utan Docker:
mvn spring-boot:run
Gå till: http://localhost:8080/hello

3️⃣ Bygga och köra med Docker
Bygg Docker-imagen:
docker build -t springboot-demo:latest .
Kör containern:
docker run -p 8080:8080 springboot-demo:latest
Gå till: http://localhost:8080/hello

🐳 Docker Compose
För enklare hantering av containern kan du använda Docker Compose.

1. Bygg och starta containern:
docker-compose up --build -d

Flaggor:
--build säkerställer att en ny build görs vid behov.
-d kör containern i bakgrunden.

2. Kontrollera att containern körs:
docker ps

3. Stoppa och radera containern:
docker-compose down

📁 Projektstruktur
Projektet är organiserat enligt Maven/Spring Boot-konventionen:
.
├── Dockerfile
├── docker-compose.yml
├── README.md
├── pom.xml
├── src/
│   └── main/
│       ├── java/com/example/demo/
│       │   ├── DemoApplication.java
│       │   └── HelloController.java
│       └── resources/application.properties

📜 Licens
Detta projekt kan användas under MIT-licens eller annan valfri licens.
