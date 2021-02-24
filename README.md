# An Employee Rest Service

An implementation of an Employee REST service using nodejs and expressjs with a few endpoints to login employees, add new employees, get all employees, get a specific employee. update employees details and lastly, delete employees. 

---
## Requirements and Dependencies

For development, you will only need Node.js and a node global package, express, and a few dependencies installed in your environement to properly run this service.

### Web Server
- #### Download a local web server
  
  Download a local web server like xampp to create a local server.You can download xampp [here](https://www.apachefriends.org/download.html).
   Create a database with a name of your choosing and run
  
 CREATE DATABASE node_mysql_crud_db;

CREATE  TABLE IF NOT EXISTS `employees` (
  `id` BIGINT UNSIGNED AUTO_INCREMENT,
  `first_name` VARCHAR(255) NOT NULL,
  `last_name` VARCHAR(255) NOT NULL,
  `email` VARCHAR(255) NOT NULL,
  `phone` VARCHAR(50) NOT NULL,
  `organization` VARCHAR(255) NOT NULL,
  `designation` VARCHAR(100) NOT NULL,
  `salary` DECIMAL(11,2) UNSIGNED DEFAULT 0.00,
  `status` TINYINT UNSIGNED DEFAULT 0,
  `is_deleted` TINYINT UNSIGNED DEFAULT 0,
  PRIMARY KEY (`id`))
ENGINE = InnoDB;


### Node
- #### Node installation on Windows

  Just go on [official Node.js website](https://nodejs.org/) and download the installer.
Also, be sure to have `git` available in your PATH, `npm` might need it (You can find git [here](https://git-scm.com/)).


- #### Other Operating Systems
  You can find more information about the installation on the [official Node.js website](https://nodejs.org/) and the [official NPM website](https://npmjs.org/).

If the installation was successful, you should be able to run the following command.

    $ node --version
    v15.7.0

    $ npm --version
    6.1.0

## Install

    $ mkdir NODEMYSQLCRUDAPI
    $ cd NODEMYSQLCRUDAPI
    
To install all the dependencies(express, body-parser & mysql) in the `package.json` file, run.
    
    $ npm install

You can then run the service with the following command 
    
    $ nodemon index.js
####    
NOTE: The service is running in port `5000` and can easily be changed by changing port value in `index.js` file. The `node_module` file should also be added to the `.gitignore` file
