# Promts example

|NAME|PROMPT|DESCRIPTION|EXAMPLE|
|----|------|-----------|-------|
|app.yaml|Create an nginx deployment with 3 replicas|Simple pod|[app.yaml](./app.yaml)|
|app-livenessProbe.yaml|Create an nginx deployment with 3 replicas and liveness probes|Liveness probe for pod|[app-livenessProbe.yaml](./app-livenessProbe.yaml)| 
|app-readinessProbe.yaml|Create an nginx deployment with 3 replicas include liveness and readiness probes|Readiness and liveness probes|[app-readinessProbe.yaml](./app-readinessProbe.yaml)|
|app-volumeMounts.yaml|Create an nginx deployment with 3 replicas include liveness and readiness probes and vlume mounts. Also proved comments in yaml|Adds mount of emptyDir|[app-volumeMounts.yaml](./app-volumeMounts.yaml)|
|app-cronjob.yaml|Create cronjob manifest to export all RBAC users and send via email monthly|Cronjob example|[app-cronjob.yaml](./app-cronjob.yaml)|
|app-job.yaml|Create job to email log configuration for pods in default namespace|kind: Job|[app-job.yaml](./app-job.yaml)|
|app-multicontainer.yaml|Create an multiconteiner deployment with nginx and log exporter containers include liveness and readiness probes and vlume mounts. Also proved comments in yaml|Multicontainer deployment|[app-multicontainer.yaml](./app-multicontainer.yaml)|
|app-resources.yaml|Create an multiconteiner deployment with nginx and log exporter containers include liveness and readiness probes and vlume mounts and limit resources for containers. Provide comments in yaml|Resource limits example|[app-resources.yaml](./app-resources.yaml)|
|app-secret-env.yaml|Create secret example. Provide comments in yaml|kind: Secret|[app-secret-env.yaml](./app-secret-env.yaml)|

# AI integration
Using https://github.com/sozercan/kubectl-ai
## Preparation
```
read -s OPENAI_API_KEY
export OPENAI_API_KEY
export OPENAI_DEPLOYMENT_NAME=gpt-4o-mini
```
## Examples
```
k ai "Create an nginx deployment with 3 replicas include liveness and readiness probes and vlume mounts. Also proved comments in yaml" --raw | tee app-volumeMounts.yaml
```