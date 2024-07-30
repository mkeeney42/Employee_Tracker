Employee Tracker
Description
Employee Tracker is a command-line application designed to manage a company's employee database. It allows users to interact with the database and perform various operations such as viewing departments, roles, and employees, as well as adding new departments, roles, and employees. The application is built using Node.js, Inquirer, and PostgreSQL.

User Story
css
Copy code
AS A business owner
I WANT to be able to view and manage the departments, roles, and employees in my company
SO THAT I can organize and plan my business
Table of Contents
Installation
Usage
Features
Database Schema
License
Contributing
Questions
Installation
Clone the repository:

bash
Copy code
git clone <repository-url>
Navigate to the project directory:

bash
Copy code
cd employee-tracker
Install dependencies:

bash
Copy code
npm install
Install the required PostgreSQL package:

bash
Copy code
npm install pg
Set up the PostgreSQL database:

Create a PostgreSQL database.
Create the necessary tables using the provided schema.
Configure the database connection:

Create a .env file in the root of the project and add your database credentials:

makefile
Copy code
DB_USER=your_username
DB_PASSWORD=your_password
DB_HOST=your_host
DB_PORT=your_port
DB_NAME=your_database
Usage
Start the application:

bash
Copy code
npm start
Follow the prompts:

The application will present a menu with the following options:

View all departments
View all roles
View all employees
Add a department
Add a role
Add an employee
Update an employee role
Select an option:

Use the arrow keys to navigate the menu and press Enter to select an option. Follow the prompts to perform the desired action.

Features
View all departments with their IDs.
View all roles with their IDs, titles, salaries, and department names.
View all employees with their IDs, names, job titles, departments, salaries, and managers.
Add new departments, roles, and employees.
Update an employee's role.
Database Schema
The database schema consists of three tables:

Department

id: SERIAL PRIMARY KEY
name: VARCHAR(30) UNIQUE NOT NULL
Role

id: SERIAL PRIMARY KEY
title: VARCHAR(30) UNIQUE NOT NULL
salary: DECIMAL NOT NULL
department_id: INTEGER NOT NULL (References Department)
Employee

id: SERIAL PRIMARY KEY
first_name: VARCHAR(30) NOT NULL
last_name: VARCHAR(30) NOT NULL
role_id: INTEGER NOT NULL (References Role)
manager_id: INTEGER (References Employee)
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing
Contributions are welcome! If you have any suggestions or improvements, please feel free to fork the repository and create a pull request.

Questions
If you have any questions about the project, feel free to contact me:

GitHub: your_github_username
Email: your_email@example.com
Be sure to customize this README with your specific project details, including the GitHub repository URL, your GitHub username, and your email address. Additionally, update the project directory name and any specific instructions relevant to your setup.
