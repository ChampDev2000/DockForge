\# 🐳 Ruby on Rails Development Environment (Docker)



This repository provides a lightweight and reproducible setup for developing \*\*Ruby on Rails\*\* applications inside Docker.  

It includes Ruby, Rails, and an optional PostgreSQL instance for local testing.



---



\## Getting Started



\### 1. Add your project files

Place your Rails project’s `Gemfile` and `Gemfile.lock` in the same directory as the `Dockerfile`.  

These are required so that the following line in your Dockerfile works during the build:

```dockerfile

COPY Gemfile Gemfile.lock ./



\## Build the Docker image

Run this command in the directory containing your Dockerfile:



```bash

docker build -t rails-dev .

```



\## Run the container

Start an interactive container and expose port 3000:



```bash

docker run -it -p 3000:3000 rails-dev bash

```

This opens a shell inside the container.



\## (Optional) Install PostgreSQL inside the container

If you want to test Rails with a local PostgreSQL instance inside the same container, run:



```bash

apt update \&\& apt install -y postgresql postgresql-contrib

service postgresql start

```



\## Create database user and database

Inside the container, execute:



```bash 

su - postgres -c "createuser -s root"

su - postgres -c "createdb testapp\_development"

```



\## Test Rails database connectivity

Now, migrate your database and start the Rails server:



```bash

rails db:migrate

rails server -b 0.0.0.0

```

Your Rails app should now be running at:

👉 `http://localhost:3000`



\## Notes



Installing PostgreSQL inside the container works for local testing but is not ideal for reusable or production setups:



Each new container will need to reinstall PostgreSQL.



The image size increases significantly.



Developers may prefer using an external database container or their local PostgreSQL instance.



This setup is fine for one-off testing, but for long-term or collaborative environments, use Docker Compose instead.

