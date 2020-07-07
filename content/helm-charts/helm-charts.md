# Helm Charts
A helm chart is organized as a collection of files inside of a directory.

## Helm
Helm is a tool for managing Charts. Helm Charts are packages of pre-configured Kubernetes resources.

Use Helm to:

1. Create new charts from scratch
2. Package charts into chart archive (tgz) files
3. Interact with chart repositories where charts are stored
4. Install and uninstall charts into an existing Kubernetes cluster
5. Manage the release cycle of charts that have been installed with Helm

## Charts
Helm uses a packaging format called charts. A chart is a collection of files that describe a related set of Kubernetes resources. A single chart might be used to deploy something simple, like a memcached pod, or something complex, like a full web app stack with HTTP servers, databases, caches, and so on. Charts are created as files laid out in a particular directory tree. They can be packaged into versioned archives to be deployed.

### Why use Helm Charts

1. Helm Charts help define, install, and upgrade even the most complex Kubernetes application.
2. Helm charts can contain any number of Kubernetes objects, all of which are deployed as part of the chart. 
3. Helm charts usually contain a Deployment and a Service, but it can also contain an Ingress, Persistent Volume Claims, or any other Kubernetes object.
4. Helm charts are used to deploy an application, or one component of a larger application. 
5. Helm Charts describe even the most complex apps, provide repeatable application installation, and serve as a single point of authority.
6. Take the pain out of updates with in-place upgrades and custom hooks.
7. Charts are easy to version, share, and host on public or private servers.

## Installing Helm and Helm Charts

### Helm
Check [here](https://helm.sh/docs/intro/) for basic Helm installation directions.

### Helm Charts
After installing Helm, you can easily install helm charts from the official repository using the following command
`helm install stable/chart_name`

## Helm Charts File Structure
A helm chart is organized as a collection of files inside of a directory.

Inside of this directory, Helm will expect a structure that matches this:
```
application/
  Chart.yaml          # A YAML file containing information about the chart
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart
  README.md           # OPTIONAL: A human-readable README file
  values.yaml         # The default configuration values for this chart
  values.schema.json  # OPTIONAL: A JSON Schema for imposing a structure on the values.yaml file
  charts/             # A directory containing any charts upon which this chart depends.
  crds/               # Custom Resource Definitions
  templates/          # A directory of templates that, when combined with values,
                      # will generate valid Kubernetes manifest files.
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes
```
Helm reserves use of the charts/, crds/, and templates/ directories, and of the listed file names. Other files will be left as they are.

## Chart.yaml File Structure
The `Chart.yaml` file is required for a chart. It contains the following fields:
```
apiVersion: The chart API version (required)
name: The name of the chart (required)
version: A SemVer 2 version (required)
kubeVersion: A SemVer range of compatible Kubernetes versions (optional)
description: A single-sentence description of this project (optional)
type: The type of the chart (optional)
keywords:
  - A list of keywords about this project (optional)
home: The URL of this projects home page (optional)
sources:
  - A list of URLs to source code for this project (optional)
dependencies: # A list of the chart requirements (optional)
  - name: The name of the chart (nginx)
    version: The version of the chart ("1.2.3")
    repository: The repository URL ("https://example.com/charts") or alias ("@repo-name")
    condition: (optional) A yaml path that resolves to a boolean, used for enabling/disabling charts (e.g. subchart1.enabled )
    tags: # (optional)
      - Tags can be used to group charts for enabling/disabling together
    enabled: (optional) Enabled bool determines if chart should be loaded
    import-values: # (optional)
      - ImportValues holds the mapping of source values to parent key to be imported. Each item can be a string or pair of child/parent sublist items.
    alias: (optional) Alias to be used for the chart. Useful when you have to add the same chart multiple times
maintainers: # (optional)
  - name: The maintainers name (required for each maintainer)
    email: The maintainers email (optional for each maintainer)
    url: A URL for the maintainer (optional for each maintainer)
icon: A URL to an SVG or PNG image to be used as an icon (optional).
appVersion: The version of the app that this contains (optional). This needn't be SemVer.
deprecated: Whether this chart is deprecated (optional, boolean)
annotations:
  example: A list of annotations keyed by name (optional).
```

## How to use 
Click [here](https://helm.sh/docs/intro/using_helm/) to learn how to use helm charts.


## Resources 
- Official Helm Website - https://helm.sh/
- Official GitHub Repo  - https://github.com/helm/charts
- YouTube Video         - https://youtu.be/-ykwb1d0DXU

## Pain Points 
The Helm Charts are not completely stable and major changes are expected that may disrupt the existing projects.
