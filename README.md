# Apron101-Aviation-Campus-Project 
Apron101 | Aviation Campus Project | Full-Stack Project Management Documentation

## INTRODUCTION
### ✈Overview 
Apron 101 is a full-stack web application designed to provide aviation professionals and enthusiasts with a comprehensive and user-friendly platform. The goal of the project is to create a valuable resource for those working or interested in aviation by blending educational content with practical tools.
### ✈Project Features
Apron101 Aviation Campus consists of below sections:
- Aviation dictionary with terms and abbreviations,
- The Aviation 101 section features articles covering foundational knowledge about aviation, 
- The Technical Knowledge Hub includes in-depth technical information such as aircraft and engine components, aircraft types, and related articles.
### ✈Live Demo
[Check out the live site ➤ Apron101](https://www.apron101.com/)

## DEVELOPMENT PROCESS
### 👩‍💻Technologies Used
#### BACKEND
###### Development Tools
- **Java 17:** The project uses Java 17 as the primary programming language.
- **Spring Boot 3.x:** For rapid application development and handling REST API endpoints.
###### Database:
- **PostgreSQL:** The database used to store aviation-related data, such as terms, articles, and user information.
- **Neon DB:** A cloud-based PostgreSQL database for reliable data storage.
- **Google Cloud:** A cloud-based solution for image storage.
###### Libraries:
- **Spring Data JPA:** Integrated for Object-Relational Mapping (ORM), enabling easy data manipulation and retrieval.
- **Hibernate:** Used for ORM to map Java objects to database tables.
- **Lombok:** Simplifies Java code by generating boilerplate code like getters, setters, and constructors.
- **Model Mapper:** For converting data between different layers, e.g., from entities to DTOs.
- **JWT (JSON Web Token):** For secure authentication and authorization of users via token-based systems.
- **Spring Security:** Used to handle security aspects like user authentication and authorization, ensuring that sensitive data is protected.

#### FRONTEND
###### Development Tools
- **React:** A JavaScript library for building user interfaces, enabling the development of reusable components.
- **TypeScript:** A superset of JavaScript, providing static typing and enhancing code quality and maintainability.
###### Libraries and Frameworks
- **React Router DOM:** For routing and navigation in the React application, allowing for smooth client-side transitions.
- **Redux:** A state management library for managing and centralizing the state of the application.
- **Redux Toolkit:** A set of tools for Redux that simplifies the development process and reduces boilerplate code.
- **React-Redux:** The official Redux bindings for React, enabling seamless integration between Redux and React components.
- **Formik:** A library for building and handling forms in React, simplifying form state management and validation.
- **Yup:** A JavaScript schema builder for validation, used with Formik to validate forms.
- **Axios:** A promise-based HTTP client for making API requests to the backend.
- **Axios Token Interceptor:** An Axios interceptor that helps in managing token-based authentication for API requests.
- **JWT Decode:** A library used for decoding JSON Web Tokens (JWT) to extract user information after authentication.
- **React Toastify:** A library for adding toast notifications to React applications, providing feedback to users for events like success or errors.
- **Bootstrap:** A CSS framework that provides responsive grid systems and pre-built components for faster frontend development.
###### Development Dependencies
- **@types/axios:** TypeScript types for the Axios library to enhance development with type safety.
- **@types/jwt-decode:** TypeScript types for the JWT Decode library.
- **@types/redux-persist:** TypeScript types for Redux Persist, which helps persist the Redux state across browser sessions.

#### Deployment
- **Frontend**: The frontend is deployed on [Vercel](https://vercel.com/) for fast, scalable, and reliable hosting with built-in CI/CD support.
- **Backend**: The backend is hosted on [Render](https://render.com/), ensuring a secure and efficient server environment for API handling.


### 👩‍💻Design and Architecture
#### Backend Architecture
The backend of the Apron101 project follows an N-Layered Architecture pattern, which promotes separation of concerns and modularity. The architecture is divided into distinct layers, each with specific responsibilities:
- **Controller Layer:** Acts as the intermediary between the frontend and backend, handling HTTP requests and responses. It includes controllers that process incoming requests and delegate them to the appropriate services for further action.
- **Service Layer:** Contains the application's business logic and orchestrates operations across different layers. This layer ensures seamless coordination between various services to meet business needs.
- **Core Layer:** Centralizes the core business logic and entities, operating independently of external services or infrastructure. This isolation helps maintain the integrity and consistency of business rules.
- **Repository Layer:** Manages interactions with data sources, external services, and third-party libraries. It handles database operations, API communications, and other external system integrations, ensuring that data is accessible and reliable for the upper layers.
- **Entity Layer:** Defines the core data structures and models used throughout the application. It encapsulates the essential attributes and behaviors of the domain, serving as a foundation for the business logic.
This architecture ensures a clear separation of concerns, making the system more maintainable, scalable, and testable. 
I leveraged the advantages of **Object-Oriented Programming (OOP)** principles, such as interfaces, dependency injection, and abstract classes, to enhance the application's flexibility and scalability. By adhering to these principles, the system is designed to facilitate the seamless addition of new features and to adapt swiftly to evolving requirements, ensuring a robust and maintainable codebase.
### 👩‍💻Key Features
#### Backend Features:
- **RESTful API:** Developed using Spring Boot to handle requests and provide data to the frontend.
- **CRUD Operations:** Endpoints to create, read, update, and delete aviation-related data.
- **JWT Authentication:** Secured endpoints with JWT for user login and access control.
- **Database Integration:** PostgreSQL is used to store all relevant data. Neon DB is utilized for cloud storage.
- **Data Mapping:** Model Mapper helps convert data between the layers (entities, DTOs, etc.).
#### Frontend Features:
- **State Management with Redux:** Using Redux and Redux Toolkit to manage the state of the application and ensure predictable behavior across components.
- **Form Handling:** Using Formik and Yup for handling complex form inputs, validations, and error management.
- **Routing:** Seamless navigation across different views with React Router DOM.
- **API Integration:** Axios handles all HTTP requests, with token-based authentication using Axios Token Interceptor and JWT Decode.
- **Responsive Design:** Bootstrap helps in making the application responsive across various devices.
- **User Notifications:** React Toastify provides real-time feedback for users in the form of toast notifications.
#### Backend Integration:
The integration between the frontend and backend in the Apron101Frontend project is designed to ensure seamless communication and data flow. The backend, built using Java Spring Boot, provides a robust and scalable API that the frontend, developed with React and TypeScript, interacts with. Key aspects of this integration include:
- **RESTful API:** The backend exposes a set of RESTful endpoints, enabling the frontend to perform CRUD operations efficiently. Each endpoint is designed to handle specific tasks, ensuring a clean separation of concerns.
- **Asynchronous Communication:** To enhance user experience and performance, asynchronous requests are employed, allowing the frontend to fetch and update data without blocking the user interface.
- **Data Serialization:** JSON is used for data serialization, ensuring that data is transferred in a lightweight and human-readable format. The backend utilizes Jackson for JSON parsing, facilitating smooth data conversion between the frontend and backend.
- **Authentication and Security:** Security measures are implemented to protect data and ensure secure communication between the frontend and backend. This includes token-based authentication to verify user identities and safeguard sensitive information.
- **Error Handling:** Both the frontend and backend are equipped with comprehensive error handling mechanisms. The backend returns standardized error codes and messages, which the frontend interprets and displays appropriately to the user, enhancing usability and reliability.
This well-structured integration ensures that the frontend and backend operate cohesively, providing a smooth and responsive experience for the users.
#### Responsive Design: 
The Apron101 project incorporates a responsive design approach to ensure optimal usability across a variety of devices and screen sizes. This is achieved through a combination of Bootstrap and custom CSS.
- **Bootstrap Framework:** The project leverages Bootstrap's grid system and responsive utilities to quickly and efficiently build layouts that adapt to different screen sizes. This includes using pre-defined classes for responsive spacing, alignment, and component behavior, reducing the need for extensive custom CSS for layout management.
- **Custom CSS:** While Bootstrap provides a solid foundation for responsiveness, custom CSS is used to fine-tune the design and address specific styling needs. This includes:
  - **Media Queries:** Custom media queries are written to handle design tweaks for specific breakpoints, ensuring that each page maintains a consistent and user-friendly layout across all devices.
  - **Modular CSS:** Styles are modularized to maintain clarity and prevent conflicts, focusing on encapsulating component styles and promoting reusability.
  - **Custom Components:** Unique UI components are styled using core CSS to align with the project's specific design language, complementing Bootstrap's default styles.
By integrating Bootstrap and custom CSS, the project achieves a balance between rapid development and tailored design, delivering a cohesive and responsive user experience across desktops, tablets, and mobile devices.

























































