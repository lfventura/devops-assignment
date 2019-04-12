## Preparation
Dentro de la carpeta `task` you will find an Ansible Playbook to provision a new server
This task was prepared to be executed using Virtualbox or Parallels

### Base server image
- Debian 8

### Services to be launched
- nginx
- PHP7.0
- MySQL5.6

### Setup
1. cd devops-assignment/tasks 
2. `vagrant up --provision`

Te execute or provision again, execute `vagrant provision`
Access the instance via https(s) at `http://myplay.local`

## Tasks
### Part 1: Ansible and Linux fundamentals
01. There are one or more errors in the ansible playbook. It is necessary to correct the errors so that the playbook completely turns
02. Create a role that blocks the machine's TCP ports to only allow ports 80, 443 and 22 from any source
03. Configure nginx so that the http page redirects to the https page
04. Nginx can not return in headers the version of Nginx. Configure the server so that this field is not filled in the response header
Create a new role that creates users on the server. This role should create the users `dev1` and` dev2`, and users should not have a password, but should be public key authentication. Users' public keys can be found in the `pubkeys` directory


### Part 2: Docker (optional)
06. Create a directory called `docker`
07. Migrate services running on the Virtual machine to run on Docker containers. Each Service must run in a different container
08. Specify the process to start the docker environment created in the previous item

### Part 3: Questions

09. What is missing for this system can be considered as production? Which points should be reviewed?

10. Suppose the web application is already running at a time and has begun to receive a lot of traffic. What techniques would you use to ensure site performance?

11. What would you need to do if you wanted to configure more than one vhost on this nginx server?

12. Explain briefly: How would you do to promote the DEV environment code to production? How many environments do you think you need and what process would you do for promotion between environments?

13. What is Auto Scaling? How to implement? Is it possible to have Auto Scaling with Containers?

14. What is CI? What is CD? What tools do you know?

15. Describe what would be the ideal in your opinion regarding monitoring the site that we have just uploaded. What should we monitor and what tools could be used?

16. Which Public Clouds have you worked with?

