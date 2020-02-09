# Example of Traefik 2.x and Portainer for local Development

Traefik 2.0 is not backwardly compatible to Traefik 1.0 and as of this writing there are not a lot of examples using Traefik 2.0.

## What does this do?
Traefik is a container aware reverse proxy that can instantaneously create route to containers using the labels on a container as configuration. There are many other capabilities of Traefik that you can explore [here](https://docs.traefik.io/). For the purpose of this example, Traefik will allow us to run multiple container and reach those containers by a URL instead of having to setup multiple exposed ports on your local environment.

Portainer is an open source container management package that is a replacement for Docker EE UCP and in my humble opinion, far better. Portainer will allow you to quickly and easily manage your containers and stacks running on your local environemnt.

The docker-compose stack detailed here is very simliar to some production environments that use Traefik and gives a developer a close-to-production environment to work in.

## How to use
Fork this repo to use as a template. Once forked edit the `.env` file for your preferences then start adding your services to the compose file. Follow the pattern in the Portainer service to expose other services through Traefik

## Notice
The setup defined here is insecure and should only be used on your local machine. Even then be warned that it freely opens upcontrol to your local Docker engine. If you are working on public wifi you should protect your ports via a firewall.
