## Docker-Compose-API

This project demonstrates a Node.js application with Prisma ORM, running a PostgreSQL database, set up using three different methods: Manual Installation, Docker, and Docker Compose. Below are the step-by-step instructions for each method, along with explanations.

## Overview

This project, `docker-compose-api`, demonstrates my journey of building a Node.js application with Prisma ORM and a PostgreSQL database using three different approaches: Manual Installation, Docker, and Docker Compose.


- **Manual Installation**:
  - Installed Node.js locally and cloned the repository.<br>

![image](https://github.com/user-attachments/assets/3567da7a-58a1-4671-82a8-5f5fb564e915)

![image (1)](https://github.com/user-attachments/assets/185358da-dcf2-4102-a67a-8bbb5af44b40)

  - Set up a PostgreSQL container with `docker run`.
  - Created a new database on [neon.tech](https://neon.tech).
  - Updated the `.env` file with database credentials.
  - Ran `npx prisma migrate dev`, `npx prisma generate`, `npm run build`, and `npm run start`.

![image (2)](https://github.com/user-attachments/assets/7248d290-0dce-48cd-9b9a-f6606d0dd62a)


  **Explanation**: This method requires manual setup of Node.js, database, and environment variables. It’s straightforward but time-consuming and less portable.


- **Docker Approach**:
  - Installed Docker and created a custom network with `docker network create user_project`.

![image (4)](https://github.com/user-attachments/assets/c7afdda0-a5cc-45a6-b1e0-e5daf7d97bdd)

  - Launched a PostgreSQL container and built a Docker image with `docker build --network=host -t user-project .`.

 ![image (3)](https://github.com/user-attachments/assets/ab1779ea-fbbc-4c93-9544-c818ea31153e)

  - Ran the container with `docker run`.

![image (5)](https://github.com/user-attachments/assets/d6fbc8c1-6a8f-485e-ad08-0a3d4e913278)

![image (6)](https://github.com/user-attachments/assets/3e181326-74ea-4158-85b1-8a5022b6395a)

    
  **Explanation**: Docker simplifies dependency management by containerizing the app and database. The network ensures communication between containers, and the build step creates a custom image.


- **Docker Compose Approach**:
  - Installed Docker and Docker Compose.
  - Used a `docker-compose.yml` file and ran `docker-compose up`.

![image (7)](https://github.com/user-attachments/assets/d1d96054-a062-40d2-bd83-b288d94dcc26)
  
  - Experienced automatic building and running of PostgreSQL and app services in seconds.

![image (8)](https://github.com/user-attachments/assets/2250bb94-df3e-4945-8c1a-df9010d28f2e)
    
  - Found it to be the most efficient method, saving significant setup time.

![image (9)](https://github.com/user-attachments/assets/c585c47f-db44-441d-9dfa-7d2c69d63aac)


**Explanation**: Docker Compose automates the process by defining services in a docker-compose.yml file. It builds and runs the app and database in one command, saving time and ensuring consistency.


This evolution reflects my learning from manual setup to automated deployment, with Docker Compose proving the most effective. For detailed contribution steps, check the `CONTRIBUTE.md` file.


### Conclusion

The Docker Compose method is the most efficient, as it automates the build and run process in seconds, reducing manual steps. Use the manual method for local testing or when Docker isn’t available, and the Docker method for a balance between control and containerization.
