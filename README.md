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

Response:
{
  "id": 1,
  "title": "Inception",
  "release_date": "2010-07-16",
  "rating": 8.8
}
