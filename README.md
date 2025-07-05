Floor Master CRUD API (FastAPI + MongoDB Atlas)

Project Overview
This project implements a simple CRUD (Create, Read, Update, Delete) API using FastAPI and MongoDB Atlas for managing building floor data. It supports operations like adding, viewing, updating, and deleting floor entries.

Features:
->Create floor entry with floor number and description
->Retrieve all floors
->Get floor by ID
->Update floor by ID
->Delete floor by ID


Technology Stack:

->FastAPI (Python Framework)
->MongoDB Atlas (Cloud Database)
->Uvicorn (ASGI server for running FastAPI)
->Pydantic (Data validation)
->python-dotenv (Environment variable management)

Folder Structure:

floor_master_crud/
├── main.py              # FastAPI entry point
├── models.py            # Pydantic models
├── routes.py            # API routes for CRUD
├── requirements.txt     # Project dependencies
├── .env                 # MongoDB URI and DB config (not to be shared)
├── README.md            # This file



Environment Setup (for local development)
->Clone the project
->Create virtual environment
python -m venv venv
venv\Scripts\activate  (on Windows)


Install dependencies

pip install -r requirements.txt
Set environment variables
Create a .env file and add the following:

MONGO_URI=your-mongodb-atlas-uri
DB_NAME=Floor_master
Run the project

->uvicorn main:app --reload


API Endpoints
Method	Endpoint	Description
POST	/floors/	Add a new floor
GET	/floors/	List all floors
GET	/floors/{id}	Get floor by ID
PUT	/floors/{id}	Update floor by ID
DELETE	/floors/{id}	Delete floor by ID

How to Test (using Postman)
Base URL: http://127.0.0.1:8000/floors/

Example Request Body (POST & PUT)

{
  "floor_number": 2,
  "description": "Second floor near cafeteria"
}




Author
Name: Mohammed Afnan Khan
Task: FastAPI + MongoDB CRUD API (Internship Submission)
