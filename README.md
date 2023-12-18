Code From @shreys7 https://github.com/shreys7
# django-todo
A simple todo app built with django

![todo App]https://github.com/RishiKandi/ToDo-List-Django.git
### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
$ git clone (https://github.com/RishiKandi/ToDo-List-Django.git)

cd  ToDo-List-Django
```
You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide

Once you have downloaded django, go to the cloned repo directory and run the following command

```bash
$ python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
$ python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
$ python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
$ python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

**Deploy on AWS EC2 Instance:**

**Navigate to the EC2 Dashboard:**
Once signed in, go to the "Services" menu at the top left corner and select "EC2" under the "Compute" section. This will take you to the EC2 Dashboard.

**Launch an Instance:**
On the EC2 Dashboard, click the "Launch Instance" button.

**Choose an Amazon Machine Image (AMI):**
Select an AMI that suits your needs. The AMI is essentially a pre-configured template for your virtual machine.

**Choose an Instance Type**:
Select the instance type based on your requirements. Different instance types offer varying amounts of CPU, memory, storage, and networking capacity.

**Configure Instance:**
Configure the instance details such as the number of instances, network settings, and other options. You can use the default settings or customize them as needed.

**Add Storage:**
Specify the amount of storage for your instance. You can add additional volumes if necessary.

**Add Tags (Optional):**
Add tags to your instance for better organization and identification. Tags are key-value pairs.

**Configure Security Group:**
Configure the security group to control inbound and outbound traffic to your instance. You need to define rules for which ports should be open.

**Review Configuration:**
Review your instance configuration to ensure everything is set up correctly.

**Launch:**
Click the "Launch" button.

**Key Pair:**
Choose an existing key pair or create a new one. A key pair is required to connect to your instance securely.

**Launch Instances:**
Click the "Launch Instances" button.

**View Instances:**
After launching, go back to the EC2 Dashboard and click on "Instances" in the left navigation pane to view your newly created instance.

**Connect to the Instance:**
Once your instance is running, you can connect to it using SSH (for Linux instances) or Remote Desktop (for Windows instances). Use the key pair you selected or created during the launch process.

Once Connect to EC2 Instance Clone the Repo and run the code, Navigate to the public ip address of instance and follwoed by port
(python3 manage.py runserver 0.0.0.0:8000)

**Dockerize Deployement**
Created a Dockerfile
 
Build Docekrfile 

```bash [docker build -t imageName .]

Run Container

```bash [docker run -d -p 8000:8000 imageName]

Check Docker Logs
```bash [docker logs (container id)]

Check Running Containers
```bash [docekr ps -a]

That's It. Deployed on EC2 Instance with dockerfile.
