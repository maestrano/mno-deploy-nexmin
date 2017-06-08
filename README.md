# Minimal Ansible Configuration for deploying Nex!™
This project provides the minimal configuration set required to setup Nex!™ using the [mno-deploy Ansible framework](https://github.com/maestrano/mno-deploy).

## Context
This repository assumes a project called **nexmin** is to be deployed to two environments: uat and production. You can use this repository as boilerplate configuration to bootstrap your own configuration repository (just search and replace **nexmin** by your own project name).

## Important Note
The nexmin_prd_secrets.yml and nexmin_uat_secrets.yml are here unencrypted for educational purpose. In real life these two files must be encrypted using the `ansible-vault encrypt` command.

## Prerequisites
You must be familiar with the mno-deploy deployment process. This repository is not used directly by servers to configure themselves. This repository is instead built into an archive file (e.g. by a service like codeship) and pushed to a remote bucket (only AWS S3 supported at this stage). The configuration package is then fetched by instances - typically inside an auto-scaling group - along with the mno-deploy framework to (re)configure themselves.

See this [wiki entry for more information](https://maestrano.atlassian.net/wiki/display/ENTDESK/Deployments+using+Rundeck).
