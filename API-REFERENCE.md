# API Documentation

## Overview  
This document contains the API reference for the **Independence Services NZ** application. It includes information on the available endpoints, request/response examples, error codes, and authentication details.

## Authentication  
To access the API, you need to include an API key in the request headers. You can obtain an API key by registering on our platform.

### Example Authentication Header  
```
Authorization: Bearer YOUR_API_KEY
```

## Endpoints  

### 1. Get All Services  
- **Endpoint:** `/api/services`  
- **Method:** `GET`  
- **Description:** Retrieves a list of all available services.

#### Request Example  
```http
GET /api/services HTTP/1.1
Host: api.independenceservicesnz.com
Authorization: Bearer YOUR_API_KEY
```

#### Response Example  
```json
[
  {
    "id": 1,
    "name": "Service A",
    "description": "Description of Service A."
  },
  {
    "id": 2,
    "name": "Service B",
    "description": "Description of Service B."
  }
]
```

#### Error Codes  
- **401 Unauthorized:** API key is missing or invalid.  
- **500 Internal Server Error:** Something went wrong on the server.

---

### 2. Create a New Service  
- **Endpoint:** `/api/services`  
- **Method:** `POST`  
- **Description:** Creates a new service.

#### Request Example  
```http
POST /api/services HTTP/1.1
Host: api.independenceservicesnz.com
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "name": "New Service",
  "description": "Description of New Service."
}
```

#### Response Example  
```json
{
  "id": 3,
  "name": "New Service",
  "description": "Description of New Service."
}
```

#### Error Codes  
- **400 Bad Request:** Invalid input data.  
- **401 Unauthorized:** API key is missing or invalid.  
- **500 Internal Server Error:** Something went wrong on the server.

---

### 3. Update a Service  
- **Endpoint:** `/api/services/{id}`  
- **Method:** `PUT`  
- **Description:** Updates an existing service.

#### Request Example  
```http
PUT /api/services/1 HTTP/1.1
Host: api.independenceservicesnz.com
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "name": "Updated Service",
  "description": "Updated description."
}
```

#### Response Example  
```json
{
  "id": 1,
  "name": "Updated Service",
  "description": "Updated description."
}
```

#### Error Codes  
- **404 Not Found:** Service not found.  
- **400 Bad Request:** Invalid input data.  
- **401 Unauthorized:** API key is missing or invalid.  
- **500 Internal Server Error:** Something went wrong on the server.

---

### 4. Delete a Service  
- **Endpoint:** `/api/services/{id}`  
- **Method:** `DELETE`  
- **Description:** Deletes a service.

#### Request Example  
```http
DELETE /api/services/1 HTTP/1.1
Host: api.independenceservicesnz.com
Authorization: Bearer YOUR_API_KEY
```

#### Response Example  
```json
{
  "message": "Service deleted successfully."
}
```

#### Error Codes  
- **404 Not Found:** Service not found.  
- **401 Unauthorized:** API key is missing or invalid.  
- **500 Internal Server Error:** Something went wrong on the server.

---