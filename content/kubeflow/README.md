# Kubeflow

What is Kubeflow?
The Kubeflow project is dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable. It provides a straightforward way to deploy best-of-breed open-source systems for ML to diverse infrastructures. Anywhere you are running Kubernetes, you should be able to run Kubeflow. The Kubeflow project comes with many
various components that can be used to deploy a ML pipeline end to end.

The following diagram shows Kubeflow as a platform for arranging the components of your ML system on top of Kubernetes:
![Fig 1: Kubeflow](/content/kubeflow/kubeflow.PNG)

# Useful components
## Central Dashboard
The Dashboard is a UI that provides access to some components of kubeflow such as server for jupyter notebooks and pipelines.

## Jupyter Notebook Server
This is where data scientists can access Jupyter Notebooks which is a tool used to work on creating ML models. Advantages of having a notebook server on kubeflow are as follows:
-Integrates well with the rest of the infrastructure with respect to authentication and access control.
-Enables easier notebook sharing across the organization. Users can create notebook containers or pods directly in the cluster, rather than locally on their workstations. Admins can provide standard notebook images for their organization, and set up role-based access control (RBAC), Secrets and Credentials to manage which teams and individuals can access the notebooks.

## Fairing
Kubeflow Fairing is a Python package that makes it easy to train and deploy ML models on Kubeflow. Kubeflow Fairing can also been extended to train or deploy on other platforms. Currently, Kubeflow Fairing has been extended to train on Google AI Platform.

Kubeflow Fairing packages your Jupyter notebook, Python function, or Python file as a Docker image, then deploys and runs the training job on Kubeflow or AI Platform. After your training job is complete, you can use Kubeflow Fairing to deploy your trained model as a prediction endpoint on Kubeflow.

The following are the goals of the Kubeflow Fairing project:

-Easily package ML training jobs: Enable ML practitioners to easily package their ML model training code, and their code’s dependencies, as a Docker image.
-Easily train ML models in a hybrid cloud environment: Provide a high-level API for training ML models to make it easy to run training jobs in the cloud, without needing to understand the underlying infrastructure.
-Streamline the process of deploying a trained model: Make it easy for ML practitioners to deploy trained ML models to a hybrid cloud environment.

## Kubeflow pipelines
A pipeline is a description of an ML workflow, including all of the components in the workflow and how they combine in the form of a graph. (See the screenshot below showing an example of a pipeline graph.) The pipeline includes the definition of the inputs (parameters) required to run the pipeline and the inputs and outputs of each component.

After developing your pipeline, you can upload and share it on the Kubeflow Pipelines UI.

A pipeline component is a self-contained set of user code, packaged as a Docker image, that performs one step in the pipeline. For example, a component can be responsible for data preprocessing, data transformation, model training, and so on.

The following are the goals of Kubeflow Pipelines:
End-to-end orchestration: enabling and simplifying the orchestration of machine learning pipelines.
Easy experimentation: making it easy for you to try numerous ideas and techniques and manage your various trials/experiments.
Easy re-use: enabling you to re-use components and pipelines to quickly create end-to-end solutions without having to rebuild each time.

## Model Serving
Kubeflow supports two model serving systems that allow multi-framework model serving: KFServing and Seldon Core. Alternatively, you can use a standalone model serving system.

## How to use 
- To install on AWS follow instructions from the following link: https://www.kubeflow.org/docs/aws/deploy/install-kubeflow/
- In order to access and configure components you will need to be able to be comfortable using kubectl command and have familiarity with kubernetes(namespaces,pods, etc.)


## Resources 
https://www.kubeflow.org/docs/started/kubeflow-overview/



## Pain Points 
- Kubeflow is still relatively new and a lot of the components are still in beta.
- Kubeflow is not event driven, things like event triggering(training or model deployment) cannot be automated with the out of the box installment
