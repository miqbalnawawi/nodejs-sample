# NODE-JS-DOCKER-SAMPLE

[![Build Status](https://badgen.net/badge/docker/containers/blue?icon=docker)](https://www.docker.com/)
[![Build Status](https://badgen.net/badge/Node/JS/green)](https://nodejs.org/en)

This repository contains a simple Node.js application that is deployed using Docker, allowing for consistent and isolated execution across different environments. Docker simplifies the process of packaging applications and their dependencies into containers, ensuring a seamless experience from development to deployment.

## Prerequisites

Before you begin, ensure you have the following software installed on your system:

- [Docker](https://www.docker.com/) - Docker

## Getting Started

Follow these steps to set up and run the Node.js application using Docker:
 1. **Clone the Repository**: Start by cloning this repository to your local machine:
    ```sh
    git clone https://github.com/chisomije92/node-js-docker-sample.git
    cd node-js-docker-sample
    ```
2. **Build the Docker Image**: Build the Docker image using the provided **Dockerfil**e:
    ```sh
   docker build -t node-js-docker .
    ```
3. **Run the Docker Container**: Once the image is built, run a Docker container based on that image:
     ```sh
   docker run -p 3000:3000 -d nodejs-docker
    ```
    This will start the Node.js application in the container and map port 3000 from the container to port 3000 on your host machine.

4. **Access the Application**: Open your web browser and navigate to `http://localhost:3000` to access the running Node.js application.

## Customization

Feel free to customize the application to your needs. You can modify the source code in the `server.js` file. After making changes, you'll need to rebuild the Docker image and restart the container:

1. Modify the code in the `server.js` file or/and add your own folders/directory.
2. Rebuild the Docker image:
    ```sh
   docker build -t node-js-docker .
    ```
3. Stop the existing container:
     ```sh
    docker stop <container_id>
    ```
4. Run a new container using the updated image (repeat step 3 from the "Run the Docker Container" section).




## Cleanup

When you're finished using the application, you can clean up by stopping and removing the Docker container and image:

1. Stop the running container:
    ```sh
    docker stop <container_id>
    ```

2. Remove the container:

    ```sh
    docker rm <container_id>
    ```

3. Remove the Docker image:

    ```sh
    docker rmi nodejs-docker-app
    ```



## Conclusion

Congratulations! You've successfully deployed a Node.js application using Docker. This approach makes it easy to share, deploy, and manage your application in various environments while maintaining consistency. If you have any questions or run into issues, please refer to the official Docker documentation or reach out for assistance.

Happy coding! 🚀



