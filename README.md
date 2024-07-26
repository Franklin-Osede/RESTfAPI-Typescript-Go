# User Management API

A Comprehensive User Management System

## Introduction

Welcome to the User Management API! This project provides a robust backend service developed using Go, with a PostgreSQL database, and a Next.js frontend. The application supports creating, retrieving, updating, and deleting users, leveraging Axios for HTTP requests and TypeScript for type safety. Both the backend and frontend are containerized using Docker for easy deployment and scalability.

## Why?

The motivation behind this project is to create an efficient and scalable user management system. This API aims to solve common problems associated with managing user data, such as secure data storage, efficient data retrieval, and seamless integration with frontend applications.

## What does the program do?

The User Management API allows you to:
- Create new users
- Retrieve user information by ID
- Update existing user details
- Delete users from the database

## How to Install

### Prerequisites
- Docker
- Docker Compose
- PostgreSQL (optional, if not using Docker for the database)

### Setting Up the Project

1. **Clone the repository:**
    
    git clone https://github.com/your-username/user-management-api.git
    cd user-management-api
    

2. **Dockerize the application:**

   The project includes `Dockerfile` and `docker-compose.yml` files to facilitate the containerization of both the backend and frontend.

   **Backend Dockerfile:**
   This file defines the Docker image for the Go backend, including all dependencies and setup instructions.
   
   # Backend Dockerfile
   
   FROM golang:1.16-alpine
   WORKDIR /app
   COPY . .
   RUN go mod tidy
   RUN go build -o main .
   EXPOSE 8080
   CMD ["./main"]
