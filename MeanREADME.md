# ***MEAN STACK PROJECT IMPLEMENTATION***

**The main aim for this project is to explain the DevOps concepts and processes using a MEAN web stack on a simple to-do application. Some developers use this set of framework and tools to develop software products. We would be carrying out this project in the AWS platform and these concepts are very similar to the LAMP,LEMP AND MERN web stack concept.**

**MEAN is an acronym of sets of technologies used to develop a technical software product.**

**MongoDB Express AngularJS NodeJS**

**MongoDB is the document database that stores and allow it possible to retrieve data. Express JS is the back end application that makes a request to the Database for reads and write and gets response from the database . AngularJS is the front end application  that handles Client and Server requests.Node.js is the JavaScript**

**Pre-requisite for the projects is the following.** 

1) **Fundamental Knowledge of Installing and downloading software** 
1) **Basic Understanding of Linux Commands** 
1) **AWS account login with EC2 instance**
1) **Internet connection**

**IMPLEMENTATION STEPS:**

1) **Ensure you login with your details to your AWS console via the  [https://aws.amazon.com**](https://aws.amazon.com)**
1) **Click on the EC2 link to create instances.** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/df5704fb-3d7b-412f-a1c7-e1ffeed52a93)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b809b5a4-09c1-40bd-bb20-5dddd2fa74ec)


**iii)Click on launch instance dropdown button and select launch instance .**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/38acabf5-9df1-490a-a71b-5abd194afb78)


**iv)Fill in all relevant details to the MEAN project such as:**

**Type in the name and additional tag to the project (mean). Select ubuntu  from the quick start option .Also note that the Amazon machine image selection varies from user to user**

**Select Ubuntu server 20.04 LTS (HVM),SSD Volume Type (Free Tier )**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/93a77629-4ff7-40be-9a3c-fd83bdf2bdbc)

**v)The instance type selected in the configuration is the t2 micro -free tier.**

**Click on the “Create new key pair” link.**

**Ensure the Checkbox remains unchanged on the “Create security group”.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4e63c465-81e5-426a-9fd4-a2b219d58d0b)


**vi)Type in the key pair name, chose the default key pair type and private key file format  (rsa and .pem) and clicked the “Create key pair button”**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/11b88281-02bb-4422-8967-1849ec9615c8)


**vii) The  .pem  file was downloaded successfully** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ac33bcaa-5a1c-4817-a96e-2e05b91e588b)


**viii) I have deliberately chosen default settings to allow SSH traffic from anywhere as well as the storage volume given by AWS.** 

**Then we proceed to launch our instance finally.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ae94dbdb-4d0a-4d8d-b1d4-3a1d2288064d)


**Instance successfully launched and click to view Instance details with the IP address.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/86c1ad27-4250-4794-b84a-24f45fb77f34)


**Click the “Connect” button and copy the ssh client details we would be using on the git bash console.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/740bc8e2-3db3-4284-b9a5-28855927d90a)


**Open git bash on visual studio code or whichever console is convenient to use. We are using git bash here with Visual Studio Code and Type YES to connect.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b0f1b468-04d1-4d4d-91e8-b2a01107c33e)


**You have successful connected to the EC2 instance launched on AWS via ssh**

**Type clear to have a clear console and proceed to updating the lists of packages in the package manager.**

`sudo apt update`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c4d55760-9447-48c1-bb1a-344b74275e8a)

**Then we proceed to upgrade the packages and Type YES to continue.**

`sudo apt update`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/fd5c13b7-9a27-4176-9266-4890adeedb3c)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/59a63650-6277-410e-bd3f-6b00fb19c714)


**Still upgrading and finally completed as shown below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/dece3a77-91a4-489f-91b4-11543795b560)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/27fc9ee1-7627-4fa7-8877-6d8b22435c08)

**Now we add the certificates. Type YES to continue and check the node version** 

`sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common`

`wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add`

`echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list`


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6a2f568d-ef75-4557-85a8-29157426060b)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/fdc86290-a6fd-4afd-97dc-442aa594373f)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5eb496d8-34c3-4fe9-a877-c71ea4f4fa18)



**NODE.JS INSTALLATION**

**Now we need to get the location of Node.js using a node source PPA** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/70cf853b-a559-4ef6-9fd8-bf5e931e6aae)

**We can now install Node.js on the server and confirm the versions of the node and npm package managers as shown below.**

 `curl -sL https://deb.nodesource.com/setup_16.x -o /tmp/nodesource_setup.sh`
 `vi /tmp/nodesource_setup.sh`
 `sudo bash /tmp/nodesource_setup.sh`
 `sudo apt install nodejs`
 `node -v`
 
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/82281d4d-1130-4e8d-b172-0e93af06a858)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/7bd550b2-21cf-4ac5-a07e-111acb4e2e88)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/310ea67a-f2cf-4f60-94b1-bc6a9f9eb652)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/83682548-1ca1-45b3-8b92-2e91ce016650)



**INSTALLATION OF  MONGODB**

**MongoDB stores data in flexible JSON format documents and can vary from document to data structure which can be changed over time .Here we would be adding a book records to the database containing the book name ,ISBN number ,Author and number of pages .We run the  following command as shown below to download MongoDB**

`sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common`

`wget -qO - https://www.mongodb.org/static/pgp/server-5.0.asc | sudo apt-key add`

`echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/5.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-5.0.list`

`sudo apt-get update`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/bab9a790-7b5d-4623-8cbf-f70265d85f01)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d39f63d4-da4d-41f8-af71-7df4f0e767f5)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/8542ad73-b95f-4dc2-819b-d655e360d845)


**Once installed we have to start the server and verify that it is running as expected as shown below . MongoDB is active and running** 

`sudo apt-get install -y mongodb-org`
`sudo systemctl start mongod` 
`sudo systemctl enable mongod`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ebbe8940-5214-4a54-8bab-e484e22674b8)


**Next we install node package manager  and body-parser package** 

`sudo apt install -y npm`
`sudo npm install body-parser`

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c533edd7-4378-481c-92a2-9099e58e5bb0)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5322d791-5e64-4293-9a17-4593c6e53c1d)



**And then proceed to create the folder named Books and change directory to the new Books folder.**

`mkdir Books && cdBooks`
`npm init `

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1e0e3a67-ad8c-400f-b3b0-657152a2b4e1)


**In the Books directory ,we initialize the npm project and add a file into server.js**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9bc1a4a6-026b-4363-8118-959981e12494)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0abcde0b-efb7-404b-841c-7e287affd010)


**INSTALLATION EXPRESS AND SET UP ROUTES TO THE SERVER**

**Express is a minimal and flexible Node.js web application framework that provides features for web and mobile application .We would be installing a Mongoose package which provides straight forward ,schema-based solution  to model application data** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1d5592f4-8c60-4b9e-b00a-982a7117021c)


**We create the folder named apps and change directory to the new apps folder. Edit the route.js file and input the codes below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5a7d0175-f9cf-489d-887d-26b5ec3a721a)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/37e58c06-ae97-48f4-b8b7-eb93763663b8)


**We create the folder named models and change directory to the new models folder. Edit the book.js file and input the codes below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a835bb30-6a3b-4982-b072-5efa32d9cb02)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/aa81e040-f071-44a3-a23e-bfad941bce78)


**ACCESSING THE ROUTES WITH ANGULARJS**

**AngularJS provides a web framework for creating dynamic views in your web applications. We would be changing the directory back to Books  and then we create a new folder named public and change directory to the new folder. Edit the script.js file and input the codes below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/086e80e1-bb49-44a8-a483-12b88a1bd71a)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d7bfd828-7c07-45b7-8251-7d96b6d4d9d2)


**We would creating a new folder named index.html  and edit  the file  and input the codes below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c08d36bc-2a74-45ed-adeb-af2dd1a24117)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/721eaa49-d510-40ef-9c93-f70f3ee85372)


**We would then navigate back to Books and start the server by running a command.** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ea714c29-dca7-4fd1-8d6a-1bf95fe9631a)


**We see the server is up at port:3300**

**For this to happen we need to open TCP port 3300 in our AWS Web Console accessing the security group through the EC2 instance** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/24f021c1-919f-4732-b1c1-8a38ce10df49)


**Add a new rule.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d0533819-05a6-4427-b903-32beae56e2c3)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/28ba46f3-0b4c-4641-8f37-6bc9f25d80b2)


**Type in the port range 3300 and click “Anywhere ipv4”**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/fd65f859-1641-4541-9dc6-97f7c9231baa)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/14b45ccf-1e4f-4014-9f9d-857d5d9a36ed)



**Click the “Save rules” Button**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/52c61d8b-12a1-448d-81e3-1ee9085674ca)


**Inbound rule successfully modified**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/bca1cf5c-4005-4e36-ab11-c887d1edccc5)


**Open any browser of your choice and access the URL** 

**http://54.89.144.227:3300**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/77d0e641-f9a6-49b8-8c1f-b4d17cd2b5c8)


**Book web page successfully displayed.We have to test the web page by inputting data and get it to be populated below** 

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a8eb8879-d1b0-4818-8c02-3953cfc394d8)


**Refresh the page and see the data below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6de03fa5-6cb7-448e-8875-1550cd1535e0)







**Congratulations we have successfully launched our Web Book Register**
