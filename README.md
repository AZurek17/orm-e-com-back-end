# orm-e-com-back-end ![GitHub License Badge](https://img.shields.io/badge/License-MIT-yellow)

[Link to Walkthrough Video](https://watch.screencastify.com/v/GkLn6BAAw9DhN8k4BYd0)

![orm-e-com-back-end](./images/Screenshot.png)

## Technology Used:

 * node - https://nodejs.org/en/about
 * npm - https://www.npmjs.com/
 * mysql2 - https://www.npmjs.com/package/mysql2
 * sequelize - https://sequelize.org/
 * express - https://expressjs.com/
 * dotenv - https://www.npmjs.com/package/dotenv

 ## Description

  This application is a backend for a e-commerce website which uses the latest technologies listed above. 
  which allows for an API GET, POST, PUT, and DELETE request for each models: Category, Products, Tag.

 ## Table of Contents
  
   * [Installation](#installation)
   * [Usage](#usage)
   * [License](#license)
   * [Badges](#badges)
   * [Tests](#tests)
   * [Contributing](#contributing)
   * [Credits](#credits)

## Installation

This application requires dotenv, express, , mysql2, and sequelize.  
* To install all dependences, run: npm install
* Create the database in MYSQL using the schema.sql.
* To load the seeds into the database, run: npm run seed 
* To start the server, run: node server.js

## Usage
This application uses dotenv which allows you to store your login information in an .env file. By creating a config folder with a connection.js inside, and an .env file in the root folder of the application. Remeber to add .env into your .gitignore file so you dont upload you private information into your repository for others to see. Below is a snippet of code:
  
.env

    DB_NAME='ecommerce_db'
    DB_USER='<enter username here>'
    DB_PW='<enter password here>'

connection.js  

    const sequelize = process.env.JAWSDB_URL
      ? new Sequelize(process.env.JAWSDB_URL)
      : new Sequelize(process.env.DB_NAME, process.env.DB_USER, process.env.DB_PW, {
          host: 'localhost',
          dialect: 'mysql',
          dialectOptions: {
            decimalNumbers: true,
          },
        });

After creating routes, you can create API GET, POST, PUT, and DELETE requests with using Using Insomnia Core.

below is a code snippet:

Get Request:

    router.get('/', (req, res) => {
     associated Products
     Category.findAll().the((categoryData) => {
       res.json(categoryData);
    });
    });

Please watch the walkthrough video (see link above), testing each route request created for each model created.


## License

 This project is licensed with MIT license

 Link to License - [Website to MIT License]((https://opensource.org/license/mit))

 ## Badges

 ![GitHub License Badge](https://img.shields.io/badge/License-MIT-yellow)

 ## Tests
 
 This application tested the writen code using Insomnia Core application

 ## Contributing

 Contact me if you interested in contributing:

 Check out my [github](https://github.com/AZurek17) page or send me a [email](mailto:andyzurek@gmail.com)

 ## Credits
 * Tutoring Session
 * ChatGPT
 * StudyGroup

 &copy;2023, Written by Andy Zurek