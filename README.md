# Timestamp Microservice

## Project Overview
The Timestamp Microservice is a simple web API that converts a given date into both Unix timestamp and UTC string formats. It serves as a useful example of how backend development works using Express.js and how APIs can interact with time-related data.

This project is part of the FreeCodeCamp Back-End Development and APIs certification, aimed at building a functional and efficient microservice API.

## Features
- **Date Conversion**: Converts a date string to a Unix timestamp (milliseconds since January 1, 1970).
- **Automatic UTC Format**: Converts the Unix timestamp into a human-readable UTC string.
- **Error Handling**: Provides meaningful error messages when an invalid date is provided.
- **Current Time**: Returns the current Unix timestamp and UTC string when no date is provided.

## Live Demo
You can access a live version of the project at:  
[Timestamp Microservice - Live Demo](https://freecodecam-boilerplate-6errsjx2jie.ws-us117.gitpod.io/)

## API Endpoints

### 1. `/api/:date?`
- **Method**: `GET`
- **Description**: Converts a provided date to both Unix timestamp and UTC format.
- **Parameters**:
  - `date` (optional): A date in either **YYYY-MM-DD**, **Unix timestamp**, or a natural language date (e.g., "December 25, 2015").
- **Response**:
  - **Success**: `{ "unix": <timestamp>, "utc": "<UTC string>" }`
  - **Error**: `{ "error": "Invalid Date" }`

#### Example:
- Request: `/api/2015-12-25`
- Response:
  ```json
  {
    "unix": 1451001600000,
    "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
  }
  ```

### 2. `/api`
- **Method**: `GET`
- **Description**: Returns the current date and time in both Unix timestamp and UTC format when no date is provided.
- **Response**:
  ```json
  {
    "unix": <current timestamp>,
    "utc": "<current UTC string>"
  }
  ```

## Getting Started

### Prerequisites
To run this project locally, make sure you have:
- **Node.js** installed (v14 or higher).
- **npm** (Node Package Manager).

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/timestamp-microservice.git
   ```

2. Navigate into the project directory:
   ```bash
   cd timestamp-microservice
   ```

3. Install the required dependencies:
   ```bash
   npm install
   ```

### Running the Application

To start the server, run:

```bash
npm start
```

The application will run locally on [http://localhost:3000](http://localhost:3000). You can access the API endpoints by navigating to:

- `http://localhost:3000/api/<date>`
- `http://localhost:3000/api`

## Technologies Used
- **Node.js**: JavaScript runtime to run the backend server.
- **Express.js**: Web framework for Node.js to simplify server creation.
- **CORS**: Cross-Origin Resource Sharing for handling requests from external origins.
- **Date API**: JavaScript's `Date()` API to handle date manipulations.

## Project Structure

```
/timestamp-microservice
│
├── /public
│   └── (static files)
│
├── /views
│   └── index.html  # HTML file that serves as the front end
│
├── /node_modules
│   └── (installed dependencies)
│
├── index.js  # Main server file
├── package.json  # Project metadata and dependencies
└── README.md  # Project documentation
```

## Contributing

Feel free to fork this project, make improvements, and create a pull request. Any contribution is welcome to enhance this project, including code improvements, bug fixes, or additional features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with ❤️ by [Your Name](https://github.com/<your-username>)
```

### Explanation:
- **Project Overview**: A brief description of the project’s functionality.
- **Features**: Key features and functionalities of the project.
- **Live Demo**: A link to access the live version of the project.
- **API Endpoints**: Describes each endpoint and how to use them with example responses.
- **Getting Started**: Instructions on how to set up and run the project locally.
- **Technologies Used**: A list of key technologies and tools used in the project.
- **Project Structure**: Describes the file structure for easy navigation.
- **Contributing**: An invitation for others to contribute to the project.
- **License**: Licensing information to give credit to contributors and make the project open for use.
