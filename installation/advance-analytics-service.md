# Advance Analytics Service
A service written in python using H2O.ai to do model creation and interaction

## Getting Started
These instructions will assist on getting the docker image startup

### Prerequisite
- Has access to giant container repository

### Installation (Docker)

```bash
docker run -d --name h2o
     -e GIANT_CONNECTION_URL=http://<giant-semantic-service-ip>:<giant-semantic-service-port>/connections/ 
     -p 12048:12048 -p 54321:54321 
     asia.gcr.io/fx-giant-container/giant-aanalytics-py:1.0.0

# To validate provided configurations is correctly being applied
curl localhost:12048
```

- port 12048: This port is the port that is being used by the service to accept the request to generate and interact with model

- port 54321: This port is the port that is being used to directly accessing the H2O.ai Flow UI

Note: the port 12048 is configured by the env.py inside the service. This port is not currently available to be changed using OS environment values
