# Rust-JWT-Warp Implementation

This project is an example of authorization and authentication using JSON web tokens in Rust using the warp framework
By default the project has two role-based users, one is the admin and the other one is the user.

## Cloning the repository

run the command

    git clone https://github.com/meetjn/Rust-Authenticaion-server

## Running the project

Run this command on your terminal, it will successfully create a hash-based token for you

    cargo run

    curl http://localhost:8000/login -d '{"email": "user@userland.com", "pw": "1234"}' -H 'Content-Type: application/json'

    curl http://localhost:8000/user -H 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIxIiwicm9sZSI6IlVzZXIiLCJleHAiOjE2MDMxMzQwODl9.dWnt5vfcGdwypEQUr3bLMrZYfdyxj3v6-io6VREWHXebMUCKBddf9xGcz4vHrCXruzx42zrS3Kygiqw3xV8W-A' -H 'Content-Type: application/json'

## Testing Admin Endpoint

        curl http://localhost:8000/login -d '{"email": "admin@adminaty.com", "pw": "4321"}' -H 'Content-Type: application/json'

        curl http://localhost:8000/user -H 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIxIiwicm9sZSI6IlVzZXIiLCJleHAiOjE2MDMxMzQwODl9.dWnt5vfcGdwypEQUr3bLMrZYfdyxj3v6-io6VREWHXebMUCKBddf9xGcz4vHrCXruzx42zrS3Kygiqw3xV8W-A' -H 'Content-Type: application/json'

## Testing the User Endpoint

        curl http://localhost:8000/login -d '{"email": "admin@adminaty.com", "pw": "4321"}' -H 'Content-Type: application/json'
