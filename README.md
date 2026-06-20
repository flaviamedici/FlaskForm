# 📋 Online Registration Form with Flask

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge\&logo=python)
![Flask](https://img.shields.io/badge/Flask-Web%20Application-black?style=for-the-badge\&logo=flask)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-ORM-red?style=for-the-badge)
![SQLite](https://img.shields.io/badge/SQLite-Database-blue?style=for-the-badge\&logo=sqlite)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

A Flask web application that allows users to submit a registration form, stores submissions in a SQLite database, and sends a confirmation email upon successful registration.

This project demonstrates how to integrate:

* Flask web development
* SQLAlchemy ORM
* SQLite database management
* Email notifications with Flask-Mail
* Form handling and validation
* Flash messages for user feedback

---

# 🚀 Features

✅ User registration form

✅ Store submissions in SQLite database

✅ Automatic database table creation

✅ Confirmation email notifications

✅ Flash success messages

✅ SQLAlchemy ORM integration

✅ Responsive Flask backend

---

# 📸 Application Workflow

```text
User submits form
         ↓
Flask receives data
         ↓
Data saved to SQLite
         ↓
Confirmation email generated
         ↓
Success message displayed
```

---

# 🛠️ Technologies Used

| Technology | Purpose             |
| ---------- | ------------------- |
| Python     | Backend programming |
| Flask      | Web framework       |
| SQLAlchemy | Database ORM        |
| SQLite     | Local database      |
| Flask-Mail | Email notifications |
| HTML       | Frontend template   |

---

# 📂 Project Structure

```bash
project-folder/
│
├── app.py
├── data.db
│
├── templates/
│   └── index.html
│
├── static/
│
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/flask-registration-form.git

cd flask-registration-form
```

---

## 2️⃣ Create a Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install flask flask-sqlalchemy flask-mail
```

Or:

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Application

```bash
python app.py
```

The application will start on:

```bash
http://127.0.0.1:5001
```

---

# 🗄️ Database Schema

The application stores submissions in a SQLite database using SQLAlchemy.

### Form Table

| Field      | Type                  |
| ---------- | --------------------- |
| id         | Integer (Primary Key) |
| first_name | String                |
| last_name  | String                |
| email      | String                |
| date       | Date                  |
| occupation | String                |

Model definition:

```python
class Form(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    first_name = db.Column(db.String(80))
    last_name = db.Column(db.String(80))
    email = db.Column(db.String(80))
    date = db.Column(db.Date)
    occupation = db.Column(db.String(80))
```

---

# 📧 Email Notifications

After a successful form submission, the application generates a confirmation email containing:

* First name
* Last name
* Submission date
* Thank-you message

Example:

```text
Thank you for your submission, John Smith!

Here are your data:

John
Smith
2025-01-15

Thank you
```

---

# 🔄 Application Process

1. User fills out the registration form
2. Flask receives the form data
3. Data is converted and validated
4. Information is stored in SQLite
5. Confirmation email is generated
6. Success message is displayed

---

# 💡 Key Flask Concepts Demonstrated

### Form Handling

```python
request.form['first_name']
```

### Database Operations

```python
db.session.add(form)
db.session.commit()
```

### Flash Messages

```python
flash("Form submitted successfully", "success")
```

### Email Notifications

```python
message = Message(
    subject="New Form Submission",
    sender=app.config['MAIL_USERNAME'],
    recipients=[email],
    body=message_body
)
```

---

# 🔥 Future Improvements

* Send emails asynchronously
* Add form validation
* Password-protected admin dashboard
* Search and filter submissions
* Export submissions to CSV
* Add Bootstrap styling
* Deploy to Render or Railway
* Add CAPTCHA protection

---

# 🐛 Known Limitations

* Email credentials are stored in configuration
* No authentication system
* Minimal form validation
* SQLite is intended for small-scale applications
* Email sending logic is not fully implemented

---

# 📚 Learning Outcomes

This project demonstrates:

* Flask application structure
* Working with SQLAlchemy ORM
* SQLite database management
* Form processing with Flask
* Sending emails using Flask-Mail
* Flash messages and user feedback
* CRUD fundamentals

---

# 👩‍💻 Author

Developed by Flavia Medici

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.

Feedback and contributions are always welcome!

