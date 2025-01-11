
# URL Shortener

A simple and efficient URL shortening service that allows users to shorten long URLs for easier sharing and tracking.

## Features

- Shorten long URLs to compact, shareable links.
- Redirect users from shortened links to original URLs.
- Easy-to-use web interface.
- Built using **Node.js**, **Express.js**
- RESTful API support for programmatic URL shortening.


## Installation

Follow these steps to get the project running on your local machine.

### Prerequisites

- [Node.js](https://nodejs.org/) installed.
- [MongoDB](https://www.mongodb.com/) running locally or on a cloud server.

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/sandeep1404-praj/URL_Shortner.git
   cd URL_Shortner
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables:
   Create a `.env` file in the root directory and add the following:
   ```env
   PORT=3000
   MONGO_URI=your_mongodb_connection_string
   BASE_URL=http://localhost:3000
   ```

4. Start the application:
   ```bash
   npm start
   ```

5. Open your browser and navigate to `http://localhost:3001`.

## Usage

### Shorten a URL
1. Enter a long URL into the input field on the homepage.
2. Click "Shorten" to generate a shortened link.

### API Endpoints
#### Shorten a URL
- **POST** `/api/url/shorten`
- Request Body:
  ```json
  {
    "longUrl": "https://example.com/very/long/url"
  }
  ```
- Response:
  ```json
  {
    "shortUrl": "http://localhost:3001/abc123"
  }
  ```

#### Redirect to Original URL
- **GET** `/:shortCode`
- Example: `http://localhost:3000/abc123` will redirect to the original URL.

## Folder Structure

```
URL_Shortner/
├── public/         # Static files (CSS, JS, images)
├── routes/         # API and view routes
├── models/         # Database schemas
├── views/          # HTML templates (if applicable)
├── server.js       # Main application file
├── package.json    # Dependencies and scripts
└── README.md       # Project documentation
```

## Technologies Used

- **Frontend**: HTML, CSS
- **Backend**: Node.js, Express.js

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for review.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

