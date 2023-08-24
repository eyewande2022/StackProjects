**MERN STACK PROJECT IMPLEMENTATION ON A SIMPLE TO-DO APPLICATION**


**The main aim for this project is to explain the DevOps concepts and processes using a MERN web stack on a simple to-do application. Some
developers use this set of framework and tools to develop software products. We would be carrying out this project in the AWS platform.
MERN is an acronym of sets of technologies used to develop a technical software product.**

**MongoDB**\
**Express**\
**ReactJS**\
**NodeJS**

**PROJECT:**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0f906575-eb44-4649-babd-a336034be7f6)



**Pre-requisite for the projects is the following.**

**1) Fundamental Knowledge of Installing and downloading software** 
**2) Basic Understanding of Linux Commands**\
**3) AWS account login with EC2 instance**\
**4) Internet connection**\


**IMPLEMENTATION STEPS:**\

**i)** **Ensure you login with your details to your AWS console and click on the EC2 link to create instances.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9f1a6a50-4fb9-41ba-8338-79a6cdaf2b56)


**iii)Click on launch instance dropdown button and select launch instance .**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/87a93f60-ef78-4235-ba04-59f5d7eb8c73)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ec45f3a4-2d4d-4f0e-a304-0b4b95a20e5e)


**iv)Fill in all relevant details to the LEMP project such as:**

**Type in the name and additional tag to the project (mern). Select ubuntu from the quick start option .Also note that the Amazon machine
image selection varies from user to user**

**Select Ubuntu server 22.04 LTS (HVM),SSD Volume Type (Free Tier )**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2be147b7-48d6-4852-aae4-c17473d25249)


**v)The instance type selected in the configuration is the t2 micro-free tier.**

**Click on the "Create new key pair" link.**

**Ensure the Checkbox remains unchanged on the "Create security group".**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1462e357-a9b0-4d5f-b038-225aafa92931)


**vi)Type in the key pair name, chose the default key pair type and private key file format (rsa and .pem) and clicked the "Create key pair
button"**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c32c9ea9-2a2b-4c49-a1c3-e6400bd1e0e9)


**vii) The .pem file was downloaded successfully**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9176d554-e6f7-44c3-9b86-a7cdd8f13e31)


**viii) I have deliberately chosen default settings to allow SSH traffic from anywhere as well as the storage volume given by AWS.**

**Then we proceed to launch our instance finally.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/bcb724f2-8c14-405e-9c4e-8772495beb70)


**Instance successfully launched and click to view Instance details with the IP address.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2bf5e48b-76bc-4a38-884b-99af055ce08a)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/81708412-9503-48a0-a0d2-854d392684fe)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9de5698c-3aff-4712-aee7-698cc311aa39)



**Click the "Connect" button and copy the ssh client details we would be using on the git bash console.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d5493275-f2bb-4851-9687-5aed98cba9c8)


**Open git bash on visual studio code or whichever console is convenient to use. We are using git bash here with Visual Studio Code**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a4d811d0-d3b2-4acb-8aa1-38eb2e27db09)


**Type YES to connect.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/82b35c70-7983-4edf-9fd6-b2f273b3e925)


**You have successful connected to the EC2 instance launched on AWS via
ssh**\

**Type clear to have a clear console and proceed to updating the lists of packages in the package manager.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1e6b3659-8f6c-43f3-8ea1-78187c58db7c)


**Then we proceed to upgrade the packages and Type YES to continue.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/70b922ab-e4b5-4a48-a518-9148bcef8628)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/242f16c1-2ccb-454f-9878-fa8f73ce2f4d)


**Still upgrading**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6195897d-66fd-4c1d-b6b6-e5a398764531)


**Now we need to get the location of Node.js software from the ubuntu repositories by typing the command below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/07723a94-31e5-459b-9fce-4bc8cc80c531)


**We can now install Node.js on the server and confirm the versions of the node and npm package managers as shown below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/791827e3-6970-4ad7-a988-a66fd867717f)


**Once versions are confirmed. We created a directory called To-Do project and verify the directory is present .We then change directory
with the cd command to the new directory we just created .**

**After which we initialize the project with the npm init command as seen below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/efac54c3-abf5-4a55-b8dd-8de201b769c4)


**The reason for this is to create a new package.json file .This files contains the application and its dependencies it needs to run and we
need to press the Enter button several times to confirm the details we intend to use for its documentation and finally click "yes" to proceed
.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/4e8f18fd-5df7-4019-9fac-ba97616be937)


**An error appears which states we should install a new minor npm update from 9.51. to version 9.6.7 as seen below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/856a23ac-a427-43d1-ae0b-dbe584708f50)


**Lets run the ls command to confirm the package .json file is created.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/9db7dea9-2d9b-4382-9319-ee3a050afaf8)

**Next, we will install ExpressJS and create the Routes directory**

**INSTALL EXPRESSJS**

**Express is a framework for Node.js which further simplifies**\
**development and makes things work seamlessly. Express helps to define routes of the application based on HTTP methods and URL's.**

**We install the npm package modules for express and create an index file. Ensure to verify with an ls command to see the newly created
index.js file.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/05eff75e-6a2a-4217-b870-f62de1a54279)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2004eb01-5e91-4e3f-97eb-51309d159378)



**We then install the dotenv module**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d3cfec91-afab-4397-a4b7-ea673d3f6582)


**Edit the index.js file with the vim command and type in the code  below. Please take note of the port :5000 that was in the file .This
would be required late when we want to get it working on the browser.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b761036c-cf27-4cfa-9117-f368003aab54)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/822b1814-72bd-423e-85c1-a035e6115177)


**Save with the esc :wq Enter. Next step is to start our server to see if it works**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6981f59d-197c-4a76-bee3-d77f9b360090)


**Our server is running at port 5000.We need to click Ctrl C to exit from the message caption .We would need to create an inbound rule to
open at port 5000**\

**Click on security button**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0695749d-f798-4200-80ed-befd4b9dcae6)


**And click the security group link.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/74c57a55-8efa-44c1-87cb-c27ccba16e82)


**Click on "Edit inbound rules "in order to add a new rule for port 5000**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e5f6ae28-9787-4d9a-a9a1-4200ac148eee)


**Add a new rule.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/34d15971-d9cb-4431-bf2a-f60e39f2fc09)


**Type in the port range and click "Anywhere ipv4"**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1914daaa-5f86-4a75-baa7-f94506e58cca)


**Click the "Save rules" Button.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/074cef8c-298f-4686-aa15-988664cd30eb)


**Inbound rule successfully modified**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/cd7177bd-7d29-42fd-b374-c1f3391e3b5c)


**Open any browser of your choice and access the URL**

http://100.24.45.95:5000

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/cfada9c0-04a9-4186-afc5-826255c104a5)


**ExpressJS default page successfully displayed.**

**From the MERN stack, we have implemented with Linux and now have Express ready**\

**We would need to perform some actions in our simple to-do application which are the following:**\

**1) Create a new task.**

**2) Display all tasks.**

**3) Delete all tasks.**


**Please note that each tasks is associated with some particular endpoints and would use the standard HTTP request methods namely :POST
,GET AND DELETE**\

**Each tasks would require us to create routes that defines the endpoints that the to-do application would depend on .**
>
> **So we create a folder routes and change directory to the new folder**
>
> ![image](https://github.com/eyewande2022/StackProjects/assets/116227096/73ed69e8-79fe-4619-9cfb-44b60470941a)

>
> **We create a file called api.js**
>
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/25d8e89f-9455-4a26-b173-6d455759fdc9)


**Edit the file and paste some code inside it .press ESC ,save and exit with ":wq**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e738dc7d-82cf-4046-8606-d05dde16114e)


> **After this has been done, we would need to create models because we would be making use of a NoSQL database called MongoDB. These models function at the helm of JavaScript based application and makes it very interactive. Models are also used to define database schema which is the blueprint of how database are constructed including other data fields that aren't required to be stored in a database known as virtual properties.**
>


**To achieve this we need to install mongoose which is a node package.**

**Next step is to change directory back to Todo folder and install mongoose.**


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/be0bc9dc-7c1f-4836-8154-8cbbc3dd0f03)

>
> **Create models folder and change directory into the new folder Create a todo.js file and edit the file and paste this code inside it .**
>
> **press ESC ,save and exit with " :wq" command**
>
>
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/2e539ebf-ff34-4858-a97a-7d8465ac0392)

>
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f4432ad1-975b-4e27-af99-cf96c2167db3)

>
> **Next we need to change the directory to update our routes and edit the api.js in the routes directory to make use of this model as illustrated below.**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a00686df-1251-4db0-a03f-98195f1eeb91)

>
> **Replace this previous line of codes with the delete command :%d**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/adaf8c18-bc08-48c9-afc4-05f5efb49da8)

>
> **With this new set of codes. Press ESC ,save and exit with " :wq" command**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b257637b-43da-4dce-9740-ab35f2595822)

>
> **After completion we need to create the MongoDB database**
>
> **MONGODB DATABASE**
>
> **A database is needed to store data and we would be making use of MongoDB database provided by mlab as a service solution. It is
> expected to have signed up for an account and select AWS as the cloud provider choosing a region close to you .**
>
> **When we click on browse collections we have access to the database name and collection name created .We would need these details when
> configuring the .env file .**
>
> **Please note: When you sign up ensure you change the time of**\
> **deleting the entry from 6hours to 1 week and for the testing purpose we would allow access to our database from anywhere for study purpose but not secure to do that .**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/18b6a362-6340-42d3-8701-7c3c4694914f)

>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/89d3ef2c-4876-4873-a56c-4d0a7af00632)

>
> **When we click on connect, we connect to our application through the drivers as seen below**
>
![image](https://github.com/eyewande2022/StackProjects/assets/116227096/370af0a6-23fa-49f8-92be-b4d3f06c5ff9)

>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/8f511e6e-3286-497b-85e0-db2445a28e26)

>
> **We then cope the connection string and edit the parameter to fit our details ,then input it into our application code in this format**
>
> **DB =
> \'mongodb+srv://\<username\>:\<password\>@\<network-address\>/\<dbname\>?retryWrites=true&w=majority\'**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a2247928-e89d-4437-8ef1-18f263c0395a)

>
> **Create a file in Todo directory called .env and edit the file and paste the connection string from the database inside it .press ESC
> ,save and exit with " :wq**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/821cdf3a-cfb5-467a-b00a-aa849ad47620)

>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/59b79486-ae4b-48e8-99fc-1297b91a2417)

>
> **Then we need to update index.js to show the use of .env so that  node.js can connect to the database**

**Simple delete the existing content and update the previous codes with the code below.**
>
> **Replace this previous line of codes.**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/dc1b29ab-c5fb-49b9-811f-b3c8e94b89a6)

>
> **With this new set of codes below. Press ESC, save and exit with ":wq" command**
>


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/fcfc7b0d-5332-48fe-8740-393c2b2bcea2)

>
> **Using environmental variable is very important and most secure and best practice to store sensitive or secrete data from the
application.**
>
> **We would start our server using the command below and our database should ne connected successfully.**
>


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/1b96d3ec-7f0c-4b34-89e6-f06b44489238)

>
> **Now we open our postman to be able to perform some API request as mentioned earlier. We have to test that all API endpoints are**\
> **working as expected .**
>
> **First task would be to create a POST request. Click the header and select the right key value pair as shown below.**
>

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/24b09c31-c5d6-4bc5-936b-b733176aa804)

>
> **Click on the body and raw, select JSON format .Then type the details as seen below**


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6f40b103-c1ed-4cf3-8529-a2808d3bec2b)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/09079a5f-d35e-46ab-999a-527f78deafa0)


**Then 200 OK status is displayed to confirm it is working as expected.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/67d82d5c-1095-444d-8cf2-bfe75d3248df)


> **Second task would be to send a GET request and with the relevant details we get the Then 200 OK status is displayed to confirm it is working as expected.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a9744a46-c101-4071-91b8-d42491c86cd3)


**Third task would be to delete any request as seen below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/868ae47d-74fd-4c01-8e5d-5849eaf16148)


**After deleting, try to get the same data ,You would find out it has been deleted from the database**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ff767fc0-516e-4f21-b04f-e5ebc02bbc9d)


**Now that we are done with the 3 task, we would then proceed to create the front end**

**FRONTEND CREATION**

**It is time to create the user interface for a web client to interact with the application via API. To start out we would need to use the
command below to scaffold our app.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ee992ced-f7ab-40c6-897d-a68d1b8560e3)


**This would create a new folder called client in the todo directory and this is where we would add the react code .**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ab170621-763a-4948-8c5a-8be651da3ac5)


**We would now 2 dependencies**

**1)Install concurrently which is used to run more than one command simultaneously from the same terminal window.**

**2)Install nodemon which is used to run and monitor the server. If there's any change in the server nodemon would always restart
automatically and load the new changes**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0413134d-8295-46d4-8ec9-f9396c689985)


**Then we would open the package.json file in the todo folder and change the scripts and test section from the file and replace with the code
below**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/392c8a56-3430-4fb5-8cb5-3b95bd12b070)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e9c8561b-ac24-4656-bbdc-b4e02c79ca53)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/ee4c049c-e451-4ec0-941c-7923eb49d240)


**Change directory to client and edit the package.json file and add the key value pair to the file . .Press ESC, save and exit with " :wq"
command**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f81fdad3-af32-4cff-aa46-d9e510457242)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/aef039c5-080f-4e74-b3ca-9dd2d0768920)


**Now ensure you are inside the todo directory and run the npm run dev command. You should see that the application was compiled**\
**successfully.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/941761f4-fc58-4ad1-9086-06fc27870ccd)


**Your application should open and start running on localhost:3000. We would need to create an inbound rule to open at port 3000**

**Click on security button**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/6a3c83db-5b8f-4071-92e9-3c1ed720f84f)


**And click the security group link.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c57d64c1-1cde-4f21-95e1-396d84c0b2b5)


**Click on "Edit inbound rules "in order to add a new rule for port 5000**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/c4d30162-a2a2-4000-b631-001a110b8045)


**Add a new rule.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/759c48c4-02ca-4255-be6d-6ecfb48956a7)


**Type in the port range and click "Anywhere ipv4"**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f5c28646-fbe5-4be6-9a37-5b228a8d8a64)


**Click the "Save rules" Button**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/d65771a0-1b18-4b2b-9705-539f4dfeda31)


**Inbound rule successfully modified**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/68c61397-8a73-41bd-bb09-eab8b6aae32e)


**React app launches successfully at port 3000**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/f014e9b2-d5b6-41b9-b8f1-d259ab795312)


**From our todo app, there would be two stateful component and one**

**stateless component .This is because we want to make the code**

**modular and reusable**

**Change directory to client and move to the src directory .**

**Create another folder names components and change directory into the new folder**\

**Create 3 files as earlier explained (be two stateful component and one stateless component) input.js ListTodo.js Todo.js**\

**Open the input.js file and paste the code below.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/b3396762-1b77-4fa8-baa8-96881d6735e2)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/a9a6cac9-1bfe-4118-9b63-50c520afe05a)


**Then we try to install Axios which is a promise-based HTTP client for the browser and node.js.**

**Move back twice to get to the client folder and install Axios Move to component directory and edit ListTodo.js**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/307e3da1-3eb1-452a-89ad-430e2f738a71)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/574ad2f7-dc47-44e4-b7f6-9ea0e9c5d278)


**We would then navigate to the Todo.js file and copy the code below**

**inside it.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/429519e3-bc63-4dea-8574-e8805b5efa7f)


![image](https://github.com/eyewande2022/StackProjects/assets/116227096/720fb399-0235-4c3e-80c8-1868f9a9b10b)


**We need to make a little adjustment to our react code .Delete the logo and adjust our App.js to look like this**

**Move to src folder**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/e575dd08-e914-4358-a5b4-36a490edf51f)

**Logo has been deleted and replaced**\

**Next step would be to pass the new code below into the App.css file and exit it**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/5e458bd8-d3f8-4515-868f-b1a9725a1c87)

**Next step would be to pass the new code below into the index.css file and exit it**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/0718e31b-d18b-4f5a-8866-252cec1fd960)

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/42cd7664-b8cb-46e3-bec2-494ce564f9e8)


**Navigating back to the todo directory Running the command npm run dev**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/826cf917-4f8b-4311-9e28-d7ae3cf1087d)


**Our To-do application should be ready and fully functional with all functionality working perfectly .**

**Creating a task ,deleting a task and viewing all your tasks.**

![image](https://github.com/eyewande2022/StackProjects/assets/116227096/3f51509f-286d-4c27-9d50-acaf1f318b55)


**Simple to-do application deployed in a MERN stack**\

**A Front-end application using React.js that communicates with the backend application written using Express.js.**

**Created a MongoDb backend for storing tasks in a database**
