# 📚 Book CRUD REST API (Spring Boot + MySQL)

A minimal and beginner-friendly RESTful API built using **Spring Boot** to perform CRUD operations on `Book` entities.  
It uses **Spring Data JPA** for DB access and integrates with a **MySQL** database. A ready-to-use **Postman collection** is also provided for quick testing.

---

## 🚀 What’s Inside

- Create, Read, Update, Delete (`Book`) APIs
- Spring Boot + Spring Data JPA setup
- MySQL DB support (Docker or local)
- Postman Collection included
- Clean and modular project structure

---

## 🔧 Tech Stack

- **Java 17+**
- **Spring Boot 3.x**
- **Spring Data JPA**
- **MySQL 8**
- **Maven**
- **Postman** (for API testing)

---

## ✅ Pre-Requisites

- JDK 17 or higher
- Maven installed
- Git (for cloning)
- MySQL (local or Docker)

---

## 🚦 Getting Started

1. **Clone this repo**
    
    ```bash
    git clone https://github.com/UrsTrulyDeep/book-crud-rest-springboot.git
    cd book-crud-rest-springboot
    ```

2. **(Optional)** Spin up MySQL using Docker
    
    ```bash
    docker run -d \
      --name book-db \
      -e MYSQL_ROOT_PASSWORD=secret \
      -e MYSQL_DATABASE=mydatabase \
      -p 3306:3306 \
      mysql:8
    ```

3. **Update DB config** in `src/main/resources/application.properties`
    
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/mydatabase
    spring.datasource.username=root
    spring.datasource.password=secret

    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    ```

4. **Run the app**
    
    ```bash
    mvn spring-boot:run
    ```

    The API will be live at: `http://localhost:8080`

---

## 🧪 API Testing (Postman)

A ready-to-import Postman collection is available at:

````

src/main/resources/Book API.postman\_collection.json

````

### Steps to Use

1. Open Postman → click **Import**
2. Select `Book API.postman_collection.json`
3. Ensure your app is running on port `8080`
4. Use the collection to test all available endpoints

---

## 📁 Folder Structure

```plaintext
book-crud-rest-springboot
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.springbootrestapi
│   │   │       ├── SpringBootRestApiApplication.java
│   │   │       ├── controller       # REST endpoints
│   │   │       ├── entity           # JPA entities (Book)
│   │   │       ├── repository       # Repository interfaces
│   │   │       └── service          # Business logic
│   │   └── resources
│   │       ├── application.properties
│   │       └── Book API.postman_collection.json
├── pom.xml
└── README.md
````

---

## 💡 Notes

* You can customize database properties in `application.properties` as needed.
* To reset the DB, just stop & remove the Docker container and re-run it.
* Swagger/OpenAPI can be added easily if needed for API docs.

---

## 🙌 Contributions

Feel free to fork, clone, or tweak this project for learning or real-world use. PRs are welcome.

---

**Maintained by:** [Deep Kushwaha](https://github.com/UrsTrulyDeep)

```
