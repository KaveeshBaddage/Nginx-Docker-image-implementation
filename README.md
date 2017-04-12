# Nginx-Docker-image-implementation

*Create a Dockerfile

	FROM nginx:1.10.1-alpine
	MAINTAINER kbaddage98@gmail.com
	COPY ./nginx.conf  /etc/nginx/nginx.con

*Create a directory src with the following content in index.html

	<html>
	<body>
	<p> Hello nginx docker</p>
	</body>
	</html>

*Your directory should look like this

$ Nginx .
.
├── Dockerfile
├── nginx.conf  
└── src
    └── index.html


Create a Docker image using nginx:1.10.1-alpine

	sudo docker build -t my-nginx:1.0 .

This will create a my-nginx:1.0 image.

View docker images

	sudo docker images

Create a Docker Container running this image

 	sudo docker run --name my-nginx -d -p 80:80 -v /home/kaveesh/Desktop/NginX/src:/usr/share/nginx/html:ro my-nginx:1.0

Open browser of the host at http://localhost:80, you will see the website up and running

View running containers

	sudo docker ps
