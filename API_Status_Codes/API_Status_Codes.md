[About](https://github.com/bathai420/interview_data_quality/blob/main/About/README.md),
[Framework](https://github.com/bathai420/interview_data_quality/blob/main/Framework/README.md),
[RestAssured](https://github.com/bathai420/interview_data_quality/blob/main/RestAssured/README.md),
[API_Status_Codes](https://github.com/bathai420/interview_data_quality/blob/main/API_Status_Codes/API_Status_Codes.md),
[HTTP_Methods_API_Guide](https://github.com/bathai420/interview_data_quality/blob/main/HTTP_Methods_API_Guide/HTTP_Methods_API_Guide.md),


# API Status Codes – Quick Reference Guide

HTTP status codes are standard response codes returned by APIs to indicate the result of a client request.

---

## 📊 Status Code Categories

| Category | Description |
|--------|-------------|
| 1xx | Informational responses |
| 2xx | Successful responses |
| 3xx | Redirection responses |
| 4xx | Client-side errors |
| 5xx | Server-side errors |

---

## ✅ 2xx – Success Status Codes

| Status Code | Meaning | Real-Time Usage |
|-----------|--------|----------------|
| 200 OK | Request successful | GET, PUT, PATCH |
| 201 Created | Resource created | POST create APIs |
| 202 Accepted | Request accepted for async processing | ETL / job trigger |
| 204 No Content | Success with no response body | DELETE APIs |

Example:
GET /api/pipelines/101  
Status: 200 OK

---

## 🔁 3xx – Redirection Status Codes

| Status Code | Meaning |
|-----------|--------|
| 301 | Moved Permanently |
| 302 | Found |
| 304 | Not Modified |

Mostly seen in authentication redirects or caching scenarios.

---

## ❌ 4xx – Client Error Status Codes

| Status Code | Meaning | Example Scenario |
|-----------|--------|------------------|
| 400 Bad Request | Invalid request payload | Missing mandatory field |
| 401 Unauthorized | Missing or expired token | OAuth token expired |
| 403 Forbidden | No access permission | Role-based restriction |
| 404 Not Found | Resource not found | Invalid ID |
| 409 Conflict | Duplicate request | Creating same resource |
| 422 Unprocessable Entity | Business validation failed | Invalid configuration |
| 429 Too Many Requests | Rate limit exceeded | API throttling |

---

## 🔥 5xx – Server Error Status Codes

| Status Code | Meaning | Example |
|-----------|--------|--------|
| 500 Internal Server Error | Unhandled exception | Backend crash |
| 502 Bad Gateway | Invalid upstream response | API Gateway issue |
| 503 Service Unavailable | Server down | Maintenance |
| 504 Gateway Timeout | Backend timeout | Long-running ETL job |

---

## 🧪 Status Code Validation in Automation

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
const response = await request.get('/api/pipelines/101');
expect(response.status()).toBe(200);
```

---

## ⭐ Best Practices
- Always validate status code and response body
- Match status codes with business behavior
- Handle negative scenarios explicitly
- Log request/response for 4xx and 5xx failures
- Do not ignore 5xx errors in automation
