# Usage
This is an nginx/lighttpd/apache2 WebDAV docker with basic auth functionality.

Via two environment variables basic authentication can be set:

	HTUSER
	HTPASSWORD

If either environment variable is missing, basic authentication is removed.

## Basic usage

	docker run -d --name webdav -p 80:80 -v "$PWD":/app:z docker.io/smoebody/webdav

this starts the container with nginx as server

## Advanced usage

	docker run -d --name webdav -p 80:80 -v "$PWD":/app:z docker.io/smoebody/webdav apache2

this starts the container with apache2 as server

	docker run -d --name webdav -p 80:80 -v "$PWD":/app:z docker.io/smoebody/webdav lighttpd

this starts the container with lighthttpd as server
