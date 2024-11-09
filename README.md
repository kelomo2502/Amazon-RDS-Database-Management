# Amazon-RDS-Database-Management

This project introduces Amazon Relational Database(RDS) , focusing on creating and setting up databases. It delves into the importance of managing clients database and project details efficiently and securely using best practices

## Let's get practical

- Navigate to search bar of the AWS console
- input RDS service and locate it
- Locate the databases tab on the left side of the panel and click on create database
- Select standard create as database creation method
- Choose MySql engine with the community edition
- Select latest engine or preffered version
- Choose a free-tier template
- Specify the DB instance name
- select master username for your database
- Enter password and reconfirm password
- Choose the db class to be db.t3.micro
- You can keep every other setting here as default
- Choose your VPC
- Select public access as yes for the purpose of this practice
- Choose your secuirty group and ensure that the inbound rule allows traffic from MySQL on port 3306
- Choose your availabilty zone
- You can leave other settigs as default
- Proceed to clicking on the create database button to initiate the process
- NB: The creation might take sometime, so you can refresh the page a couple of times while you wait until the database is created and active
- Now that the database is created, we can click on it to checkout the details
- Copy the database endpoint into a note pad for reference during connection
- We have already created an instnce with amazon-linux image
- Connect to the instance
- Run the code `sudo wget https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm`
- Run `sudo yum localinstall mysql57-community-release-el7-11.noarch.rpm`
- NB: type Y to accept the promptings
- At the root you should run `rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2022`
- Run `sudo yum install mysql-community-server`
- run `sudo systemctl start mysqld.service `
- run `sudo systemctl enable mysqld.service `
- run `sudo systemctl status mysqld.service `

## For connection to the database
- run `mysql -h[endpoint] -P [port] -u [username] -p[password]`
- NB: Remember to replace all the paramaters with your database details
- If you want to see all the databases run `show databases;`
- To use the database you have created execute `use mysql;`
- If you want to the the tables run `show tables;`
- You have successfully created the database and connect to it via your ec2 instance
