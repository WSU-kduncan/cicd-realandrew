# Project 6

This is my repo of my Project 6 for CEG-3120. The project focuses on CI & CD (namely Docker and GitHub actions).

## Part 1

To setup and run the project follow these steps:

  1. Install Docker. These instructions are specific to Ubuntu (though for WSL2/Windows you can just download Docker Desktop, which is what I used for this project since I already had it installed for my personal Docker projects I've worked on). If you are using a different system, you can find instructions online to install Docker on almost any system.
      1. Remove any existing Docker packages using `sudo apt-get remove docker docker-engine docker.io`
      2. Update your packages with `sudo apt-get update`
      3. Install Docker with `sudo apt install docker.io`
      4. Install dependencies with `sudo snap install docker` or `sudo apt install docker`
  2. Build the Docker file. Open a terminal to the root of the project and run `docker build -t ceg3120_project6 .` which builds the local Dockerfile to an image and stores it under the name "ceg3120_project6", feel free to name it whatever you'd like.
  3. Run the image with `docker run -dp 80:80 --name project6 ceg3120_project6`
  4. With the project running you can go to [http://localhost:80](http://localhost:80) or [http://127.0.0.1:80](http://127.0.0.1:80) in your browser to view the website.

## Part 2
