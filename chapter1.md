# Installation

The Apinf platform is provided as a Docker image. Follow these steps to deploy tye Apinf Docker image.

## Install Docker

As a prerequisite, you will need to install Docker. Please ensure your system has an active Docker installation, by following the official [Docker installation instructions](https://docs.docker.com/engine/installation/).

## Run APInf container

    docker run -p 8080:80 -e MONGO_URL=mongodb://localhost:27017/your_db -e MAIL_URL=smtp://some.mailserver.com:25 -e ROOT_URL=`[`http://YOUR_SITE_DOMAIN`](http://YOUR_SITE_DOMAIN)`apinf/platform:latest

## Installation with Proxy \(API Umbrella\)

We have also prepared a Docker Compose image to aide with  installation of Apinf and an accompanying API proxy service \([API Umbrella](https://apiumbrella.io/)\). 

**Prerequisite**: You will need to [install Docker Compose](https://docs.docker.com/compose/install/).

To install the combined Apinf platform with proxy, follow these steps:

1. Create "docker-compose.yml" file on your server and copy content from [docker-compose.yml](https://github.com/apinf/api-umbrella-dashboard/blob/develop/docker-compose.yml).
2. In the same folder create file "docker/api-umbrella/config/api-umbrella.yml" based on example "docker/api-umbrella/config/api-umbrella.yml.example". 
   * **ATTENTION**: replace "example.com" on YOUR\_SITE\_DOMAIN for keys "ssl\_cert" and "ssl\_cert\_key".
3. Create file "docker/apinf/env" based on example "docker/apinf/env.example".
4. Create file "docker/ssl/env" based on example "docker/ssl/env.example".
5. Run `docker-compose up -d`. The first launch of will be slow because \(take couple of minutes\) of the DH parameter computation and configure Let's Encrypt certificate.

## Configure Apinf/proxy integration

In order to use the API Umbrella proxy through the Apinf platform user interface, follow these instructions:

1. Visit [https://YOUR\_SITE\_DOMAIN:3002/signup/](https://YOUR_SITE_DOMAIN:3002/signup/) and fill form for get API Key.
2. Visit [https://YOUR\_SITE\_DOMAIN:3002/admin/](https://YOUR_SITE_DOMAIN:3002/admin/) and click on 'My Account' link for find Admin API Token.
3. Visit [https://YOUR\_SITE\_DOMAIN/sign-up](https://YOUR_SITE_DOMAIN/sign-up) and create new account.
4. Fill data in "Settings for API Umbrella: APINF Configuration Wizard".
   * Host: "[https://YOUR\_SITE\_DOMAIN:3002](https://YOUR_SITE_DOMAIN:3002)"
   * API Key: from step \#1
   * Auth Token: from step \#2
   * Base URL: "[https://YOUR\_SITE\_DOMAIN:3002/api-umbrella/](https://YOUR_SITE_DOMAIN:3002/api-umbrella/)"
   * Elasticsearch: "[http://elasticsearch.docker:9200](http://elasticsearch.docker:9200)"



