# Cluster Mock App

This example is for testing with ClusterTasks.

## Create Workload with Pipelines

ClusterTasks are useful for when we want to copy a pipeline and connect it with a workload as it's created.

There `pipeline.yaml` file is a template with no connection for the workload + pipeline flow. However, the other pipelines listed here are setup to use the same ClusterTasks as `pipeline.yaml` but also come with a label to connect to the import/create workload flow via a specific builder image or through the dockerfile import flow.
