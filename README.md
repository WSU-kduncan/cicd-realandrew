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

1. Create a Docker Hub account (if you don't already have one) at [https://hub.docker.com](https://hub.docker.com).
2. Create a new repository by clicking the big blue "Create Repository" in the top right of the screen. Give it an appropriate name, set it to public, and click the blue "create" button.
3. Login to Docker Hub in your CLI by typing `docker login` and entering your credentials (or `docker login --username <username>` if you need to login to a different account).
4. On your repository, set 2 Github secrets, set `DOCKER_USERNAME` equal to your Docker Hub username and set `DOCKER_PASSWORD` equal to your Docker Hub password.
5. In the `.github\workflows\docker-push.yml` file set `images` under `with` to `username/reponame` using your Docker Hub user name and repository name.
