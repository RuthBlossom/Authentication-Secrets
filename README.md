# Express Authentication App

This is a web application built using Express.js for user authentication. Users can register, login, and submit their secrets anonymously. Authentication is implemented using Passport.js with both local strategy (username and password) and Google OAuth 2.0 strategy.

## Features
- **User Registration**: Allows users to register with a username and password.
- **User Login**: Enables registered users to log in to access their secrets.
- **Google OAuth 2.0 Authentication**: Provides an option for users to authenticate using their Google accounts.
- **Anonymous Secrets Submission**: Allows authenticated users to submit their secrets anonymously.
- **Secrets Display**: Displays submitted secrets from all users.

## Prerequisites
- Node.js installed on your system.
- npm (Node Package Manager) for installing dependencies.
- MongoDB installed and running on your local machine.

## Installation
1. Clone this repository to your local machine:
   ```
   git clone https://github.com/your-username/express-authentication.git
   ```
2. Navigate to the project directory:
   ```
   cd express-authentication
   ```
3. Install dependencies using npm:
   ```
   npm install
   ```

## Configuration
1. Create a `.env` file in the root directory and add the following variables:
   ```
   CLIENT_ID=<your_google_client_id>
   CLIENT_SECRET=<your_google_client_secret>
   ```
   Replace `<your_google_client_id>` and `<your_google_client_secret>` with your actual Google OAuth 2.0 client ID and client secret obtained from the Google Developer Console.

## Usage
1. Start the MongoDB server:
   ```
   mongod
   ```
2. Start the Express server:
   ```
   node app.js
   ```
3. Access the application in your web browser at `http://localhost:3000`.

## Endpoints
- **GET /auth/google**: Initiates Google OAuth 2.0 authentication process.
- **GET /auth/google/secrets**: Callback URL for handling Google authentication.
- **GET /login**: Displays the login form.
- **POST /login**: Handles user login requests.
- **GET /register**: Displays the registration form.
- **POST /register**: Handles user registration requests.
- **GET /submit**: Displays the form for submitting secrets.
- **POST /submit**: Handles secret submission requests.
- **GET /secrets**: Displays all submitted secrets.
- **GET /logout**: Logs out the current user.

## Dependencies
- express
- body-parser
- ejs
- mongoose
- express-session
- passport
- passport-local-mongoose
- passport-google-oauth20
- mongoose-findorcreate
- dotenv

