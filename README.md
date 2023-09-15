# E-Commerce Back End

Welcome to the E-Commerce Back End project! In this project, we have developed a fully functional back end for an e-commerce website using the latest technologies and industry best practices. This back end allows your company to compete effectively in the e-commerce market.

## Table of Contents

- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [Database Models](#database-models)
- [API Routes](#api-routes)
- [Database Seeding](#database-seeding)
- [Getting Started](#getting-started)

## Introduction

E-commerce is a booming industry, and having a robust back end is essential for success. This project provides a back end solution for an e-commerce website, allowing you to manage categories, products, and tags. You can create, read, update, and delete data in your database through well-defined API routes.

## Technologies Used

This project leverages the following technologies and packages:

- **Express.js**: A popular Node.js framework for building web applications and APIs.
- **Sequelize**: An ORM (Object-Relational Mapping) library for Node.js that simplifies database interactions.
- **MySQL2**: A Node.js driver for MySQL, used to connect to the database.
- **dotenv**: A package for storing sensitive data like database credentials as environment variables.
- **Insomnia**: A powerful API testing tool used to test the API routes.
- **MySQL**: The database management system used to store data.

## Setup

To set up this project locally, follow these steps:

1. Clone the repository to your local machine.

```bash
git clone github.com/musicchef/ORM_E-Commerce_BackEnd
```

2. Install project dependencies using npm.

```bash
npm install
```

3. Create a .env file in the root directory and add your MYSQL configuration.

```bash
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=your_database_name
```

## Database Models

This project defines four database models:

Category: Represents product categories.

id: Auto-incremented integer (primary key).
category_name: String (no null values).
Product: Represents products.

id: Auto-incremented integer (primary key).
product_name: String (no null values).
price: Decimal (no null values, must be a decimal).
stock: Integer (no null values, default 10, must be numeric).
category_id: Integer (foreign key referencing Category).
Tag: Represents product tags.

id: Auto-incremented integer (primary key).
tag_name: String.
ProductTag: Represents the many-to-many relationship between products and tags.

id: Auto-incremented integer (primary key).
product_id: Integer (foreign key referencing Product).
tag_id: Integer (foreign key referencing Tag).

## API Routes
Implemented RESTful CRUD (Create, Read, Update, Delete) operations for categories, products, and tags. The routes are defined in the following files:

product-routes.js
tag-routes.js
category-routes.js
These routes allow you to manage your e-commerce data efficiently.

## Database Seeding
```bash
npm run seed
```

## Getting Started
```bash
npm start
```

