Online Bookstore App

This project is a full-stack web application for an online bookstore built using ASP.NET Core Web API and React (TypeScript). It allows users to view a list of books stored in a database, with support for pagination, sorting, and customizable page sizes.

Features
View a list of books from a database
Pagination (default: 5 books per page)
Adjustable results per page (5, 10, 20, etc.)
Sort books by title
Styled using Bootstrap
Connected to a pre-populated SQLite database
Tech Stack
Backend
ASP.NET Core Web API
Entity Framework Core
SQLite Database
Frontend
React (TypeScript)
Axios
Bootstrap / React-Bootstrap
Database

The app uses a prebuilt SQLite database provided by the instructor. It contains book records with the following fields:

Title
Author
Publisher
ISBN
Category (Classification)
Number of Pages
Price

All fields are required and mapped to the backend model.

Setup Instructions
1. Clone the repository
git clone https://github.com/your-username/bookstore-app.git
cd bookstore-app
2. Backend Setup (ASP.NET Core)
cd BookstoreApi
dotnet restore
dotnet run

Make sure the SQLite database file is located in the correct directory (for example, /Data/Bookstore.sqlite).

Confirm your connection string in appsettings.json:

"ConnectionStrings": {
  "DefaultConnection": "Data Source=Data/Bookstore.sqlite"
}
3. Frontend Setup (React)
cd bookstore-frontend
npm install
npm start

The app will run on:
http://localhost:3000

Ensure the API is running on:
http://localhost:5000

API Endpoint
GET /api/books

Query Parameters:

page (default: 1)
pageSize (default: 5)
sort (default: Title)

Example:

http://localhost:5000/api/books?page=1&pageSize=5&sort=Title
Project Structure
bookstore-app/
│
├── BookstoreApi/          # ASP.NET Core backend
│   ├── Controllers/
│   ├── Models/
│   ├── Data/
│   └── appsettings.json
│
├── bookstore-frontend/    # React frontend
│   ├── src/
│   ├── components/
│   └── App.tsx
Author

Angelique Miller
