# Installation

The Apinf platform is provided as a Docker image. Follow these steps to deploy tye Apinf Docker image.

## Run APInf container

docker run -p 8080:80 -e MONGO\_URL=mongodb://localhost:27017/your\_db -e MAIL\_URL=smtp://some.mailserver.com:25 -e ROOT\_URL=http://YOUR\_SITE\_DOMAIN apinf/platform:latest



