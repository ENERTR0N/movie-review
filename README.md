#Movie Review Website

This is a full-stack movie review platform where users can browse, search for, and review movies. The application allows users to view detailed movie information, rate films, and write reviews. It features a user-friendly interface and is built using React on the frontend, Spring Boot on the backend, and MongoDB for the database.

Features

Movie Database: Browse a collection of movies with detailed information such as title, synopsis, genre, cast, and release date.
User Reviews and Ratings: Authenticated users can write reviews and rate movies.
Search and Filter: Search for movies by title, genre, or release date, and filter results based on ratings or popularity.
User Authentication: Users can sign up and log in to submit reviews, rate movies, and manage a personal list of favorite or watched movies.

Tech Stack

Frontend:

HTML5, CSS3, JavaScript
React.js: For building a responsive, interactive user interface.

Backend:
Spring Boot: Java-based framework for building the RESTful API that handles business logic, user authentication, and database interaction.

Database:
MongoDB: NoSQL database to store movie details, user reviews, and ratings.

API Integration:
Integrated with external movie APIs (e.g., TMDb API or OMDb API) to fetch up-to-date movie data.

Project Structure

/movie-review-website
│
├── /frontend/              # React frontend
│   ├── /public/            # Public assets (images, HTML)
│   ├── /src/               # Source code (React components, services)
│   │   ├── /components/    # Reusable UI components (Navbar, MovieCard, etc.)
│   │   ├── /pages/         # Application pages (Home, Movie Details, etc.)
│   │   ├── /services/      # API call services (HTTP requests to backend)
│   └── package.json        # Frontend dependencies
│
├── /backend/               # Spring Boot backend
│   ├── /src/main/          # Backend source code
│   │   ├── /controller/    # REST API controllers
│   │   ├── /service/       # Business logic and services
│   │   ├── /model/         # MongoDB data models
│   │   ├── /repository/    # Data access layer (MongoDB repositories)
│   └── pom.xml             # Backend dependencies
│
└── README.md               # Project documentation

API Endpoints

User Management:

POST /api/auth/register: Register a new user.
POST /api/auth/login: Log in a user and return a token for authentication.
Movie Operations:
GET /api/movies: Fetch a list of all movies.
GET /api/movies/{id}: Fetch details of a specific movie by its ID.
Review Operations:
POST /api/movies/{id}/reviews: Add a review to a specific movie.
GET /api/movies/{id}/reviews: Get all reviews for a specific movie.

Workings of the Application:

User Flow:

Users can sign up and log in.
Once authenticated, they can search for movies, view details, and post reviews.
Users can rate movies and manage a list of favorite or watched movies.
Movie Data:

Movie data is fetched from an external API (e.g., TMDb), and user reviews are stored in MongoDB.
Frontend-Backend Communication:

The frontend sends HTTP requests to the Spring Boot backend to fetch or update data (movies, reviews, users) via RESTful APIs.
Authentication is handled using JSON Web Tokens (JWT), ensuring secure access to protected routes and features.

Future Enhancements:

Add advanced search filters (by rating, director, etc.).
Implement pagination for movie lists and reviews.
Add social media sharing options for users to share movie reviews.
Improve the UI/UX for a more seamless experience.
