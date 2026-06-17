# Goslish Trac — Product Tracking Demo

A full-stack CRUD application built with **FastAPI** (backend) and **React** (frontend) for managing products.

## Features

- Create, Read, Update, Delete products
- Sortable table by ID, Name, Price, Quantity
- Search/filter products by ID, name, or description
- Responsive UI with real-time feedback

## Tech Stack

| Layer    | Technology             |
| -------- | ---------------------- |
| Backend  | Python, FastAPI, SQLAlchemy, MySQL |
| Frontend | React, Axios           |
| Database | MySQL                  |

## Prerequisites

- Python 3.10+
- Node.js 18+
- MySQL server running locally

## Setup

### 1. Clone and configure

```bash
git clone <repo-url>
cd fastAPIProductTrackDemo
```

### 2. Backend

```bash
# Create a virtual environment (optional)
python -m venv env

# Activate it
.\env\Scripts\activate   # Windows
source env/bin/activate  # Linux/macOS

# Install dependencies
pip install fastapi uvicorn sqlalchemy pymysql python-dotenv

# Copy environment config and fill in your MySQL credentials
cp .env.example .env
```

Edit `.env` with your MySQL credentials:

```
DB_USERNAME=root
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=3306
DB_NAME=crud_with_fastapi
```

Run the backend:

```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`.

### 3. Frontend

```bash
cd frontend
npm install
npm start
```

The UI will be available at `http://localhost:3000`.

## API Endpoints

| Method | Endpoint          | Description        |
| ------ | ----------------- | ------------------ |
| GET    | `/`               | Welcome message    |
| GET    | `/products`       | List all products  |
| GET    | `/products/{id}`  | Get product by ID  |
| POST   | `/products/`      | Create a product   |
| PUT    | `/products/{id}`  | Update a product   |
| DELETE | `/products/{id}`  | Delete a product   |
