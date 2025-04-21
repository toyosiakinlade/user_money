# 💰 User Money API

This is a simple REST API built with **FastAPI** and **MongoDB** that allows users to register, login, create accounts, deposit/withdraw money, and view account statements.

---

## ✅ Features

### Functional Requirements

1. Users can **register** and **log in**
2. Users can **create accounts** and **view account details**
3. Users can **deposit** and **withdraw money**
4. Users can **view account statements**

### Non-Functional Requirements

1. Users **can’t withdraw more than twice in one minute**
2. User accounts are **protected using JWT authentication**

---

##  API Endpoints

###  User

- `POST /register` – Create a new user  
- `GET /login` – Login and get access token  
- `GET /token` – Refresh token  
- `GET /user/{id}` – View user info

###  Account

- `POST /accounts` – Create an account  
- `GET /accounts/{id}` – View account info  
- `POST /accounts/{id}/deposit` – Deposit money  
- `POST /accounts/{id}/withdraw` – Withdraw money  

---

## 📦 Project Setup

1. **Clone the repo**  
   ```bash
   git clone https://github.com/toyosiakinlade/user_money.git
   
2. Create and activate a virtual environment
   python -m venv venv
venv\Scripts\activate  # On Windows

3. Install requirements
   pip install -r requirements.txt
   
4. Set up .env file
Create a .env file in the root folder and add:

DB_URL=your_mongodb_connection_string
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

5.Run the server
uvicorn main:app --reload
