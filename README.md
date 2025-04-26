
# MongoDB-Based Student Management System

## 📚 Project Overview
This project is a MongoDB-based Student Management System designed to manage student records, including personal details and course enrollments. 
It covers complete backend operations like schema design, CRUD operations, indexing, and database relationships.

---

## 🚀 Features
- Database setup using MongoDB (local/Atlas)
- Students and Courses collections creation
- Full CRUD operations implementation
- One-to-Many relationship between Students and Courses
- Indexing for fast searches and data uniqueness
- Data retrieval with `$lookup` aggregation

---

## 🛠️ Technologies Used
- MongoDB
- Mongo Shell / Compass
- JavaScript (optional for scripting)
- Node.js with Mongoose (optional)

---

## 📦 Project Structure
- `students` collection: Stores student details with enrolled course IDs
- `courses` collection: Stores course details
- `$lookup`: Fetches enrolled course details along with student data

---

## 🔥 How to Run
1. Install MongoDB locally or create an account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
2. Connect to your database.
3. Create a new database called `student_management`.
4. Insert documents using provided Mongo Shell commands or use MongoDB Compass GUI.
5. Perform CRUD operations and experiment with indexing and relationships.

---

## 📜 Example Commands

### Create Database and Collections
```bash
use student_management
```

### Insert Sample Documents
```javascript
db.courses.insertMany([
  { courseName: "Computer Science", instructor: "Dr. Smith", credits: 4 },
  { courseName: "Mathematics", instructor: "Prof. Adams", credits: 3 }
]);

db.students.insertOne({
  name: "John Doe",
  email: "john@example.com",
  age: 20,
  enrolledCourses: [],
  createdAt: new Date()
});
```

### Create Indexes
```javascript
db.students.createIndex({ email: 1 }, { unique: true });
db.courses.createIndex({ courseName: "text" });
```

---

## ✨ Author
- **Tejasree Arepalli**

---

## 📎 Additional Notes
- MongoDB relationships are demonstrated through `ObjectId` references and `$lookup` aggregation.
- Ensure MongoDB server is running during testing.
- Node.js + Mongoose can be used to automate these operations further.

---

⭐ Happy Learning with MongoDB! ⭐
