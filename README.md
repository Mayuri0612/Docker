PROJECT DESCRIPTION

This is a small introductory project based on Docker compose. Mysql database and Joomla is integrated where both are running as separate container in my base O.S. Both OS is linked using DNS and Joomla is linked to external clients(any outside computer) using PAT concept.




TECHNOLOGIES USED


-Virtual Box

-Redhat Linux version 8(I prefer)

-Container images:- Joomla, Mysql

-Mysql software

-For Networking: - PAT concepts

-For storage: - Volume concepts

-Docker compose	




STEP BY STEP PROCESS

Considering you have Docker installed in your system and already started, follow the given steps:
1.	Make your account on https://hub.docker.com/
    docker pull mysql:5.7
    docker pull joomla
    
2.	Setup the mysql on your system. To do run the following commands in the same order as shown:

    a)	yum install mysql
    
    b)	docker run -it -e MYSQL_ROOT_PASSWORD= password -e MYSQL_USER=user name –e MYSQL_PASSWORD=password -e MYSQL_DATABASE=database   name --name dbos mysql:5.7
    
    c)	docker inspect os_id | grep IP
    
    d)	mysql –h IP –u username –ppassword
    
    You will be now connected to mysql data base
    
3.	Install Docker compose using following link

    https://docs.docker.com/compose/install/
    
    Then run following commands:
    
    a)	mkdir /mycompose
    
    b)	cd /mycompose
    
    c)	vim docker-compose.yml
    
    In this file write the code as shown in attached docker-compose.yml file 
    
4.	Run the above file and just by one click whole infrastructure gets created. That is why it is known as Infrastructure as a code.

5.	Now run your website in any computer just by writing IP address and posrt number. Bingo! Your Joomla will run on that browser.
