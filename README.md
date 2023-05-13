# E-commerce Back End Starter Code

This is a backend application for an eCommerce website, built using Node.js, Express.js, and Sequelize ORM. The application provides RESTful APIs for managing products, categories, and tags.

## Installation
1. Clone the repository to your local machine : 
```bash
git clone https://github.com/your-username/e-commerce-back-end-starter-code.git
```

2. Install the required dependencies by running the following command:
``` bash
npm i
```

3. Create a `.env` file in the root directory of the project, and add the following environment variables:

```.env
DB_NAME = ecommerce_db
DB_USER = YOUR_DB_USER_NAME
DB_PW = YOUR_DB_PASSWORD
```
Replace `YOUR_DB_PASSWORD` with the password and `DB_USER` with the username for your MySQL database.


 4. Create the MySQL database by running the following command: 
 ```bash
    mysql -u root -p
 ```

Enter your MySQL password, and then run the following SQL command:
```sql
CREATE DATABASE ecommerce_db;
```
5. Seed the database with some sample data by running the following command:
```bash
npm run seed
```
This will populate the database with some sample products, categories, and tags.

***

## Usage
To start the server, run the following command:
```bash
npm start
``` 
This will start the server on port 3001. You can then use a REST client such as [Insomnia](https://insomnia.rest/products/insomnia) to interact with the APIs.

## API Endpoints

The following API endpoints are available:
### Product Routes
- Returns a list of all products, including their associated categories and tags.

    ```bash
    GET /api/products
    ```
- Returns a single product by ID, including its associated category and tags.

    ```bash
    GET /api/products/:id
    ```
- Creates a new product.

    ```bash
    POST /api/products
    ```

    Request body example:
    ```json
    {
	"product_name": "Basketball",
	"price": 200.00,
	"stock": 3,
	"tagIds": [1, 2, 3, 4]
    }
    ```
- Updates a product by ID.

    ```bash
    PUT /api/products/:id
    ```
- Deletes a product by ID.

    ```bash
    DELETE /api/products/:id
    ```

### Category Routes
- Returns a list of all categories, including their associated products.

    ```bash
    GET /api/categories
    ```
- Returns a single category by ID, including its associated products.

    ```bash
    GET /api/categories/:id
    ```
- Creates a new category.

    ```bash
    POST /api/categories
    ```
    Request body example:
    ```json
    {
        "category_name": "New Category"
    }
    ```
- Updates a category by ID.

    ```bash
    PUT /api/categories/:id
    ```
- Deletes a category by ID.

    ```bash
    DELETE /api/categories/:id
    ```
### Tag Routes
- Returns a list of all tags, including their associated products.

    ```bash
    GET /api/tags
    ```
- Returns a single tag by ID, including its associated products.

    ```bash
    GET /api/tags/:id
    ```
- Creates a new tag.

    ```bash
    POST /api/tags
    ```
    Request body example:
    ```json
    {
        "tag_name": "New Tag"
    }
    ```
- Updates a tag by ID.

    ```bash
    PUT /api/tags/:id
    ```

- Deletes a tag by ID.

    ```bash
    DELETE /api/tags/:id
    ```

## Demo
![Demo Video]("demo.webm")

## Credits
- [express](https://www.npmjs.com/package/express): Fast, unopinionated, minimalist web framework for Node.js
- [mysql2](https://www.npmjs.com/package/mysql2): MySQL client for Node.js with focus on performance.
- [sequelize](https://www.npmjs.com/package/sequelize): Promise-based Node.js ORM for Postgres, MySQL, MariaDB, SQLite and Microsoft SQL Server.
- [dotenv](https://www.npmjs.com/package/dotenv): Zero-dependency module that loads environment variables from a .env file into process.env.
- [nodemon](https://www.npmjs.com/package/nodemon): A utility that monitors for any changes in the source and automatically restarts your server.