# Movie API

This is a simple Movie API built with Go, using the Gorilla Mux router. The API allows you to perform CRUD operations (Create, Read, Update, Delete) on a collection of movies.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Testing the API](#testing-the-api)

## Features

- Get a list of all movies
- Get a single movie by ID
- Create a new movie
- Update an existing movie
- Delete a movie

## Installation

• Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   go run main.go
   ```

## Testing the API

 Make a POST request to Create a movie:

   ```bash
   curl -X POST http://localhost:8000/movies \
   -H "Content-Type: application/json" \
   -d '{
       "isbn": "789012",
       "title": "Movie Three",
       "director": {
           "firstname": "Jane",
           "lastname": "Doe"
       }
   }'
   ```
 Read Update Delete Movies:
   •Get all movies
   ```bash
   curl -X GET http://localhost:8000/movies
   ```
   •Get movie by id:
   ```bash
   curl -X GET http://localhost:8000/movies/1
   ```
   •Update Movie:
   ```bash
   curl -X PUT http://localhost:8000/movies/1 \
   -H "Content-Type: application/json" \
   -d '{
       "isbn": "123789",
       "title": "Updated Movie One",
       "director": {
           "firstname": "Rodney",
           "lastname": "Doe"
       }
   }'
   ```
   •Delete movie:
   ```bash
   curl -X DELETE http://localhost:8000/movies/1 \\
   ```
   
