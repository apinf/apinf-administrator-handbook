# Installation

The Apinf platform is provided as a Docker image. Follow these steps to deploy tye Apinf Docker image.

## Install Docker

As a prerequisite, you will need to install Docker. Please ensure your system has an active Docker installation, by following the official [Docker installation instructions](https://docs.docker.com/engine/installation/).

## Run APInf container

`docker run -p 8080:80 -e MONGO_URL=mongodb://localhost:27017/your_db -e MAIL_URL=smtp://some.mailserver.com:25 -e ROOT_URL=`[`http://YOUR_SITE_DOMAIN`](http://YOUR_SITE_DOMAIN)`apinf/platform:latest`

