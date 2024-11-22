# Full Stack Interactive Quiz Application

## Project Overview
This project is a comprehensive full-stack interactive quiz application designed to enhance your development skills using React for the front-end, Spring Boot for the back-end, and MySQL for the database. The application allows users to take quizzes, view scores, and review answers. It also includes an admin panel for adding and managing quiz questions.

## Features
- User registration and authentication
- Quiz creation and management by admin
- Taking quizzes and viewing scores
- Reviewing correct and incorrect answers
- Secure handling of user data and authentication

## Technologies Used
- **Frontend**: React
- **Backend**: Spring Boot
- **Database**: MySQL
- **Others**: Spring Security, JWT

## Setup and Installation

### Prerequisites
- Node.js and npm
- Java JDK (version 11 or higher)
- MySQL Server

### Frontend Setup
1. Clone the repository:
    ```sh
    git clone https://github.com/Soumyaatanna/Quiz.git
    cd Quiz
    ```

2. Navigate to the frontend directory and install dependencies:
    ```sh
    cd frontend
    npm install
    ```

3. Start the React development server:
    ```sh
    npm start
    ```

### Backend Setup
1. Navigate to the backend directory and open it in your IDE (e.g., IntelliJ IDEA):
    ```sh
    cd backend
    ```

2. Configure the `application.properties` file with your MySQL database details:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/quizdb
    spring.datasource.username=root
    spring.datasource.password=your_password
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
    ```

3. Build and run the Spring Boot application:
    ```sh
    mvn clean install
    mvn spring-boot:run
    ```

### Database Setup
1. Create the `quizdb` database in MySQL:
    ```sql
    CREATE DATABASE quizdb;
    ```
   The database schema will be automatically created by the Spring Boot application based on JPA entities.

## API Endpoints

### User Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/signin` - Authenticate a user

### Quiz Management
- `POST /api/quizzes` - Create a new quiz (admin only)
- `GET /api/quizzes` - Retrieve all quizzes
- `GET /api/quizzes/{id}` - Retrieve a specific quiz by ID
- `PUT /api/quizzes/{id}` - Update a quiz (admin only)
- `DELETE /api/quizzes/{id}` - Delete a quiz (admin only)

### Quiz Taking
- `POST /api/quizzes/{id}/take` - Submit quiz answers and calculate score
- `GET /api/quizzes/{id}/results` - Retrieve quiz results for a user

## Security
- User authentication and authorization are implemented using Spring Security.
- Passwords are securely hashed and stored in the database.

## Testing and Debugging
- Thoroughly tested both frontend and backend functionalities.
- Used browser developer tools and backend logs for debugging.

## Contributing
- Feel free to open issues or submit pull requests for improvements and new features.

## License
This project is licensed under the MIT License.

## Contact
For any questions or support, please contact Soumya Tanna.
