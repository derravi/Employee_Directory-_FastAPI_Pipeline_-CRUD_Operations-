EMPLOYEE DIRECTORY FASTAPI PROJECT
=================================

This project is a simple Employee Directory REST API built using FastAPI.
It performs CRUD (Create, Read, Update, Delete) operations on employee data
stored in a local JSON file.

The project is suitable for:
- FastAPI beginners
- REST API practice
- Interview/demo projects
- Learning Pydantic validation and file-based storage

--------------------------------------------------
FEATURES
--------------------------------------------------
- View all employees
- View a specific employee by ID
- Add a new employee
- Update existing employee details (partial update supported)
- Delete an employee
- Data validation using Pydantic
- JSON-based persistent storage

--------------------------------------------------
TECH STACK
--------------------------------------------------
- Python 3.9+
- FastAPI
- Pydantic
- Uvicorn
- JSON (as database)

--------------------------------------------------
PROJECT STRUCTURE
--------------------------------------------------
project-folder/
│
├── main.py              # FastAPI application
├── employee.json        # Employee data storage
├── README.txt           # Project documentation
└── requirements.txt     # Project dependencies (optional but recommended)

--------------------------------------------------
API ENDPOINTS
--------------------------------------------------
GET     /                     -> Default welcome message
GET     /employee              -> Get all employees
GET     /employee/{emp_id}     -> Get employee by ID
POST    /employee_add/         -> Add new employee
PUT     /employee_edit/{id}    -> Update employee details
DELETE  /remove_patient/{id}   -> Remove employee

--------------------------------------------------
HOW TO RUN THIS PROJECT (CMD / TERMINAL)
--------------------------------------------------

Step 1: Clone the repository
----------------------------
git clone <your-github-repo-url>
cd <project-folder-name>

Step 2: Create a virtual environment (optional but recommended)
---------------------------------------------------------------
python -m venv venv

Activate virtual environment:

Windows:
venv\Scripts\activate

Linux / Mac:
source venv/bin/activate

Step 3: Install dependencies
----------------------------
pip install fastapi uvicorn pydantic

(OR if requirements.txt exists)
pip install -r requirements.txt

Step 4: Run the FastAPI server
------------------------------
uvicorn main:app --reload

Step 5: Open browser
--------------------
API Root:
http://127.0.0.1:8000/

Swagger UI (API Documentation):
http://127.0.0.1:8000/docs

ReDoc UI:
http://127.0.0.1:8000/redoc

--------------------------------------------------
SAMPLE EMPLOYEE JSON FORMAT
--------------------------------------------------
{
  "E001": {
    "name": "John Doe",
    "email": "john@example.com",
    "department": "Backend",
    "role": "Developer",
    "date_of_joining": "2022-01-01",
    "is_active": true
  }
}

--------------------------------------------------
FUTURE IMPROVEMENTS
--------------------------------------------------
- Add database (MySQL / PostgreSQL / MongoDB)
- Authentication & Authorization
- Pagination & filtering
- Docker support
- Logging & exception handling

--------------------------------------------------
AUTHOR
--------------------------------------------------
Developed by: Der Ravi
Specialization: Python | FastAPI | Data Analytics | AI/ML

--------------------------------------------------
LICENSE
--------------------------------------------------
This project is open-source and free to use for learning and educational purposes.
