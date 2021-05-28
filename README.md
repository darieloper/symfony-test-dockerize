# symfony-test-dockerize
Symfony Test Dockerize

### Steps to start working
1. `git clone --recursive https://github.com/darieloper/symfony-test-dockerize.git` (Clone the docker repo and symfony project submodule)
2. `cd symfony-test-dockerize/` (Open directory to start working on docker commands)
3. `sudo docker-compose up -d --build` (Build the containers and start them)

> In case that all the containers was started successfully, You can start one by one with this command `sudo docker container start <container-id> -a`

4. `sudo docker exec -it <php-container-id> bash` (Open a bash inside the php container to start runing php commands)
5. `composer install` (Install all php dependencies)
6. `php bin/console doctrine:database:create` (Create database)
7. `php bin/console doctrine:migrations:migrate --no-interaction` (Run migrations to create the tables)
8. `php bin/console doctrine:fixtures:load --no-interaction` (Populate the Tags table)
9. `php bin/phpunit` (Run the PHPUnit tests)

> Now you are ready, visit this [link](http://localhost:8081/) to start
