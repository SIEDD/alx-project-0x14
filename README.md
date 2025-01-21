# Main Project Title
This is the top-level heading. Use `#` for the largest heading.

## API Overview
This is a second-level heading. Use `##` for subheadings.

The MoviesDatabase API allows developers to search for movies, retrieve detailed information, and access user reviews. It supports various endpoints to fetch data based on genre, popularity, and user ratings.

## Version
This is another second-level heading.

The current version of the API is `v1.2.0`.

## Available Endpoints
Below is a list of available endpoints provided by the API:

- `/movies/popular` - Retrieve a list of popular movies.
- `/movies/{id}` - Get details about a specific movie.
- `/genres` - Fetch a list of available genres.

## Request and Response Format
Requests are made in the following format:

```json
GET /movies/{id}

Headers:
{
  "Authorization": "Bearer YOUR_API_KEY"
}

## Authentication
To use the MoviesDatabase API, you need an API key. Follow these steps to authenticate your requests:

1. Register for an API key on the MoviesDatabase platform.
2. Include the API key in the `Authorization` header for all requests.
```

### Example Header


Response:
{
  "id": 1,
  "title": "Inception",
  "release_date": "2010-07-16",
  "rating": 8.8
}

## Error Handling
The MoviesDatabase API provides structured error responses to help identify and resolve issues with requests. Common errors include:

- **400 Bad Request**: The request was malformed or missing required parameters.
- **401 Unauthorized**: The API key is invalid or missing.
- **403 Forbidden**: The API key does not have permission to access the requested resource.
- **404 Not Found**: The requested resource does not exist.
- **429 Too Many Requests**: Rate limit exceeded; wait before making more requests.
- **500 Internal Server Error**: An unexpected error occurred on the server.

### Example Error Response
```json
{
  "status_code": 401,
  "status_message": "Invalid API key: You must be granted a valid key.",
  "success": false
}

## Usage Limits
The MoviesDatabase API enforces rate limits to ensure fair usage among all users. These limits vary based on the subscription tier:

- **Free Tier**: Allows up to 100 requests per hour.
- **Pro Tier**: Allows up to 10,000 requests per hour.
```

### Monitoring Usage
- Most API platforms provide a usage dashboard. Use it to monitor your request counts.
- Consider implementing logging in your application to track API requests and responses.

### What Happens When You Exceed Limits?
- If the rate limit is exceeded, you will receive a `429 Too Many Requests` response.
- The response headers often include information about when you can resume making requests.

```json
{
  "status_code": 429,
  "status_message": "Rate limit exceeded. Try again in 60 seconds.",
  "success": false
}

