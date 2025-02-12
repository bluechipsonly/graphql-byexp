# Django GraphQL CRUD API

## Overview
This project is a fully functional GraphQL-based CRUD (Create, Read, Update, Delete) application built using Django and GraphQL. It provides an API Endpoint for managing simulated restaurant data with support for queries and mutations. Designed for efficient and structured data handling, this application enables seamless interaction through GraphQL endpoints.

## Features
- **GraphQL API**: Implements GraphQL using `graphene-django`, allowing efficient data retrieval and manipulation.
- **CRUD Operations**: Create, Read, Update, and Delete restaurant records.
- **GraphiQL Interface**: Enables interactive API testing via `/graphql`.
- **Error Handling**: Provides meaningful messages for missing or invalid data.
- **Query Filtering**: Allows filtering restaurants by `id` or `name`.
- **Modular Design**: Uses Django’s model-based approach for extendability and maintainability.


## Technologies Used
- **Django** – Web framework for backend development.
- **Graphene-Django** – GraphQL API integration.
- **SQLite** – Default database (can be switched to PostgreSQL or MySQL).
- **Python 3.8+** – Core language for the project.

## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/iburr/graphql-byexp.git
cd graphql-byexp
