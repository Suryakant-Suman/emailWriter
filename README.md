# 📧 Email Writer using Gemini API

A Spring Boot application that generates **professional email replies** using **Google Gemini API**.  
This project takes input email content and tone (formal, friendly, polite, etc.) and generates a well-structured response automatically.

---

## 🚀 Features
- ✨ Generate AI-powered professional email replies
- 🔧 Built with **Spring Boot** and **WebClient**
- 🔒 Secure API key handling via `application.properties`
- 📝 Customizable tone (formal, casual, polite, etc.)
- ⚡ Uses **Google Gemini 2.5 Flash model** for fast responses

---

## 🛠️ Tech Stack
- **Java 17+**
- **Spring Boot 3**
- **Spring WebFlux (WebClient)**
- **Google Gemini API**
- **Maven**

---

## 📂 Project Structure
emailWriter/
│── src/main/java/com/surya/email_writer/
│ ├── controller/ # REST Controllers
│ ├── dto/ # Data Transfer Objects (EmailRequest, etc.)
│ ├── service/ # Business logic (EmailGeneratorService)
│ └── EmailWriterApplication.java
│
│── src/main/resources/
│ ├── application.properties
│
│── pom.xml # Maven dependencies
│── README.md # Documentation



---

## ⚙️ Setup & Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Suryakant-Suman/emailWriter.git
cd emailWriter
```

---
2️⃣ Configure API Key

Update src/main/resources/application.properties:
```bash
gemini.api.url=https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent
gemini.api.key=YOUR_API_KEY_HERE
```
---
3️⃣ Build & Run
```bash
mvn clean install
mvn spring-boot:run
```
The application will start on http://localhost:8080
---

📡 API Endpoints
Generate Email Reply

POST /api/email/generate

Request Body
```bash
{
  "emailContent": "Hi, can you share the project report by tomorrow?",
  "tone": "polite"
}
```
Response
```bash
{
  "reply": "Hello, I will make sure to send you the project report by tomorrow. Thank you for your patience."
}
```
---
🧩 Example Usage
cURL
```bash
curl -X POST http://localhost:8080/api/email/reply \
-H "Content-Type: application/json" \
-d '{"emailContent": "Can we reschedule our meeting?", "tone": "formal"}'
```
---
🔮 Future Enhancements

✅ Add frontend (React.js) for user-friendly UI

✅ Support multiple languages

✅ Save generated emails in a database
---
👨‍💻 Author

Suryakant Suman
🔗 GitHub Profile

🔗 LinkedIn
