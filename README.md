# 📊 State Statistics Management API

A complete RESTful API built using **Node.js** and **Express.js** to manage statistical data of Indian states.

This project demonstrates full REST architecture implementation including:

- ✅ GET
- ✅ POST
- ✅ PUT
- ✅ PATCH
- ✅ DELETE

⚠️ No database is used.  
All data is stored and managed in an in-memory JSON array.

---

# 🚀 Live Demo

Render Deployment Link:  
👉 https://your-render-link.onrender.com

---

# 📬 Postman Documentation

Postman Collection Link:  
👉 https://your-postman-link

All 13 routes are documented with:
- Sample requests
- Sample responses
- Status codes

---

# 🛠 Tech Stack

- Node.js
- Express.js
- CORS
- In-memory Data Structure (Array)

---

# 📂 Project Structure

```
state-statistics-api/
│
├── index.js
├── package.json
├── README.md
```

---


# 🌐 Base URL

```
https://backend-assign3-1.onrender.com/states
```

---

# 📖 API Documentation

```
https://documenter.getpostman.com/view/50839202/2sBXcHhyHJ
---

# 🔹 GET Routes (3)

---

## 1️⃣ GET /states

### Description:
Returns the complete list of states.

### Status Code:
200 OK

---

## 2️⃣ GET /states/:id

### Description:
Returns a single state by ID.

### Example:
```
GET /states/3
```

### Success Response:
200 OK

### If Not Found:
404 Not Found

```
{
  "message": "State not found"
}
```

---

## 3️⃣ GET /states/highest-gdp

### Description:
Returns the state with the highest GDP.

### Logic Used:
Array `reduce()` method.

### Status Code:
200 OK

---

# 🔹 POST Route (1)

---

## 4️⃣ POST /states

### Description:
Creates a new state.

### Request Body Example:
```
{
  "name": "New State",
  "population": 1000000,
  "literacyRate": 75.5,
  "annualBudget": 50000,
  "gdp": 3000000
}
```

### Behavior:
- Automatically generates unique ID
- Adds state to array
- Returns created object

### Status Code:
201 Created

---

# 🔹 PUT Routes (3)

PUT replaces the entire resource unless specified.

---

## 5️⃣ PUT /states/:id

### Description:
Replaces entire state record (except id).

### Status Code:
200 OK

### If Not Found:
404 Not Found

---

## 6️⃣ PUT /states/:id/budget

### Description:
Replaces only annualBudget value.

### Request:
```
{
  "annualBudget": 260000
}
```

### Status Code:
200 OK

---

## 7️⃣ PUT /states/:id/population

### Description:
Replaces population value completely.

### Status Code:
200 OK

---

# 🔹 PATCH Routes (3)

PATCH partially updates a resource.

---

## 8️⃣ PATCH /states/:id/literacy

### Description:
Updates literacyRate only.

### Status Code:
200 OK

---

## 9️⃣ PATCH /states/:id/gdp

### Description:
Updates gdp only.

### Status Code:
200 OK

---

## 🔟 PATCH /states/:id

### Description:
Updates any provided fields without replacing entire object.

### Example:
```
{
  "annualBudget": 280000
}
```

### Status Code:
200 OK

---

# 🔹 DELETE Routes (3)

---

## 1️⃣1️⃣ DELETE /states/:id

### Description:
Deletes state by ID.

### If Deleted:
204 No Content

### If Not Found:
404 Not Found

---

## 1️⃣2️⃣ DELETE /states/name/:stateName

### Description:
Deletes state by name (case-insensitive).

### Status Code:
204 No Content

---

## 1️⃣3️⃣ DELETE /states/low-literacy/:percentage

### Description:
Deletes all states where literacyRate is less than given percentage.

### Example Response:
```
{
  "deletedCount": 2
}
```

### Status Code:
200 OK

---

# 📌 HTTP Status Codes Used

| Code | Meaning |
|------|----------|
| 200  | Success |
| 201  | Resource Created |
| 204  | No Content (Deleted Successfully) |
| 404  | Resource Not Found |

---

# 🧠 Concepts Demonstrated

- RESTful API Design
- Express Middleware Usage
- Route Parameters
- Dynamic Routing
- Array Manipulation
- Resource Creation Logic
- Full Replacement (PUT)
- Partial Update (PATCH)
- Resource Deletion Logic
- Proper HTTP Status Codes
- In-memory Data Handling

---

# 📌 Assignment Requirements Covered

✔ 13 Required Routes  
✔ Proper REST Naming  
✔ Dynamic ID Generation  
✔ No Database Used  
✔ No Validation Libraries  
✔ Proper Status Codes  
✔ Business Logic Implementation  
✔ Deletion with Conditions  
✔ PUT vs PATCH Difference Demonstrated  

---

# 👨‍💻 Author

Bachhav Pritesh
Full REST Implementation Assignment  
State Statistics Management API