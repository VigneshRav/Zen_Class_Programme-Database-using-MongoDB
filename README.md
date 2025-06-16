# MongoDB Task – Zen Class Programme Database

This project demonstrates how to design and query a MongoDB database for a learning management system called **Zen Class**.

---

## 📌 Collections Overview:

Below are the collections used in the database:

1. **users** – Stores users data.
2. **codekata** – Tracks problems solved by users on CodeKata platform.
3. **attendance** – Records daily attendance status of users.
4. **topics** – Contains topics taught in class with dates.
5. **tasks** – Contains tasks assigned, linked to topics and submission info.
6. **company_drives** – Stores company placement drive details.
7. **mentors** – Stores mentor data and count of their mentees.

---

## 🗃️ Sample Document Structures:

1. Users:
{
  _id: ObjectId("user1"),
  name: "john",
  email: "john@gmail.com",
  mentor_id: ObjectId("mentor1")
}

2. Codekata:
{
  user_id: ObjectId("user1"),
  problems_solved: 15
}

3. Attendance:
{
  user_id: ObjectId("user1"),
  date: new Date("2020-10-20"),
  attendance_status: "Present"
}

4. Topics:
{
  _id: ObjectId("topic1"),
  topic_name: "JavaScript",
  date: new Date("2020-10-15")
}

5. Tasks:
{
  _id: ObjectId("task1"),
  topic_id: ObjectId("topic1"),
  task_name: "Zen Class Programme",
  date: new Date("2020-10-15"),
  submitted_by: [ObjectId("user1"), ObjectId("user2")]
}

6. Company drives:
{
  _id: ObjectId("drive1"),
  company_name: "Google",
  date: new Date("2020-10-20"),
  attended_students: [ObjectId("user1"), ObjectId("user2")]
}

7. Mentors:
{
  _id: ObjectId("mentor1"),
  name: "John",
  mentee_count: 30
}

---

## ✅ Prerequisites:

- MongoDB installed or MongoDB Atlas account.

- MongoDB Compass or shell access.

- Sample data loaded based on the schema above.

---

## 📎 Notes:

- All date filters use new Date("YYYY-MM-DD") format.

- Joins are achieved using $lookup.

- Grouping and filtering uses $project, $match, $group, $size, and $in (Aggregation Pipeline).

- Some keywords and array methods such as let, toArray() & map() are used in solving 
  the queries without using aggregations.

---

## 🙋‍♂️ Author & Contact:

- Developed by: Vignesh R
- GitHub: @VigneshRav
- Email: vignesh212000@gmail.com

---
