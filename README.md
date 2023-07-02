# Laravel Docker Development Environment
This repository contains a Dockerfile and docker-compose.yml file that can be used to build a development environment for Laravel applications. The environment includes an Nginx web server, a MySQL database, and a MailDev mail server.

## Getting Started
- Clone this repository to your local machine.
- Install Docker and Docker Compose.
- In the root directory of the repository, run the following command to start the environment:

Use code with caution. Learn more
```
docker-compose up -d
```

The laravel application will be available at http://localhost:80, through nginx proxy

## Configuring the Environment
The environment can be configured by editing the .env file in the root directory of the repository. The following environment variables are available:

* DB_DATABASE - The name of the MySQL database.
* DB_USERNAME - The username for the MySQL database.
* DB_PASSWORD - The password for the MySQL database.
* MAIL_DRIVER - The mail driver to use. Valid values are "maildev" and "smtp".
* MAIL_HOST - The host of the mail server.
* MAIL_PORT - The port of the mail server.
* MAIL_USERNAME - The username for the mail server.
* MAIL_PASSWORD - The password for the mail server.

Also if you have to change the name of the application ("app" by default) in the docker-compose file, make sure you also change it in nginx/conf.d fastcgi paramaters. So you have to change `fastcgi_pass app:9000;` to `fastcgi_pass newname:9000;`

## Troubleshooting
If you encounter any problems with the environment, please check the following:

* Make sure that you have installed Docker and Docker Compose.
* Make sure that you have built the image and started the environment.
* Make sure that you have configured the environment correctly.
* If you are still having problems, please open an issue on the GitHub repository.
