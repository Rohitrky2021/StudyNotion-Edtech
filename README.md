# StudyFy HUB: Empowering Education with MERN  
[Explore StudyFy HUB](https://studyfy-hub-frontend.vercel.app/)  

![Homepage Preview](assets/main-screenshot.png)  

## Introduction  

**StudyFy HUB** is a robust e-learning platform built with the **MERN stack** (MongoDB, Express.js, React, Node.js). It connects learners with high-quality educational content and empowers instructors to share their expertise globally.  

**Key Objectives**:  
- Deliver an engaging, accessible learning experience for students.  
- Provide instructors with tools to create and manage courses effectively.  

This README dives into the platform’s architecture, features, and vision for the future.  

---

## Contents  
- [Architecture Overview](#architecture-overview)  
- [Frontend Details](#frontend-details)  
- [Backend Structure](#backend-structure)  
- [API Blueprint](#api-blueprint)  
- [Deployment Process](#deployment-process)  
- [Testing Strategy](#testing-strategy)  
- [Future Plans](#future-plans)  

---

## Architecture Overview  

StudyFy HUB follows a **client-server architecture**, with three core components:  

- **Frontend**: A **React.js**-powered interface for seamless user interaction.  
- **Backend**: A **Node.js** and **Express.js** server handling logic and API requests.  
- **Database**: **MongoDB** for flexible, scalable storage of course and user data.  

### Architecture Diagram  
![System Diagram](assets/system-diagram.png)  

---

## Frontend Details  

The frontend of StudyFy HUB is crafted with **React.js** for dynamic, responsive UI. **Tailwind CSS** ensures a sleek, modern design, and **Redux** manages application state for smooth performance.  

### Pages & Features  

#### For Students:  
- **Home**: Welcomes users with an overview and links to courses.  
- **Courses**: Lists all courses with descriptions, ratings, and filters.  
- **Wishlist**: Saves courses for later consideration.  
- **Checkout**: Handles secure course purchases.  
- **Course View**: Displays videos, quizzes, and materials for enrolled courses.  
- **Profile**: Manages user details like name and email.  

#### For Instructors:  
- **Dashboard**: Tracks course performance and feedback.  
- **Analytics**: Offers insights into views, enrollments, and metrics.  
- **Course Tools**: Supports creating, editing, and deleting courses.  
- **Profile Editor**: Updates instructor account information.  

#### Admin (Future Scope):  
- **Platform Dashboard**: Monitors users, courses, and revenue.  
- **User Oversight**: Manages student and instructor accounts.  
- **Content Control**: Reviews and approves course content.  

### Frontend Tech  
- **React.js**: For building interactive UI components.  
- **Tailwind CSS**: For responsive styling.  
- **Redux**: For state management.  
- **React Router**: For navigation.  

---

## Backend Structure  

The backend is a **monolithic** system built with **Node.js** and **Express.js**, paired with **MongoDB** for data storage. It integrates **Cloudinary** for media management and supports secure, scalable operations.  

### Key Features  
- **Authentication**: JWT-based login, OTP verification, and password recovery.  
- **Course Management**: APIs for course creation, updates, and deletion.  
- **Payments**: **Razorpay** integration for secure transactions.  
- **Content**: Markdown support for rich course materials.  
- **Media**: Cloudinary for storing images, videos, and documents.  

### Backend Tech  
- **Node.js**: Server runtime.  
- **Express.js**: API framework.  
- **MongoDB**: NoSQL database.  
- **Mongoose**: MongoDB object modeling.  
- **JWT & Bcrypt**: For secure authentication.  
- **Cloudinary**: For media storage.  

### Data Schema  
- **Student**: Name, email, password, enrolled courses.  
- **Instructor**: Name, email, password, published courses.  
- **Course**: Title, description, instructor, content, ratings.  

![Schema Diagram](assets/database-schema.png)  

---

## API Blueprint  

StudyFy HUB’s API adheres to **REST** principles, using **JSON** for data exchange and standard HTTP methods.  

### Key Endpoints  
- `POST /api/auth/signup`: Registers a new user.  
- `POST /api/auth/login`: Authenticates and returns a JWT.  
- `POST /api/auth/verify-otp`: Validates OTP.  
- `GET /api/courses`: Lists all courses.  
- `GET /api/courses/:id`: Retrieves a specific course.  
- `POST /api/courses`: Creates a new course.  
- `PUT /api/courses/:id`: Updates a course.  
- `DELETE /api/courses/:id`: Deletes a course.  
- `POST /api/courses/:id/rate`: Rates a course.  

### Example API Call  
**GET /api/courses**  
- **Response**:  
```json
[
  {
    "id": "abc123",
    "title": "Web Development 101",
    "description": "Learn HTML, CSS, JS",
    "rating": 4.7
  },
  ...
]
