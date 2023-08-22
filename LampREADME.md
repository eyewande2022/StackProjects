## LAMP STACK PROJECT IMPLEMENTATION

The main aim for this project is to explain the DevOps concepts and
processes using a LAMP web stack. Some developers use this set of
framework and tools to develop a software products .We would be
carrying out this project in the AWS platform

LAMP is an acronym of sets of technology used to develop a technical
software product.

Linux

Apache

MySQL

PHP

Please note : (P could also stand for Python or Perl )

Apache server used is the apache2 version

Pre-requisite for the projects is the following.

```
1) Fundamental Knowledge of Installing and downloading software
2) Basic Understanding of Linux Commands
3) AWS account login with EC2 instance
4) Internet connection
```
## IMPLEMENTATION STEPS:

```
i) Ensure you login with your details to your AWS console via the
https://aws.amazon.com
ii) Click on the EC2 link to create instances.
```

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/7257cdd3-fd44-43d8-8651-7fc40289d140)

iii)Click on launch instance dropdown button and select launch instance
.
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/66dfb25c-e38f-4437-9eef-0e95102f90a8)
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5f7a165c-9319-4d92-b2a1-23c273598121)




iv)Fill in all relevant details to the lamp project such as :

Type in the name and additional tag to the project (lamp) .Selected
ubuntu from the quick start option .Also note that the Amazon machine
image selection varies from user to user

Select Ubuntu server 22.04 LTS (HVM),SSD Volume Type (Free Tier )

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/26a705af-1f6e-41b5-8363-9fe968c5714e)


v)The instance type selected in the configuration is the t2 micro -free
tier.

Click on the “Create new key pair” link.

Ensure the Checkbox remains on the “Create security group”.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/941d5471-018b-4d68-bb5c-6b19c43719db)


vi)Typed in the key pair name, chose the default key pair type and
private key file format (rsa and .pem) and clicked the “Create key
pair button”
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9b428a5e-d4f1-49b1-b048-de22ff0230e2)


vii)The .pem file was downloaded successfully.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ed43e0f2-8781-4206-b38b-f92c13377c68)

viii)I have deliberately chosen default settings to allow SSH traffic from
anywhere as well as the storage volume given by AWS. Then proceed to
launch our instance finally.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4c31dc5b-6c53-4e22-86fa-63974ae1a600)

ix)Instance successfully launched.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9380c35f-f72b-49ec-a2da-035e3752dba6)

x)Select checkboxes to view more details about the instance created.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/652a8f94-d8c5-401b-ba31-a1392d246092)

```
The public IP address shown on the screenshot should be
copied as we would be using it on the console.
Open git bash on visual studio code or whichever console is
convenient to use.
```
```
We are using git bash here with Visual Studio Code
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4dc03fd8-138a-483f-be88-3a61fba06f10)

```
Type YES ,to connect
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/fddf3ae1-9adf-4f64-a61e-dbbd4c47719e)

```
You have successful connected to the EC2 instance launched
on AWS via ssh
```
```
Type clear to have a clear console and proceed to updating the
lists of packages in the package manager
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c4b78b82-08f5-428c-8813-63a34f850024)

```
Then we run apache2 installation and click yes to complete
installation
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/3a996ac0-cf99-4ef1-9998-3446496c8be7)


We have to verify that Apache is running in our Operating
System.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/45d47c13-b1fd-4fbd-9dfa-078fbfc99aae)


To proceed by launching the web server in the AWS Cloud, we
need to navigate back to the security group on the platform to
add a new rule for TCP port 80 which is the default for web
browsers.
Once done we can access the web page on internet.

Click on security button.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b28d03c4-8cb8-4ba7-959c-5d61eaba0ddb)


And click the security group link

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f03f6791-393e-4c0b-b5bf-f2b248d2efe1)

Click on “Edit inbound rules “ in order to add a new rule for
port 80

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5819f0a4-0d5f-4566-afb9-f5b53a2fa0c1)


```
Add a new rule
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f7e739d3-6a1c-4c88-b3f3-370856506a6d)

```
Type in the port range and click “Anywhere ipv4”
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9496a5f3-4ed5-45fc-8848-c6de2ad17b63)

```
Click the “Save rules” Button
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/8bea2083-c6d6-4609-b208-6cf0c431c8c7)

```
Inbound rule successfully modified.
```
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0fb0aa3a-7d82-43b2-8a8d-464adf09331b)

Open any browser of your choice and access the URL
[http://34.201.134.152:](http://34.201.134.152:)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f480646c-19ba-474d-ac7a-a425d3eaf505)


Apache2 default page successfully displayed.

From the LAMP stack, we have implemented with Linux and got
Apache ready.

Next step would be to get the MySQL installed.

## MYSQL INSTALLATION

Now that our web server is running, we need a relational
database uses within the PHP environment hence we install
MySQL server

Type “Y” and enter.
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6c694f5a-3823-4de7-a5b5-351a82b0bb80)

When installation is finished, Log in to connect to the MySQL
server as the administrator user root so that you can have
access to the sudo command.


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/39eb697c-d60d-4a41-b3d4-647b40af3d2e)

It is important to set up a password for the user root using
mysql_native_password as a default authentication method.
Please note, Password not revealed for security purpose
Exit MySQL

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1951f861-1eb1-4f97-819e-4ae139c469bf)

Interactive script is started, and all modifications are
answered with a Y/N response

```
Root user password was set Validate password: No
Change password: No
Remove anonymous user: No
```

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/397dac64-3871-464a-93ef-81564ddcb1ae)

Disallow remote login: No

Remove test data base and access to it: No

Reload Privilege tables: Yes.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4e401a0c-7883-4f71-aa63-7690afd3836a)

Verify login details to ensure all details were inputted correctly and
exiting MySQL


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/331d17ad-be57-4816-8455-ea312f49bbb0)

MySQL server was correctly installed and secured.

Next, we proceed to the PHP installation which is the final component
of the LAMP STACK

## PHP INSTALLATION

PHP is the component that would process the codes to display dynamic
content to the end user. Hence, we would need to install 3 packages
namely :

1)PHP package 2) libapache2-mod-php 3) php-mysql.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1168dda6-022e-45fe-9f0e-34a248434b5b)

Installation continues.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/90d16169-14e8-485f-ada7-33a72b970507)

After installing, we check the PHP version.
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/aace9840-3e37-4837-8498-53bb88345fb5)

At this point the LAMP STACK implementation is completed and fully
operational

We need to test our set up with a PHP script and this needs a proper
APACHE virtual host to keep your website files and folder .Multiple
website can be hosted on a single machine and the users would not
notice

# CREATING AN APACHE VIRTUAL HOST FOR OUR WEBSITE TO USE.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1a3fa833-d526-4608-b51f-fc29705eebc5)


Next step, making a directory for the site directory, running below

Then proceed to edit a new site directory to input the virtual host
information.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c09ebf3e-ada8-4708-ba68-e1201b06183f)


Put the edited file in an insert mode by typing “i” without quotes and
add the config files, press ESC ,save and exit with “ :wq” command

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/42a8d339-ec61-459d-a373-55a726dc1bce)


Next check the content of the sites-available directory and you would
see 3 configurations files on here.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/211b4d83-9a96-45d2-bb5d-c2305133cd94)

With this configuration files, we would need to DISABLE the 000-default
config file and ENABLE the new directory we created using the
following command

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/bf1aab3d-e4b0-426a-95b3-96f6ebf41300)

After enabling and disabling done successfully, we would verify that
there are no syntax errors with the command below


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0423639a-4ec5-4bfc-8fe4-6fce9c4a5f57)

Then we proceed by reloading the Apache server to make these
changes take effects.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0f598764-f1b5-4aaf-b782-8fa977cee515)

The new website is now active but the projectlamp has empty file .We
create an index.html file in that location so that we can test our virtual
host is performing as expected.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1c8297eb-e2db-4c67-adc5-8fbfb2ccf5d0)

Proceed to the browser and open the previous website using the ip address

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/dbada1a6-4b85-4a43-a30b-c9fee0b52c79)

Echo successfully displayed but this is just to test the website.

Type “clear” command to clear screen.


## ENABLE PHP ON THE WEBSITE

We would need to set up an index.php file to replace the index.html file
from the document root as it needs to override the default settings.
This is a very useful maintenance page in PHP application

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/45ae89aa-267a-45cb-9964-2d528b92d977)

Files are edited correctly while index.php and index.html are in that
order respectively.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c8c763cf-983e-4463-9936-7f1e31eb5b43)

Edited successfully and the Apache needs to be reloaded again by the command below.


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/7eb6b374-488b-4995-ba6c-c1722db4de42)

Finally we would create the PHP script to test that PHP is correctly installed and configured on the server .The importance is to be able to
handle and process request for PHP files with the command below

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/06e9f950-8bde-4dcc-9f0b-ae88760eef1e)


Put the edited file in an insert mode by typing “i” without quotes and add the valid PHP code files, press ESC ,save and exit with “ :wq” command

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b18305d8-4e2c-461a-9e00-03ec0f031910)


Refresh the web page and you would see the web page server in a PHP perspective.

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a8299895-377d-4014-b5d3-a1bf2e6ef93a)


This is the minimum requirement to set up an AWS instance with LINUX
,APACHE,MYSQL AND PHP for a web project.

Please note: Remember to terminate your EC2 instance.


