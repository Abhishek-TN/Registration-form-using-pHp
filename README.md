# Registration-form-using-pHp
This repository contains a simple registration form built with PHP. The form allows users to register by entering a username and password, which are then securely stored in a MySQL database.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [License](#license)

## Introduction

This project demonstrates a basic user registration system using PHP and MySQL. It includes a registration form where users can sign up by providing a username and password. The password is hashed for security before being stored in the database.

## Features

- User registration with username and password
- Password hashing for secure storage
- Input sanitization to prevent SQL injection
- Error handling for database operations

## Technologies Used

- PHP
- MySQL
- HTML
- CSS (optional for styling)

## Setup Instructions

### Prerequisites

- A web server with PHP support (e.g., Apache)
- MySQL or MariaDB database server
- Composer (optional, for dependency management)

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/php-registration-form.git
    cd php-registration-form
    ```

2. **Database Setup:**

    - Create a database named `businessdb`.
    - Create a table named `users` with the following structure:

    ```sql
    CREATE TABLE users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        user VARCHAR(255) NOT NULL UNIQUE,
        password VARCHAR(255) NOT NULL
    );
    ```

3. **Configure Database Connection:**

    Update the `database.php` file with your database credentials:

    ```php
    <?php
        $db_server = "localhost";
        $db_user = "root";
        $db_pass = "";
        $db_name = "businessdb";
        $conn = "";

        $conn = mysqli_connect($db_server, $db_user, $db_pass, $db_name);
    ?>
    ```

4. **Start the Server:**

    If using a local server setup like XAMPP or MAMP, place the project folder in the `htdocs` directory and start the server.

    Alternatively, if using PHP’s built-in server, run:

    ```bash
    php -S localhost:8000
    ```

5. **Access the Registration Form:**

    Open a web browser and navigate to `http://localhost:8000` (or the appropriate URL based on your server setup).

## Usage

1. Open the registration form in your web browser.
2. Enter a username and password.
3. Click the "Register" button.
4. The form will validate the input and, if successful, store the user data in the database.

## Contributing

We welcome contributions to improve this project! Here are the steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

Please ensure your contributions adhere to the repository's coding standards and guidelines.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
