# Healthcare API System
A Django REST API for managing patients, doctors, and patient-doctor assignments. JWT-based authentication included.
------------------------------------------------------------------------------------------------------------------------------------
🛠️ Features
User registration and JWT login

Patient & Doctor management (CRUD)

Assign doctors to patients

Secure with JWT Auth
-----------------------------------------------------------------------------------------------------------------------------------
🚀 Setup Instructions
git clone https://github.com/yourusername/healthcare.git
cd healthcare

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start server
python manage.py runserver
----------------------------------------------------------------------------------------------------------------------------------

🔐 Authentication
Register and login to get JWT:

POST /api/auth/register/
POST /api/auth/login/
Use returned token:

Authorization: Bearer <access_token>
---------------------------------------------------------------------------------------------------------------------------------
📬 API Endpoints (Summarized)

POST    /api/auth/register/       # Register user
POST    /api/auth/login/          # Get JWT tokens

GET/POST    /api/patients/
GET/PUT/DEL /api/patients/<id>/

GET/POST    /api/doctors/
GET/PUT/DEL /api/doctors/<id>/

GET         /api/mappings/
GET         /api/mappings/<patient_id>/
POST        /api/mappings/create/
DELETE      /api/mappings/delete/<id>/
-------------------------------------------------------------------------------------------------------------------------------
