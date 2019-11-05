# Empty Pipeline Example

Although not very helpful, a pipeline can have no tasks and render properly in the UI. This is the use-case of that scenario.

## Create a project to work in

Create a new project (which is auto selected) so we can a new space to work in:

```
$ oc new-project tutorial-hello-world
```

*Note:* This project name is not used after this step, `oc` maintains the selection for the following steps; so feel free to change it.

## Create the Pipeline

Create the [no-task pipeline](pipeline.yaml) that exists in this folder.

```
$ oc create -f ./no-task-pipeline.yaml 
```

View that it was created:

```
$ tkn pipeline ls
NAME               AGE              LAST RUN   STARTED   DURATION   STATUS
no-task-pipeline   22 seconds ago   ---        ---       ---        ---
```
