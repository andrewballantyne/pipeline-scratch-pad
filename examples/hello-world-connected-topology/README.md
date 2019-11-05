# Hello World Connected To Topology Example

A single pipeline, single task example to echo out hello world. It contains a hook to tie into a topology instance so it can have the progress displayed in the Topology screen.

## Prerequisites

Add a deployment or deployment config to your project.

1. Click the "+Add" navbar link
2. Click "From Git" tile
3. Fill in a git repo (consider using https://github.com/nodeshift-starters/react-web-app)
4. Select "Modern Webapp" as the Builder
5. Make sure the "Name" field has "react-web-app"

## Create a project to work in

Create a new project (which is auto selected) so we can a new space to work in:

```
$ oc new-project tutorial-hello-world
```

*Note:* This project name is not used after this step, `oc` maintains the selection for the following steps; so feel free to change it.


## Create the Task

Create the [hello-world task](task.yaml) that exists in this folder.

```
$ oc create -f ./task.yaml
```

View that it was created:

```
$ tkn task ls
NAME          AGE
hello-world   7 seconds ago
```


## Create the Pipeline

Create the [hello-world pipeline](pipeline.yaml) that exists in this folder. It contains the label necessary to connect to the topology instance.

```
$ oc create -f ./pipeline.yaml 
```

View that it was created:

```
$ tkn pipeline ls
NAME                             AGE             LAST RUN                      STARTED      DURATION     STATUS
hello-world-connected-topology   5 seconds ago   ---                           ---          ---          ---
```
