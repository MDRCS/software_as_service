# software_as_service
SAAS APPLICATION USING FLASK, Postgres, REDIS, RabbitMQ, Coupons System ,Admin Panel etc ..

```
User Accounts              |	    How to Plan an Application
Database Schemas           |	    Database Queries
Jinja Templates            |	    Code Analysis
Python 2 / 3 Compatibility |	    Writing Tests
Dependency Management      |	    Flask App Factory Pattern
Application Configuration  |	    Flask Blueprints
Flask Extensions           |	    CLI Scripts
Logging                    |	    Debugging
Sending Email              |	    Form Validation / Submissions
AJAX Requests              |	    JSON Responses
Background Workers         |	    Rate Limiting
Docker                     |	    Docker Compose
Secure Tokens              |	    Custom Admin Dashboard
Pagination                 |	    Template Macros
Generating Fake Data       |	    Searching and Sorting Data
Profiling                  |	    Middleware
Custom Error Pages         |	    Exception Handling
Routing                    |	    Stripe Integration
Microtransactions          |	    Recurring Billing
Invoicing                  |	    Coupon Codes
Design Patterns            |	    Data Modeling
Subscription Management    |	    Receiving Webhooks
Database Migrations        |	    Internationalization (i18)
Password Reset Workflow    |	    Authentication and Authorization
CSRF Protection            |	    Twitter Bootstrap v4
Webpack	ES6                |        Javascript / SCSS
```

### + Docker - Recommendation  :

```
The official Docker Python image in its slim variant—e.g. python:3.8-slim-buster—is a good base image for most use cases.
it’s 60MB when downloaded, 180MB when uncompressed to disk, it gives you the latest Python releases,
and it’s got all the benefits of Debian Buster.

```

+ Bash Commands :
```
1- docker build -t snakeeyes:latest . # build an app based on `Dockerfile`, the dot . mean the app project is in this directory
2- docker images # dispay images
3- docker ps    # display all container running
4- docker kill 40d430274069 # kill a docker build
5- docker-compose up --build # Build and start everything with Docker Compose
6- docker-compose stop # stop docker image
7- ls -al # show all files even the hidden ones.
8- docker-compose ps
9- docker-compose rm -f
10- docker-compose exec website py.test snakeeyes/tests
11- docker network ls # View your Docker networks
12- docker-compose exec website snakeeyes routes
```

```
# Remove "dangling" images
docker rmi -f $(docker images -qf dangling=true)
```
```
# Run the test coverage tool
docker-compose exec website py.test --cov-report term-missing --cov snakeeyes
```
```
Performing Static Analysis on the Code Base
# Run the flake8 tool
docker-compose exec website flake8 .
```



```
- DATABASE POSTGRES.
    + Reset and seed the database
    + The database schema changed since the last section, so we need to do this.

docker-compose exec website snakeeyes db reset --with-testdb
docker-compose exec website snakeeyes add all

### Migration - Alembic :
docker-compose exec website alembic upgrade head
```
