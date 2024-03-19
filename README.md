# ScummVM File Integrity Check - GSoC 2024

This repository contains server-side code for "System for checking game integrity". This repository is part of the Google Summer of Code 2024

## Getting started
The aim of this setup guide is to allow you to setup and get running an Intregrity Site which is capable of creating all required tables by itself.

### Prerequisites
To configure credentials for the Integrity site, create a JSON file in the root. Below is an example.
* Eg:
`mysql_config.json`
```
{
  "servername" : "your_servername",
  "username" : "your_username",
  "password" : "your_password",
  "dbname" : "your_database_name",
}
```

### Configuration Guide
#### Gather required information
Before continuing make sure you have the following information:
* MySQL server details (servername, username, password)
* Database name
* Path to `mysql_config.json` file

#### Configure MySQL Credentials 
1. Using the file you created in the prerequisites you need to make sure that it is in a directory which can be accessed directly by your PHP script.
2. Populate the JSON file with your MySQL server details.
3. Save the file

#### Setup the Database and tables
1. Create a PHP file (eg: `setup_integrity_site.php`), and copy the code from the link below into the file.
```
https://github.com/scummvm/scummvm-sites/blob/integrity/bin/schema.php
``` 
2. Replace `'/../mysql_config.json'` with the correct path to your `mysql_config.json` file.
3. Upload the PHP file to your server.
4. Access the PHP file through a web browser to execute it. Which will create the necessary database and tables automatically for your integrity site.

#### Verify Setup
1. After executing the PHP script, check if there are any errors reported.
2. Verify that the database and tables have by logging into your MySQL server or using a MySQL client.

### Additional notes
For debugging or checking your code this can all be done locally for example using Local Host on VS Code or XAMPP





