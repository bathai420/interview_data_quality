[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Framework](https://github.com/bathai420/interview_data_quality/blob/main/Framework/README.md),
[API_Status_Codes](https://github.com/bathai420/interview_data_quality/blob/main/API_Status_Codes/API_Status_Codes.md),
[HTTP_Methods_API_Guide](https://github.com/bathai420/interview_data_quality/blob/main/HTTP_Methods_API_Guide/HTTP_Methods_API_Guide.md),
[RestAssured](https://github.com/bathai420/interview_data_quality/blob/main/RestAssured/RestAssured.md),

# HTTP Methods – Complete Guide for API Testing

## 📌 Overview
HTTP methods define the **action** to be performed on a resource in a REST API.

---

## 🔹 Commonly Used HTTP Methods

| Method | Purpose | CRUD Operation |
|------|--------|----------------|
| GET | Retrieve data | Read |
| POST | Create resource / trigger action | Create |
| PUT | Update entire resource | Update |
| PATCH | Update partial resource | Update |
| DELETE | Remove resource | Delete |

---

## 1️⃣ GET – Retrieve Data

### Description
GET is used to **fetch data** from the server without modifying the resource.

### Example
```http
GET /api/pipelines/101
```

### Expected Status Codes
- 200 OK
- 404 Not Found

---

## 2️⃣ POST – Create / Trigger

### Description
POST is used to **create a new resource** or **trigger a process**.

### Example
```http
POST /api/pipelines
```

### Expected Status Codes
- 201 Created
- 200 OK
- 400 Bad Request

---

## 3️⃣ PUT – Full Update

### Description
PUT is used to **replace the entire resource** with new data.

### Example
```http
PUT /api/pipelines/101
```

### Expected Status Codes
- 200 OK
- 204 No Content

---

## 4️⃣ PATCH – Partial Update

### Description
PATCH is used to **update specific fields** of a resource.

### Example
```http
PATCH /api/pipelines/101/status
```

### Expected Status Codes
- 200 OK
- 204 No Content

---

## 5️⃣ DELETE – Remove Resource

### Description
DELETE is used to **remove a resource** from the server.

### Example
```http
DELETE /api/pipelines/101
```

### Expected Status Codes
- 204 No Content
- 200 OK
- 404 Not Found

---

## PUT vs PATCH (Interview Favorite)

| PUT | PATCH |
|----|------|
| Full resource replacement | Partial update |
| Requires full payload | Requires only changed fields |
| Higher risk of data loss | Safer |
| Always idempotent | Depends on implementation |

---

## 🧪 HTTP Method Validation in Automation

### Rest Assured (Java)
```java
given()
.when()
   .get("/api/pipelines/101")
.then()
   .statusCode(200);
```

### Playwright API (TypeScript)
```ts
const response = await request.post('/api/pipelines', {
  data: payload
});
expect(response.status()).toBe(201);
```

---

## ⭐ Best Practices
- Use correct HTTP method for each operation
- Validate both status code and response body
- Follow RESTful standards
- Handle negative scenarios
- Ensure idempotency where applicable

---