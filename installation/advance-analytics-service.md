# Advance Analytics Service
A service written in python using H2O.ai to do model creation and interaction

## Getting Started
These instructions will assist on getting the docker image startup

### Prerequisite
- Has access to giant container repository
- Has a working mongo repository with survey data


### Installation (Docker)
```bash
docker run -d --name h2o
     -e GIANT_CONNECTION_URL=http://<giant-semantic-service-ip>:<giant-semantic-service-port>/connections/ 
     -p 12048:12048 -p 54321:54321 
     asia.gcr.io/fx-giant-container/giant-aanalytics-py:1.0.0

# To validate provided configurations is correctly being applied
curl localhost:12048
```
