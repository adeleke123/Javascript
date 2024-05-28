# Hello World App

This is a simple Dockerized Node.js application that serves a "Hello World" message.

## How to Run

# To run this application using Docker:

# Pull the image from Docker Hub:
- docker pull bakare1234844/node-app

# Run the Docker container:
- docker run -p 3000:3000 bakare1234844/node-app

- The application will be accessible at http://localhost:3000

- [Link to Docker Hub Repository](https://hub.docker.com/repository/docker/bakare1234844/node-app/general)


**Project Description**

- This project is a simple Node.js web application that runs on Express.
- It has been containerized using **Docker** and deployed to **Heroku.**
- The application responds with "Hello, World!" when accessed via the root URL.

**Steps Taken:**

- **Created a Node.js application:** Developed a simple Express server in **main.js**.
- **Containerized the application:** Created a **Dockerfile** to build a Docker image for the **Node.js app**.
- **Deployed to Heroku:**
  - Created a new Heroku app using the **Heroku CLI**.
  - Configured Heroku to use the Dockerfile for deployment.
  - Pushed the application code to Heroku, which built and deployed the Docker container.

Dockerfile:
----------
```
# Use the official Node.js image as a base
FROM node:20

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 3000

# Define the command to run the app
CMD ["node", "main.js"]

```
**Running Application:**

- You can access the running application via this [link:](https://leke-node-app-c257cbbe91fc.herokuapp.com/)

**Push the README.md to your repository**:
```
git add README.md
git commit -m "Add project description"
git push
```
