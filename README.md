# go-api-template
Template repository for a Go API app with Docker and `air` hot reloading and `dlv` debug server pre-configured.

# What to do

1. Clone the repo
2. Change module name in go.mod
3. Adjust port numbers in docker-compose.yml

# Production build

1. Take a look at `etc/prod/Dockerfile`
2. Build it: `docker build -t [your:tag] -f etc/prod/Dockerfile .`
