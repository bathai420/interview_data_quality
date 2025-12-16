# REST ASSURED

<!-- TOC --> 
[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Framework](https://github.com/bathai420/interview_data_quality/blob/main/Framework/README.md),
[RestAssured](https://github.com/bathai420/interview_data_quality/blob/main/RestAssured/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md),
[AMBIGUITY](https://github.com/bathai420/interview_data_quality/blob/main/Ambiguity/README.md),
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md),
[Data Quality](https://github.com/bathai420/interview_data_quality/blob/main/DataQuality/README.md),
[FRAUD DATA](https://github.com/bathai420/interview_data_quality/blob/main/FraudData/README.md),
[Work Environment](https://github.com/bathai420/interview_data_quality/blob/main/WorkEnvironment/README.md),
[New Skill](https://github.com/bathai420/interview_data_quality/blob/main/NewSkill/README.md),
[Cross-Functional](https://github.com/bathai420/interview_data_quality/blob/main/CrossFunctional/README.md),
[Issues](https://github.com/bathai420/interview_data_quality/blob/main/Issues/README.md),
[Projects](https://github.com/bathai420/interview_data_quality/blob/main/Projects/README.md),
[Questions](https://github.com/bathai420/interview_data_quality/blob/main/Questions/README.md),
[Mistake](https://github.com/bathai420/interview_data_quality/blob/main/Mistake/README.md),
[COTA](https://github.com/bathai420/interview_data_quality/blob/main/COTA/README.md),
[JOINs](https://github.com/bathai420/interview_data_quality/blob/main/Joins/README.md),
[DataAnalysis](https://github.com/bathai420/interview_data_quality/blob/main/DataAnalysis/README.md)

REST Assured is a Java library for API automation testing. it is used to REST API testing without manual HTTP handling.
---

## 📥 What is a Request in REST Assured?
Requests — a request defines the API call configuration, including the endpoint, HTTP method, headers, parameters, authentication, and request body sent to the server.
## 🧩 `given()` – Request Specification

The `given()` method is used to **build and configure the API request** before sending it to the server.

### Example: Request Configuration

```java
given()
    .baseURI("https://api.example.com")
    .header("Content-Type", "application/json")
    .queryParam("id", 10);
```

### 🔍 Explanation:
- `baseURI()` → Defines the API base URL
- `header()` → Adds request headers
- `queryParam()` → Adds query parameters to the request
- `given()` → Starts building the request specification

---

## 📥 What is a Authentication & Authorization in REST Assured?
Authentication verifies who the user is, while Authorization determines what the user is allowed to access.
### Example: Authentication & Authorization Configuration

```java
given()
            .baseURI("https://api.example.com")
            .auth().oauth2("valid_access_token")   // 🔐 Authentication
        .when()
            .get("/pipelines")
        .then()
            .statusCode(200);                      // Authenticated successfully
```
---

## 📥 What is HTTP Methods in REST Assured?
In REST Assured, HTTP methods are used to perform CRUD (creating, retrieving, updating, or deleting) operations on API resources and validate their responses.
### get - Retrieve data
```java
given()
    .baseURI("https://api.example.com")
.when()
    .get("/users/1")
.then()
    .statusCode(200);
```
### POST – Create data
```java
given()
    .baseURI("https://api.example.com")
    .header("Content-Type", "application/json")
    .body("{ \"name\": \"John\", \"role\": \"QA\" }")
.when()
    .post("/users")
.then()
    .statusCode(201);
```
### PUT – Update entire resource
```java
given()
    .baseURI("https://api.example.com")
    .header("Content-Type", "application/json")
    .body("{ \"name\": \"John\", \"role\": \"QA\" }")
.when()
    .post("/users")
.then()
    .statusCode(201);
```
### PATCH – Partial update
```java
given()
    .baseURI("https://api.example.com")
    .header("Content-Type", "application/json")
    .body("{ \"role\": \"Lead SDET\" }")
.when()
    .patch("/users/1")
.then()
    .statusCode(200);
```
### DELETE – Remove resource
```java
given()
    .baseURI("https://api.example.com")
.when()
    .delete("/users/1")
.then()
    .statusCode(204);
```

## 📥 What is Response Validation in REST Assured?
is used to verify that the API response meets expectations by checking status codes, response body, headers, and response time.
```java
given()
    .baseURI("https://api.example.com")
.when()
    .get("/users/1")
.then()
    .statusCode(200)                          // Status code validation
    .body("name", equalTo("John"))            // Response body validation
    .header("Content-Type", containsString("application/json")) // Header validation
    .time(lessThan(2000L));                   // Response time validation
```

## 📥 What is JSON & XML Parsing in REST Assured?
is used to extract and validate specific values from API responses using JsonPath or XmlPath.
```java
given()
Response response =
    given()
        .baseURI("https://api.example.com")
    .when()
        .get("/users/1");

JsonPath jsonPath = response.jsonPath();

// Extract values from JSON response
String name = jsonPath.getString("name");
int id = jsonPath.getInt("id");

// Validation
System.out.println(name);
System.out.println(id);
```

[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Framework](https://github.com/bathai420/interview_data_quality/blob/main/Framework/README.md),
[RestAssured](https://github.com/bathai420/interview_data_quality/blob/main/RestAssured/README.md),
[Interest](https://github.com/bathai420/interview_data_quality/blob/main/Interest/README.md),
[AMBIGUITY](https://github.com/bathai420/interview_data_quality/blob/main/Ambiguity/README.md),
[DATA GOVERNANCE](https://github.com/bathai420/interview_data_quality/blob/main/DataGovernance/README.md),
[Data Quality](https://github.com/bathai420/interview_data_quality/blob/main/DataQuality/README.md),
[FRAUD DATA](https://github.com/bathai420/interview_data_quality/blob/main/FraudData/README.md),
[Work Environment](https://github.com/bathai420/interview_data_quality/blob/main/WorkEnvironment/README.md),
[New Skill](https://github.com/bathai420/interview_data_quality/blob/main/NewSkill/README.md),
[Cross-Functional](https://github.com/bathai420/interview_data_quality/blob/main/CrossFunctional/README.md),
[Issues](https://github.com/bathai420/interview_data_quality/blob/main/Issues/README.md),
[Projects](https://github.com/bathai420/interview_data_quality/blob/main/Projects/README.md),
[Questions](https://github.com/bathai420/interview_data_quality/blob/main/Questions/README.md),
[Mistake](https://github.com/bathai420/interview_data_quality/blob/main/Mistake/README.md),
[Conflict](https://github.com/bathai420/interview_data_quality/blob/main/Conflict/README.md),
[COTA](https://github.com/bathai420/interview_data_quality/blob/main/COTA/README.md)