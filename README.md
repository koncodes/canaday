# WordPress Docker Environment

## Setup
1. Create a new branch to keep this "starter" clean.
2. Review and update the docker-compose file. Make sure to change the database volume for each different site.
3. Create environment file and update variables.
    ```shell
   cp .env.example .env
    ```
4. Execute the docker-compose.yml the .env file:
   ```shell
   docker compose up -d
   ```
5. Setup WordPress @ <http://localhost/>


### WordPress
<http://localhost>

### phpMyAdmin
<http://localhost:8081>

### MailHog
<http://localhost:8025>

## GIT COMMANDS

1. First pull other person's work from develop branch into your branch. 
   ```shell
   git switch katherine
   ```
      ```shell
   git pull origin develop
   ```
2. Start working. 
3. Add your edits to your branch.
   ```shell
   git add .
   ```
4. Commit your edits. 
   ```shell
   git commit -m "Your edit message"
   ```
5. Push your edits
   ```shell
   git push origin katherine
   ```
6. Push your edits to develop for the other person to pull later
   ```shell
   git switch develop
   ```
   ```shell
   git merge katherine
   ```
   ```shell
   git push origin develop
   ```

## WP CLI
You can run a single command:
```shell
docker exec -it docker-dock-it-wpcli-1 wp user list
```
or login via the terminal:
```shell
docker exec -it docker-dock-it-wpcli-1 bash
```
or open the WPCLI terminal in Docker Desktop