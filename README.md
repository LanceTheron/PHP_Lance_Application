PHPImagelance Application
Overview
This is a lightweight web application built using pure PHP, HTML, CSS, JavaScript, and Bootstrap. It runs on a Docker container with the php:7.4-apache image. This guide will walk you through how to run the application with minimal setup using Docker.

Prerequisites
Docker installed and running
Command line access (Terminal or Command Prompt)
Running the Application
Pull the Docker Image (Optional):
If the image is hosted on Docker Hub, you can pull it using:

docker pull <your-dockerhub-username>/phpimagelance

Run the Docker Container:
Use the following command to run the container on port 2000:

docker run -d -p 2000:80 --name phpimagelance-container phpimagelance

Explanation:

-d runs the container in detached mode.
-p 2000:80 maps the container’s port 80 to your computer's port 2000.
--name phpimagelance-container gives the container a meaningful name.
Verify the Container is Running:
Check if the container is running by using:

docker ps

Access the Application:
Open a browser and go to:

http://localhost:2000

Managing the Container
Stop the container: docker stop phpimagelance-container
Restart the container: docker start phpimagelance-container
Remove the container: docker rm phpimagelance-container
Technologies Used
PHP (7.4-apache):
The backend logic is built in PHP. Apache serves as the web server to deliver the PHP content to the browser.

HTML and CSS:
HTML provides the structure of the web pages, and CSS is used to style the pages for better presentation.

Bootstrap:
Bootstrap ensures that the application has a responsive design, meaning it will adapt to different devices and screen sizes.

JavaScript:
JavaScript adds interactivity, such as form validation or dynamic content updates, for an enhanced user experience.

Why These Technologies Were Chosen
Pure PHP keeps the application lightweight and easy to maintain without relying on frameworks.
HTML, CSS, and JavaScript offer a simple and effective way to create an interactive user interface.
Bootstrap ensures the design remains consistent across various devices.
Docker packages the entire application and its dependencies to ensure it runs consistently across different environments.
Troubleshooting
Port 2000 Not Accessible:
Ensure Docker is running and no other application is using port 2000. If needed, change the port by running:
docker run -d -p 3000:80 --name phpimagelance-container phpimagelance

Check Logs for Errors:
Use the command: docker logs phpimagelance-container

Verify the Container Status:
Ensure the container is running by using: docker ps
