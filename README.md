# Setup Docker for Laravel 10 Projects

This is a setup elabored to create a dockerized environment for a Laravel v10.x project.

## Build with

| Name       | Version  |
| ---------- | -------- |
| Laravel | v10.x |
| PHP | v8.2.x |
| Docker | v20.10.x |
| Docker Compose | v3.8.x |
| Redis | v6.2.x |
| Mysql | v8.0.x |

## Step by Step

### Step 1

Clone the Laravel files from the official repository. This will get the latest version (**10** at the time of the creation of this setup).

```sh
git clone https://github.com/laravel/laravel.git my-laravel-application
```

### Step 2

Clone this repository.

```sh
git clone https://github.com/dehsilvadeveloper/setup-docker-laravel10.git setup-docker-laravel10
```

### Step 3

Copy the files from the folder **setup-docker-laravel10** to the folder of the Laravel application.

```sh
cp setup-docker-laravel10/* my-laravel-application/
```

### Step 4

Remove the folder **setup-docker-laravel10**.

```sh
rm -rf setup-docker-laravel10/
```

### Step 5

Access the Laravel application folder.

```sh
cd my-laravel-application/
```

### Step 6

Verify the following files and change **names** to consider the name of your application:

- .env.example
- .env.testing
- docker-compose.yml
- .docker/mysql/scripts/initdb.sql

You can change database name, docker network name and application name, for example.

```
DB_DATABASE=application_database

could be changed to

DB_DATABASE=laravel_blog
```

### Step 7

Install the application using the Makefile.

```sh
make start-install
```

### Step 8

Access the project via url.

```
http://localhost:9999
```

## Connecting to the MYSQL database

To connect to the MYSQL database using a program like **Mysql Workbench**, you can use the following information.

```
hostname: localhost
port: 3398
username: root
password: root
```

## About Make scripts

You can check more about the Make scripts available using the help.

```sh
make help
```
