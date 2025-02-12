# Django GraphQL CRUD API

## Overview
This project is a fully functional GraphQL-based CRUD (Create, Read, Update, Delete) application built using Django and GraphQL. It provides an API Endpoint for managing simulated restaurant data with support for queries and mutations. Designed for efficient and structured data handling, this application enables seamless interaction through GraphQL endpoints.

## Features
- **GraphQL API**: Implements GraphQL using `graphene-django`, allowing for efficient data retrieval and manipulation.
- **CRUD Operations**: Create, Read, Update, and Delete restaurant records.
- **GraphiQL Interface**: Enables interactive API testing via `/graphql`.
- **Error Handling**: Provides meaningful messages for missing or invalid data.
- **Design**: Uses Django’s model-based approach for extendability and maintainability.


## Technologies Used
- **Django** – Web framework for backend development.
- **Graphene-Django** – GraphQL API integration.
- **SQLite** – Default database (can be switched to PostgreSQL or MySQL).
  - **Updating database:** You can update the database in settings.py
- **Python 3.12** – Core language for the project.

## Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/iburr/graphql-byexp.git
ls -l (to verify files are there)
cd graphql-byexp
```
## Setting up a Virtual enviorment
- I used uv to work with and manage my depedencies, versions, and files for this project
- Alternatively you can use pip or python install depending on what you need, whether it is version control or executables
- If you rather use uv (which I recommend anyways click the link below)
- **uv Documentation:** [https://docs.astral.sh/uv/](https://docs.astral.sh/uv/)

```bash
uv venv .venv
source .venv/bin/activate

# May already be setup automatically upon git clone
```
## Installing dependencies
```bash
uv add Django
uv add graphene-django

# May already be setup automatically upon git clone
```

## Applying migrations
```bash
python manage.py makemigrations
python manage.py migrate
```
## Start the Server
```bash
python manage.py runserver
```
- Visit the GraphQL API at:
  - http://127.0.0.1:8000/
  - /graphql (main GUI)
  - /admin (Optional GUI (uses Djangos) you will have to create a superuser to be able to access the url path)
  - Refer to: https://docs.graphene-python.org/projects/django/en/latest/

### GraphQL Queries and Mutations

## Fetch all Restaurants
```graphql
{
  restaurants {
    id
    name
    address
  }
}
```
## Fetch a Restaurant by ID
```graphql
{
  restaurants(id: 1) {
    id
    name
    address
  }
}
```

## Creating a Restaurant
```graphql
mutation {
  createRestaurant(name: "Pizza Palace", address: "123 Main St") {
    success
    message
    restaurant {
      id
      name
      address
    }
  }
}
```
## Updating Restaurant information
```graphql
id values go by index 0,1,2,3,4,5 etc.

mutation {
  updateRestaurant(id: 1, name: "Updated Name", address: "New Address") {
    success
    message
    restaurant {
      id
      name
      address
    }
  }
}
```
## Deleting Restaurant
```graphql
mutation {
  deleteRestaurant(id: 1) {
    success
    message
  }
}
```
### Refrences & Research 
- https://docs.djangoproject.com/en/4.0/topics/install/#how-to-install-django
- https://discuss.python.org/t/what-are-the-differences-between-str-and-repr-in-class-methods/44142/4
- https://docs.graphene-python.org/projects/django/en/latest/
- https://docs.graphene-python.org/projects/django/en/latest/authorization/
- https://docs.astral.sh/uv/
- https://graphql.org/learn/schema/

 






