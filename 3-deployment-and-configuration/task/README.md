# Table of Content

- [What to do](#what-to-do)
- [Sub-task 1: Liveness and Readiness probes](#sub-task-1-liveness-and-readiness-probes)
- [Sub-task 2: Secrets and config-maps](#sub-task-2-secrets-and-config-maps)
- [Sub-task 3: Deployment strategies](#sub-task-3-deployment-strategies)
- [Sub-task 4: Deployment history](#sub-task-4-deployment-history)

## What to do
In this module you will manage secrets and properties for your k8s objects and study deployment strategies.

## Sub-task 1: Liveness and Readiness probes
1. Add endpoints for health checks at your applications.
2. Add liveness and readiness probes for your deployment objects at k8s manifest (don't forget about database deployments).

## Sub-task 2: Secrets and config-maps
1. Add Secrets object to your k8s manifest to store database username and password.
2. Add config maps to store environment variables for application deployments.
3. Add sql scripts to init databases (create tables) to config maps.
4. Change k8s deployment objects to load these secrets and config-maps.

## Sub-task 3: Deployment strategies
In this module you will add a field to one of your services, and perform Rolling-update deployment.
1. To Post service add a new field `topic (:String)`. This is the topic for the post. You can specify it when creating a new post and when updating existing post. This field also should be returned at the responses for POST, PUT and GET operations.
2. Build a new docker image of application with changes and push it to the Docker Hub (specify another version of container).
3. Add Rolling-update deployment strategy to your deployments at manifest files and apply the  manifest, so the old versions of microservices are deployed and running.
4. Set app version of app containers to the new one and apply manifest one more time. Make sure that new changes are deployed.

## Sub-task 4: Deployment history
As you deployed a new version of your application, you can see the history of your deployments. Your task is to roll back to previous version of your deployment without changing your manifest files.
Put in comments the solution of this task.

