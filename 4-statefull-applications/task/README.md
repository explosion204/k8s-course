# Table of Content

- [What to do](#what-to-do)
- [Sub-task 1: Persistent volumes](#sub-task-1-persistent-volumes)
- [Sub-task 2: Helm charts](#sub-task-2-helm-chart-default-variables)
- [Sub-task 3: Helm chart helpers](#sub-task-3-helm-chart-helpers)

## What to do
In this module you will learn how to attach persistent storages to your applications. Also, you will understand how helm charts work. 

## Sub-task 1: Persistent volumes
In this subtask you will make your database pods use local storage. This will ensure that no database data is lost during pod deploy/redeploy.
1. Add StorageClass and Local PersistentVolume objects for the Database pods to the manifest files. Persistent volume should reference local directory on your computer.
2. Add PersistenceVolumeClaim objects to your manifest and reference them from database deployment objects.

## Sub-task 2: Helm chart default variables
1. Install helm [Official download link](https://helm.sh).
2. Add helm chart to deploy your applications. Make replica-count and namespace a helm values.
3. Add helm values file to store default values for helm variables.
4. Run helm using `helm install` command to deploy applications with default helm variables. Make sure, your applications are up and running.
5. Run helm once again, but this time set namespace and replica-count for `helm intall` to non-default values.

## Sub-task 3: Helm chart helpers
1. Create helm `_helpers.tpl` file and define next labels there: 
   - current date : use helm generator for it's value
   - version
2. Make config-map use values as labels from helm `_helpers.tpl` file.