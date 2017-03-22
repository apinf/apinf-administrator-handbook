# Installation

The Apinf platform is provided as a Docker image. Follow these steps to deploy tye Apinf Docker image:



## Run APInf container 
```docker run -p 8080:80 -e MONGO_URL=mongodb://localhost:27017/your_db -e MAIL_URL=smtp://some.mailserver.com:25 -e ROOT_URL=http://YOUR_SITE_DOMAIN apinf/platform:latest```



