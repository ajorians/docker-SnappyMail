# docker-SnappyMail
A Docker image build of SnappyMail

To build (run as root): docker build -t snappymail .

You can run it with Docker-Compose file with:
docker-compose up -d

You should have a separate mail server running as this is just the WebUI for the mail server.

Your first time navigate to your site with ?admin

What that does is writes an admin_password.txt file but in order to get it you need to retrieve it out of your container.

You can do:
docker exec -it snappymail bash

And then it is at /srv/www/htdocs/data/_data_/_default_/admin_password.txt

You'll use username admin and that as your password (until you change it) to configure.

Hope that help!
