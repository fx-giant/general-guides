# Survey Querying Service
A custom connector written in node to perform survey base query

## Getting Started
These instructions will assist on getting the docker image startup

### Prerequisite
- Has access to giant container repository
- Has a working mongo repository with survey data


### Installation (Docker)
```bash
sudo docker run -p {{port-number-use-80}}:3000 -d \
    --name survey-node \
    -e SURVEY_MONGODB_URL=mongodb://username:password@url:27017/Survey?authSource=admin \
    asia.gcr.io/fx-giant-container/tns-surveyservice-node:1.0

# To validate provided configurations is correctly being applied
curl localhost:{{port-number-use-80}}/api/configuration
```