# Task List Project

This is a simple Task List project built with PHP and MySQL. Follow the instructions below to set up the project on your local machine.

## Installation Guide

### Prerequisites
- Download and install [XAMPP](https://www.apachefriends.org/index.html).

### Setting Up the Project

1. **Download the Project**
   - Clone this repository or download the ZIP file and extract it.

2. **Move Files to XAMPP**
   - Copy the project folder and paste it into the `htdocs` directory inside your XAMPP installation folder.

3. **Set Up the Database**
   - Open XAMPP and start **Apache** and **MySQL**.
   - Open [phpMyAdmin](http://localhost/phpmyadmin/).
   - Create a new database named **epicsystem**.
   - Import the provided SQL file (`database.sql`) into the `epicsystem` database.

4. **Configure Database Connection**
   - Open the `connect.php` file in the project folder.
   - Modify the database connection settings if needed:

   ```php
   <?php
   $servername = "localhost";
   $username = "root"; // Default for XAMPP
   $password = ""; // Default is empty in XAMPP
   $dbname = "epicsystem";

   $conn = new mysqli($servername, $username, $password, $dbname);

   if ($conn->connect_error) {
       die("Connection failed: " . $conn->connect_error);
   }
   ?>
   ```

5. **Run the Project**
   - Open your browser and go to:
     ```
     http://localhost/project-folder-name/
     ```
   - Replace `project-folder-name` with your actual project folder name inside `htdocs`.

## Additional Notes

- Ensure XAMPP's Apache and MySQL services are running before accessing the project.
- You can modify database connection details in `connect.php` if using different credentials.