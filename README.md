# To Do List

This project is a full-stack application that implements a **To-Do List**. It consists of a **FastAPI backend** and a **React frontend**. Below is an overview of how the application works.

---

## Backend (FastAPI)
The backend is responsible for handling server-side logic, including database interactions and API endpoints. It is implemented using **FastAPI** and **SQLAlchemy**.

### Key Features:
1. **Database**:
   - Uses **SQLite** as the database engine (stored in the `test.db` file).
   - SQLAlchemy is used for ORM (Object-Relational Mapping) to interact with the database.

2. **Models**:
   - Database tables are defined as Python classes in `FastAPI/models.py`.

3. **Schemas**:
   - Pydantic schemas in `FastAPI/schemas.py` are used for data validation and serialization.

4. **CRUD Operations**:
   - Functions for Create, Read, Update, and Delete operations are implemented in `FastAPI/crud.py`.

5. **API Endpoints**:
   - RESTful API routes are defined in `FastAPI/main.py` to expose CRUD operations.

6. **Dependency Injection**:
   - The `get_db` function in `FastAPI/database.py` provides a database session to the API endpoints.

---

## Frontend (React)
The frontend provides the user interface for interacting with the backend. It is implemented using **React**.

### Key Features:
1. **UI Components**:
   - The main UI logic is implemented in `src/App.js` and `src/ToDoList.jsx`.
   - These components render the to-do list and handle user interactions.

2. **API Integration**:
   - The frontend communicates with the backend using **Axios**, which is configured in `src/API.js`.

3. **State Management**:
   - React's state and props are used to manage the application's data, such as the list of to-do items.

4. **Styling**:
   - CSS files like `src/App.css` and `src/index.css` are used to style the application.

5. **Development and Build**:
   - The React app can be run in development mode using `npm start` or built for production using `npm run build`.

---

## Interaction Between Backend and Frontend
- The React frontend sends HTTP requests (e.g., GET, POST, PUT, DELETE) to the FastAPI backend to perform operations like adding, retrieving, updating, or deleting to-do items.
- The FastAPI backend processes these requests, interacts with the database, and sends responses (usually in JSON format) back to the frontend.
- The frontend updates the UI based on the responses from the backend.

---

## How to Run the Application

### Prerequisites:
- **Node.js** and **npm** installed for the React frontend.
- **Python** installed for the FastAPI backend.

### Steps:
1. **Backend**:
   - Navigate to the `FastAPI` folder.
   - Install dependencies: `pip install -r requirements.txt`.
   - Start the FastAPI server: `uvicorn main:app --reload`.

2. **Frontend**:
   - Navigate to the `my-react-app` folder.
   - Install dependencies: `npm install`.
   - Start the React development server: `npm start`.

3. **Access the Application**:
   - Open your browser and go to `http://localhost:3000` to view the frontend.
   - The backend API will be available at `http://localhost:8000`.

---

## Folder Structure
```
Fullstackapp/
├── FastAPI/
│   ├── crud.py
│   ├── database.py
│   ├── main.py
│   ├── models.py
│   ├── schemas.py
│   ├── test.db
├── my-react-app/
│   ├── package.json
│   ├── public/
│   │   ├── index.html
│   ├── src/
│   │   ├── API.js
│   │   ├── App.js
│   │   ├── ToDoList.jsx
│   │   ├── App.css
│   │   ├── index.js
```

---

## Technologies Used
- **Backend**: FastAPI, SQLAlchemy, SQLite
- **Frontend**: React, Axios

---

## Author
Ahmed Tamer

---

## License
This project is licensed under the MIT License.
