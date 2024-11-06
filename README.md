# ShopEase
A student-level e-commerce application.

Content in the README.md file:
**Overview of services and technologies used.**
The services our e commerce platform provides is:
  1. User Service – Handles user registration and login. 
  2. Product Service – Manages the product catalog. 
  3. Order Service – Manages orders and payments.

**The Technologies used in our platform are**
-> Python Spring Boot
-> Java
-> Node.js i.e. JavaScript
-> html and css

Moreover, we have the Dockerfile, the docker-compose.yaml file and the reverse proxy nginx.conf file.

**Instructions on how to run the project locally with Docker Compose.**
For locally running the project you need to:
**Step#01**
Create a directory in your local disk
get inside this directory
open git bash and for initialization run the command:
git init
then Clone this git repository by the git command as:
git clone https://github.com/imamamahboob/ShopEase.git

**Step#02**
Create images of each service by getting into the respective folders and open powershell
Start the docker engine
run:
docker login
then run
docker build -t <yourusername>/<yourimagename>:latest .
then run
docker run -p <anypporthere> <yourusername>/<yourimagename>:latest

Note: Carry on these steps for the 3 services and your images will be built and run.

**Step#03**
for docker compose
cd to the main working directory
open powershell and run
docker compose up
Note: You should have the docker-compose.yaml file 


**Git workflow and collaboration guidelines.** 
First have a look at:
1. Setting Up Repository and Branching Strategy 
o Initialized a Git repository for ShopEase in my local working directory and create a remote GitHub repository. 
o Created branches for different roles: 
 main: Stable, production-ready code. 
 Feature branches:
  -> feature/user-auth
  ->feature/product-catalog
  ->feature/order-management
   - all for specific service tasks. 
2. Workflow
   1. All the branch specific code was committed and pushed in their respective branches
   2. After that, the main barnch pulled all branches into the local main branch.
   3. Following, the local main branch committed code was pushed onto the remote repo
   4. 3 compare and pull requests were accepted and each branch's code was verified and matched before merging it into the origin/main branch - where the ready and deployable code stays.
    ![merge requests](https://github.com/user-attachments/assets/f61e82d5-2861-4005-a34b-71e812c34206)


**Additionals:**
->Used environment variables stored in a .env file for database credentials, ports, 
and other configurations. 
->Set up a reverse proxy using Nginx for handling all requests and directing them 
to the correct service based on the request path. 

**Environment variable configuration details.**
you may have the .env file similar to this:

USER_SERVICE_PORT=5000
PRODUCT_SERVICE_PORT=3000
ORDER_SERVICE_PORT=8080
POSTGRES_USER=your_postgres_user
POSTGRES_PASSWORD=your_postgres_password
POSTGRES_DB=your_database
MYSQL_ROOT_PASSWORD=your_mysql_root_password
MYSQL_DATABASE=your_mysql_database


