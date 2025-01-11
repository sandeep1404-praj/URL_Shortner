
URL Shortener
A simple and efficient URL shortening service that allows users to shorten long URLs for easier sharing and tracking.

Features
Shorten long URLs to compact, shareable links.
Redirect users from shortened links to original URLs.
Easy-to-use web interface.
Built using Node.js, Express.js, and MongoDB.
RESTful API support for programmatic URL shortening.
Demo
Check out the live demo here.

Installation
Follow these steps to get the project running on your local machine.

Prerequisites
Node.js installed.
MongoDB running locally or on a cloud server.
Steps
Clone the repository:

bash
Copy code
git clone https://github.com/sandeep1404-praj/URL_Shortner.git
cd URL_Shortner
Install dependencies:

bash
Copy code
npm install
Configure environment variables: Create a .env file in the root directory and add the following:

env
Copy code
PORT=3001
MONGO_URI=your_mongodb_connection_string
BASE_URL=http://localhost:3001
Start the application:

bash
Copy code
npm start
Open your browser and navigate to http://localhost:3001.

Usage
Shorten a URL
Enter a long URL into the input field on the homepage.
Click "Shorten" to generate a shortened link.
API Endpoints
Shorten a URL
POST /api/url/shorten
Request Body:
json
Copy code
{
  "longUrl": "https://example.com/very/long/url"
}
Response:
json
Copy code
{
  "shortUrl": "http://localhost:3001/abc123"
}
Redirect to Original URL
GET /:shortCode
Example: http://localhost:3000/abc123 will redirect to the original URL.
Folder Structure
bash
Copy code
URL_Shortner/
├── public/         # Static files (CSS, JS, images)
├── routes/         # API and view routes
├── models/         # Database schemas
├── views/          # HTML templates (if applicable)
├── .env            # Environment variables
├── server.js       # Main application file
├── package.json    # Dependencies and scripts
└── README.md       # Project documentation
Technologies Used
Frontend: HTML, CSS, Bootstrap
Backend: Node.js, Express.js
Database: MongoDB
Contributing
Contributions are welcome! Please fork the repository and submit a pull request for review.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For any questions or suggestions, feel free to reach out:
