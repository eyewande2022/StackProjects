# LEMP STACK PROJECT IMPLEMENTATION

**The main aim for this project is to explain the DevOps concepts and processes using a LEMP web stack. Some developers use this set of framework and tools to develop software products .We would be carrying out this project in the AWS platform**

**LEMP is an acronym of sets of technologies used to develop a technical software product.**

**Linux**

**NGINX**

**MySQL**

**PHP**

**(P could also stand for Python or Perl )**

**NGINX is pronounced engineX where the acronym “E” originated from**

**Pre-requisite for the projects is the following.**

1. **Fundamental Knowledge of Installing and downloading software**
1. **Basic Understanding of Linux Commands**
1. **AWS account login with EC2 instance**
1. **Internet connection**

**IMPLEMENTATION STEPS:**

1. **Ensure you login with your details to your AWS console via the [https://aws.amazon.com**](https://aws.amazon.com)\*\*
1. **Click on the EC2 link to create instances.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/69c600bc-a057-4deb-9f90-4ee1f6757d3f)



**iii)Click on launch instance dropdown button and select launch instance .**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9f649f47-b146-4a5d-b514-e3f467d729a4)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d8e3f206-96ea-4c4b-88bd-6d0651577e9b)


**iv)Fill in all relevant details to the LEMP project such as :**

**Type in the name and additional tag to the project (lemp) .Select ubuntu from the quick start option .Also note that the Amazon machine image selection varies from user to user**

**Select Ubuntu server 20.04 LTS (HVM),SSD Volume Type (Free Tier )**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/04a6711f-e1ab-4529-9718-de9c287d4bbd)


**v)The instance type selected in the configuration is the t2 micro -free tier.**

**Click on the “Create new key pair” link.**

**Ensure the Checkbox remains unchanged on the “Create security group”.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/73ee3bbe-c906-462e-8a13-dcf93cecbca8)


**vi)Type in the key pair name, chose the default key pair type and private key file format (rsa and .pem) and clicked the “Create key pair button”**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/424f0ac8-43eb-446f-991d-6dcde2d79084)

**vii) The .pem file was downloaded successfully**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/28ca77e0-c7e0-4530-a160-dc7aaa9d2d02)


**viii) I have deliberately chosen default settings to allow SSH traffic from anywhere as well as the storage volume given by AWS.**

**Then we proceed to launch our instance finally.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/7c7406c8-da23-4f8c-8898-5148558acd7d)


**Instance successfully launched and click to view Instance details with the IP address.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6062e4ee-9a0e-4503-9dc9-5de65dd185cb)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/aa948c02-1afa-4405-ba4b-03ee97e8c0c5)


**Click the “Connect” button and copy the ssh client details we would be using on the git bash console.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b2125e06-4e11-4479-a6f1-91b6642572e9)



**Open git bash on visual studio code or whichever console is convenient to use. We are using git bash here with Visual Studio Code**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/50496613-1a3b-46df-9542-f6e8a0ddf438)


**Type YES to connect.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a3970fc4-0d9a-48df-b44f-eef7f3d0669f)



**You have successful connected to the EC2 instance launched on AWS via ssh**

**Type clear to have a clear console and proceed to updating the lists of packages in the package manager.**

`sudo apt update`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ac79969e-f4d6-4342-b14b-f6b257820260)


**Then we run apache2 installation and click yes to complete installation**

`sudo apt install nginx`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ec760165-d210-41dc-9edb-f3b6b66c2dba)


**Type YES to continue NGINX installation.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/238134bd-8b92-47cb-a9bf-38fcffa37618)

**We have to verify that Nginx is running in our Operating System and press the**

**Ctl + C button to get the ubuntu root.**

`sudo systemctl status nginx`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2b5865d8-3ac5-4468-a391-fb2a8cdedc55)


**To proceed by launching the web server in the AWS Cloud, we need to navigate back to the security group on the platform to add a new rule for TCP port 80 which is the default for web browsers. Once done we can access the web page on internet.**

**Click on security button.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5014cf54-e224-48cf-89c4-8eb38ccef2ac)


**And click the security group link.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/397b6191-909e-414a-bb3e-2070b8800567)


**Click on “Edit inbound rules “in order to add a new rule for port 80**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/08df446c-b0e7-4db5-a5c2-08b77e993c4c)


**Add a new rule.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/aaaa7465-e0c9-45a5-90e7-b82c302f30dc)


**Type in the port range and click “Anywhere ipv4”**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4ca32113-4851-4e2f-bb73-370915d0b979)


**Click the “Save rules” Button**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/80a61b46-1988-4d17-ad38-6696fd7b56f8)


**Inbound rule successfully modified**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/afe45f97-3c45-46e7-8039-9eacf94ab9e5)


`      `**Open any browser of your choice and access the URL http://3.95.228.188:80**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0de6b34d-bb72-44fb-9cee-b8555c4efc6d)

`  `**Nginx default page successfully displayed.**

**From the LEMP stack, we have implemented with Linux and now have Nginx ready .**

**Next step would be to get the MySQL installed .**

**MYSQL INSTALLATION**

**Now that our web server is running, we need a relational database uses within the PHP environment hence we install MySQL server**

**Type “Y” and press Enter**

`sudo apt install mysql-server`


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/99070383-4648-421e-a98f-cfb08d6bdcca)


**When installation is finished, Log in to connect to the MySQL server as the administrator user root so that you can have access to the sudo command.**

`sudo mysql`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/dde3d2af-6478-4d5b-a61e-d9fc798cc6e5)


**It is important to set up a password for the user root using mysql_native_password as a default authentication method. Please note, Password not revealed for security purpose Exit MySQL**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/75f907b3-10a3-41db-969b-04daf44b7be5)


**Interactive script is started and all modifications are answered with a Y/N response .**

**Root user password was set Validate password: No**

**Change password: No**

**Remove anonymous user: No**

`sudo mysql_secure_installation`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c2f4076e-dff9-42cd-9cf5-663ab4536160)


**Disallow remote login: No**

**Remove test data base and access to it: No Reload Privilege tables: Yes**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d7379700-3f82-480d-a0d2-a747f102d67f)


**Verify login details to ensure all details were inputted correctly and exiting MySQL**

`sudo mysql -p`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/14a72653-9702-49a3-908d-6a31d81865df)


**MySQL server is now installed and secured .**

**Next, we proceed to the PHP installation which is the final component of the LEMP STACK**

**PHP INSTALLATION**

**PHP is the component that would process the codes to display dynamic content to the end user. Nginx requires an external program to handle the PHP processing and this act as a bridge between PHP interpreter and the web server .This enhances the overall performance for most PHP web based site .It is called the PHP fastCGI process manager)**

**Hence ,we would need to install 2 packages namely : 1)php-fpm 2) php-mysql .**

`sudo apt install php-fpm php-mysql`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1cc661c9-622f-446e-8a41-d53a271d2924)


**Installation continues.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/28c1bc2a-277b-406e-b5fa-2c4954278a36)


**At this point the PHP component is installed but we need to configure the Nginx to use the PHP processor**

**CONFIGURING NGINX TO USE PHP PROCESSOR**

**We need to create server block to encapsulate the Nginx configuration details and it can host more than one domain on a single server .Therefore we would create a direct structure with the /var/www for the domain website .**

**Root web directory created for our domain below.**

`sudo mkdir /var/www/projectLEMP`

``
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/62054e73-d9e1-4f0b-afb3-a69c5b4fe8c5)


**Then proceed to open new nginx in sites-available directory using the vim editor**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/281027de-d13d-4f5b-9f22-622b651cccac)


**Put the edited file in an insert mode by typing “i” without quotes and add the bare-bones configuration files ,press ESC ,save and exit with “ :wq” command**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0b4aad44-4f07-42e7-92ba-2b80e6ea0374)


**Please observe the following functions the location block carries out: listen: Port Nginx listen to port 80**

**root: defines where the document root is served and stored by the website**

**index: defines how Nginx prioritize the index files. Index .html file gets the highest priority than the rest of the indexes.**

**Server-name: The domain name or Ip address the server block is responsible for .**

**Location: Includes try file directives that checks the files that correlates with the matching URI request. If not found, it will return Error 404**

**Location ~\.php$: Handles the PHP processing and ensures it points Nginx to the fastcgi-php.conf files and declares what socket is associated with php-fpm**

**Location ~ /\.ht : deals with .htaccess files that Nginx does not process by denying all directives and ensuring they are not served to users .**

**Now we have to activate our configuration by linking the config files from Nginx site –enabled directory and also test the configuration to know if the syntax are OK**

`sudo ln -s /etc/nginx/sites-available/projectLEMP`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1d63f285-be08-4edf-8dbf-7c7175b45794)


**Test successful and syntax are okay.**

**Next step is disabling default nginx host that is currently configured to listen to port 80.**

`sudo unlink /etc/nginx/sites-enabled/default`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ea8ea0f9-0b2a-4647-970e-1cc09525d6fd)


**Proceed to reload Nginx to apply all changes.**

`sudo systemctl reload nginx`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/61ce4363-37d9-4c6b-a23a-d4513601b9f9)


**Hence , Our new website is active but note that the /var/www/projectLemp is empty.**

**We should create a file in that location so that we can test that the blocks is working as expected .**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e31a0361-5c76-4dde-bd0d-06c01904c190)


**Now go and launch your browser URL using the IP address. [http://3.95.228.188:80**](http://3.95.228.188:80)\*\*

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/7e70656f-0567-4d55-a4c9-a3d209e9c80b)


**Our LEMP stack is fully configured successfully.**

**Next would be to create a PHP Script to test that our Nginx can handle .php files within the new configured website.**

**TESTING PHP WITH NGINX**

**Our LEMP stack is set up and completely installed and fully operational. We would test to validate that Nginx can handle .php files off to our PHP processor.**

**Create a new file called info.php and paste the file**

`sudo vim /var/www/projectLEMP/info.php`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e2e39893-98a6-4d8d-b398-b3a254d6a801)


**Paste the simplest valid php code that would return information about your server**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e0ce08ef-00cc-45e6-82f9-c0477a232e72)


**Let us access this page on our web browser with the endpoint /info.php [http://3.95.228.188/info.php**]
(http://3.95.228.188/info.php)\*\*

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/701a7625-83fa-4c8e-80cb-2ff3c5fbd24b)


**A webpage containing details information about our server should be successfully displayed .**

**Please note: After checking the relevant information about your php .Its best to remove the file created as it contains sensitive information about your PHP environment and your ubuntu server by the command below**

`sudo rm /var/www/your_domain/info.php`

**Next ,we would be retrieving data from MySQL database with PHP**

**RETRIEVING DATA FROM MYSQL DATABASE WITH PHP**

**We would be creating a test database with a simple To-do list and configure to access it ,so the Nginx would be able to query data from the database and display it .**

**A new user would be created with the “mysql_native_password” in order for it to connect to the MySQL database from PHP**

** Our new user: example_user**

** Our new database: example_database 

** We would connect to the root account by the command below**

`sudo mysql -p`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0e339953-e019-4a88-b9a5-be177ffb5f02)


**Then we create a new database called “example_database” and password.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5c3bec15-1efd-442f-8af0-88f525d5ca8f)


**We grant all permissions to the new user over the new “example_database” in order to give the new user full privileges.**

**We exit the shell and test if the new user has actually been granted permission to be able to login to the MySQL console again and display the database.**

`mysql -u example_user -p`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/70aeec5b-aa06-4406-a9d7-ac2acd11ddfb)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/49a52d0a-7d51-4dbc-b598-c475f0a670bc)


**Next, we create a test table named “todo_list” and input 4 different values on each section**


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9ec38e50-ca9f-4233-b223-a1ad908643dd)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/af636a53-68ca-4448-83db-bd6c207a2eaf)


**We confirm that the data were successfully saved to our table below and exit the table.**


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c8e55dc6-0e7d-451e-a750-d704d99f232a)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/691455eb-9289-421c-a218-1b54e21ee6b8)


**Next, we create a PHP Script that would connect to the MySQL database for our content in out root directory using vim editor to input the PHP script in the todo_list.php**

`sudo vim /var/www/projectLEMP`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2cbecb58-cbf1-4d67-b46c-d0b1e17b5ebe)


**Save and close file when done editing.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ce78e77b-ba5e-48ed-be21-f0b93424fa2b)


**We can now access the page in the browser by visiting the IP address configured for the website follow by the endpoint /todo_list.php**

[**http://3.95.228.188/todo_list.php**](

http://3.95.228.188/todo_list.php)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2a3c56c9-a1ba-4676-9a7f-71bc34ecd191)

**Test table have been successfully displayed on the webpage and our PHP environment has connected and was able interact with our MySQL server**

**Congratulations.**
