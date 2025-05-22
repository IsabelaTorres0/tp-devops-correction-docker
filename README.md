# TP DevOps Correction Docker
# Dev-Ops-1

## 1-1 For which reason is it better to run the container with a flag -e to give the environment variables rather than put them directly in the Dockerfile?
- It's better to add -e because that way we can protect our image if it's being uploaded or shared avoiding leackages, it give us more flexibility in the when running the image in diferent env.
## 1-2 Why do we need a volume to be attached to our postgres container?
- We use a volume so our data dosen't get distroyed, this way if the container get´s distroyed or upgraded our data will remain intact
- It creates an storage in the data so you can share it across containers

## 1-3 Document your database container essentials: commands and Dockerfile.
- POSTGRES_PASSWORD= pwd
- DATABASE_HOST= database
- DATABASE_PASSWORD= pwd

## 1-4 Why so we need a multistage blind?
We need it to make the process lighter and so we can eficientate process of creating an image
- also reduces image size,
- it makes it more fast and safe to deploy

## Explain each step
### Build stage
- Names the stage, and sets a working environment where we can work later on
- It later on install the needed packages and run the mvn package shiping the test practice
### Run stage
- It builds a jar file so we can run the file

## 1-5 Why do we need a reverse proxy?
- A reverse proxy helps you to run diferrent services at the same time, so it's possible to handle the HTTPS, db, app etc...

## 1-6 Why is docker-compose so important?
- helps you run several container applications at the same time while handeling your network and volumes

## 1-7 Document docker-compose most important commands.
- docker compuse up -d
- docker compose down
- docker compose build
- docker compose logs

## 1-10 Why do we put our images into an online repo?
That way we can acces it from diferrent containers and we can reference it or search it into our different environments

## 2-1  What are testcontainers?
This are Javalibraries that help you run the container during automated test

## 2-2  For what purpose do we need to use secured variables ?
This is because github is by default a public space where everyone can add their own info therefore if you want to add sensible information this way it would be protected and open to the public

## 2-3 Why did we put needs: build-and-test-backend on this job? Maybe try without this and you will see!
- It stops you from running a job if the backend build is failing or testing

## 2-4 For what purpose do we need to push docker images?
- that way we can access it remotly and between environments

## 3-1 Document your inventory and base commands
## 3-2 Document your playbook
## 3-3 Document your docker_container tasks configuration.


