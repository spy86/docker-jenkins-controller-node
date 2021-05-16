# Jenkins Continuous Integration and Delivery server.
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  [![Build Status](https://travis-ci.org/spy86/docker-jenkins-master-node.svg?branch=master)](https://travis-ci.org/spy86/docker-jenkins-master-node)
## List installed plugins      

| Name                       | Version |
|----------------------------|---------|
| ansicolor                  | Latest  |
| badge                      | Latest  |
| blueocean                  | Latest  |
| configuration-as-code      | Latest  |
| docker-workflow            | Latest  |
| github-branch-source       | Latest  |
| greenballs                 | Latest  |
| job-dsl                    | Latest  |
| kubernetes                 | Latest  |
| parameterized-trigger      | Latest  |
| pipeline-aws               | Latest  |
| pipeline-maven             | Latest  |
| pipeline-utility-steps     | Latest  |
| prometheus                 | Latest  |
| saml                       | Latest  |
| ssh-agent                  | Latest  |
| slack                      | Latest  |
| timestamper                | Latest  |
| workflow-aggregator        | Latest  |
| ansible                    | Latest  |
| permissive-script-security | Latest  |
| authorize-project          | Latest  |
| role-strategy              | Latest  |
| matrix-auth                | Latest  |


# How to use
### Basic usage
```shell
docker run -p 8080:8080 -p 50000:50000 spy86/docker-jenkins-controller-node:latest
```

### Jenkins with persistent volume (recommended)
```shell
docker run -p 8080:8080 -p 50000:50000 -v /your/home:/var/jenkins_home spy86/docker-jenkins-controller-node:latest
```

### Example docker-compose

```yaml 
version: '3'
services:
  jenkins-controller-node:
    image: spy86/docker-jenkins-controller-node:latest
    volumes:
      - /opt/jenkins_home:/var/jenkins_home
    ports:
      - "8080:8080"
      - "50000:50000"
```
