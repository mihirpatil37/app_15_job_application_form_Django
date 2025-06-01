# Job Application Form using Django
A simple Django web application that allows users to submit job applications via a form. The submitted data is stored in a database and a confirmation email is sent to the applicant. The app also features an admin panel and a responsive Bootstrap UI.



## 📂 Project Structure
```
├── job_application/
│   ├── admin.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   ├── views.py
│   └── templates/
│       ├── base.html
│       ├── index.html
│       └── about.html
├── db.sqlite3
├── manage.py
└── mysite/
    └── urls.py
```


## 🚀 Features

- 📋 Submit job applications (first name, last name, email, availability, occupation)
- 💾 Save applications to SQLite database
- 📧 Send automatic confirmation email to applicant
- 🔐 Admin panel with filters and search
- 🧭 Responsive UI using Bootstrap 5
- 📄 Static About page and navigation

---

## 🔧 Setup Instructions

### 1. Clone the repository

```bash
[git clone https://github.com/mihirpatil37/job-application-django.git](https://github.com/mihirpatil37/app_15_job_application_form_Django.git)
cd job_application_form_Django
```

### 2. Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
### 3. Install dependencies
```bash
pip install django
```
### 4. Configure Email Settings
```bash
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = "smtp.gmail.com"
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = "your_email@gmail.com"
EMAIL_HOST_PASSWORD = "your_app_password"
```
### 5. Run database migrations
```bash
python manage.py migrate
```
### 6. (Optional) Create a superuser
```bash
python manage.py runserver
```
## Functionality Overview
### Job Application Form
Users can enter:
- First Name
- Last Name
- Email Address
- Available Start Date
- Occupation (via radio buttons)
### After form submission:
- Data is validated and saved to the database
- A confirmation email is sent to the applicant
- A success message is displayed
## Admin Panel
Visit http://127.0.0.1:8000/admin/ to:
- View submitted applications
- Filter by occupation or start date
- Search by name or email
- Use Django’s built-in features

## 🧭 Navigation
A Bootstrap-based navbar links to:
- Home
- About (with extendable content)
- Contact (placeholder)

## 📬 Email Confirmation Logic
Handled inside views.py:
```bash
python
email_message = EmailMessage(
    "Form Submitted Confirmation",
    f"A new job application was submitted. Thank you, \n{first_name}.",
    to=[email]
)
email_message.send()
```
## 📄 License
This project is licensed under the MIT License.

## 👨‍💻 Author
Developed by Mihir Patil

### 💡 Feel free to contribute, suggest improvements, or report issues via GitHub.
