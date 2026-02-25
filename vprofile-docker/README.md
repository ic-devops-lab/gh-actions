# Prerequisites

## Dependencies
- JDK 21
- Maven 3
- MySQL 8

## Technologies
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch

## Database
Here,we used Mysql DB
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql

## Infractructure

- `AWS ECR` repository: `vpro-app`
- `IAM user` for using ECR repo (`AmazonEC2ContainerRegistryFullAccess`): `gh-actions-ecr`
- `CLI Access keys` for `gh-actions-ecr` user saved in the GitHub repo secrets
- `GitHub` repo `environment secrets` for `AWS Acces Key`

  GitHub repo -> Settings -> Secrets and variables -> Secrets -> Environment secrets -> \
  Manage environments secrets -> production -> Environment secrets -> Add environment secret -> \

  Add 2 secrets: `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`

- 'GitHub environment variables' for
  - AWS region, where AWS ECR repo was created: `AWS_REGION`
  - AWS ECR repository name: `AWS_ECR_REPOSITORY_NAME`
