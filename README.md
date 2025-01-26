# Spam-Detection-API
This repository contains a Spam Detection API built using Django REST Framework (DRF). The API allows users to manage contacts, detect spam phone numbers, and mark them as spam while providing JWT-based authentication for secure access. It is designed as a robust backend service for applications requiring spam detection features.

---Features---
- User Authentication:-
- User registration with unique phone numbers and optional email.
- Login using phone number and password.
- Secure token-based authentication using JWT (JSON Web Tokens).

Spam Detection Functionalities:-
- Mark phone numbers as spam.
- Search contacts by name or phone number.
- Retrieve detailed information about specific contacts, including spam status.

Contact Management:-
- Add and manage contacts for individual users.
- Associate spam detection records with authenticated users.

Sample Data Population:-
- Populate the database with sample users and contacts for testing purposes.


---API Endpoints---
Authentication:-
- POST /register/ - Register a new user.
- POST /login/ - Login and retrieve JWT tokens.

Spam Detection:-
- POST /mark_spam/ - Mark a phone number as spam.
- GET /search/?query=<query> - Search for contacts by name or phone number.
- GET /details/<phone_number>/ - Get detailed information about a phone number.

Sample Data:-
- GET /populate_sample_data/ - Populate the database with sample data.


---Setup Instructions---
1. Clone the Repository:-
git clone https://github.com/yourusername/spam-detection-api.git
cd spam-detection-api

2. Create a Virtual Environment:-
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate

3. Install Dependencies:-
pip install -r requirements.txt

4. Run Migrations:-
python manage.py makemigrations
python manage.py migrate

5. Start the Development Server:-
python manage.py runserver

6. Test the API:-
Use tools like Postman or cURL to interact with the API endpoints.


---Tech Stack---
1. Backend Framework: Django REST Framework
2. Database: SQLite (default, can be replaced with PostgreSQL/MySQL)
3. Authentication: JWT-based authentication using rest_framework_simplejwt
4. Language: Python

   
---Future Enhancements---
- Add email-based user verification.
- Integrate advanced spam detection using machine learning.
- Support for bulk contact uploads and processing.
- Implement rate-limiting to prevent abuse of the API.
