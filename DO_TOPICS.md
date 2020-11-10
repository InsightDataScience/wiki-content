# DevOps Topics



1. Istio
    - What situations is it used in?
    - How does it relate to Envoy how it interacts with it?
    - What is the preferred way of deploying it?

1. Docker Compose
    - What is it and when is it very useful to have?
    - What are the basic sections of a docker-compose file?
    - How does it relate to Helm and ECS Service Definitions?

1. Chaos Testing
    - What is chaos testing and why is it useful?
    - What are the general frameworks that are used in chaos testing?
    - How do these frameworks generally work (ie client/server interactions)

1. CircleCI
    - How does CCI work?
    - What is the general layout of the config file?
    - How to deal with secrets/contexts and multi-stage builds?

1. Jenkins
    - How does CCI work?
    - What is the general layout of the config files / use of groovy?
    - What makes Jenkins better / worse than a managed CI provider like CCI?

1. Kubernetes Service Types and Load Balancing
    - NOTE: This is going to fall into a broader K8s category.  Don't worry about deployment, just the nuances of accessing services.
    - What is a k8s service and it's types?
    - How to provision a load balancer and connect various services to it?
    - What are the critical parts of managing load balancers / maintaining observability over them?

1. Airflow
    - NOTE: Keep this focused on the DevOps part of this. Don't worry about talking too much about DAGs
    - What is Airflow and what makes it cool?
    - What are the advantages of running Airflow on VMs vs K8s?
    - What are the different topologies for workers (ie sequential executor vs celery vs k8s)
    - What are the different ways to share DAGs across workers?

1. SQLAlchemy and Alembic
    - What are ORMs and why are they cool?
    - What specific challenges do they solve (ie migrations)?
    - How does Alembic work?

1. Helm Charts
    - What is Helm and why is it cool?
    - How does it compare to other package managers?
    - How to get started with Helm?
    - How to test helm charts?

1. IAM
    - What is IAM and why is it needed?
    - What are the basic patterns of IAM and where do they come from?
        - ie Roles (different types) / Policies / Users / Instance Profiles
    - How to manage user directories with IAM (ie SSO)

1. Rook & Ceph
    - What is Ceph and why is it cool and not so cool (difficult to manage)?
    - What challenges does Rook solve and what are it's features?
    - How to deploy rook with Helm?

1. Load Testing
    - What is load testing and why is it needed?
    - What are the tools people use for load testing?
    - What are the typical tools you use in conjunction with say Locust to do load testing?

1. Vault
    - What is Vault and why is it used?
    - What is the architecture and patterns used in Vault?

1. Kubernetes Operators
    - What are K8s operators and what challenges do they solve?
    - What are the popular operators?
    - What are the patterns that people use to manage operators?

1. Prometheus & Grafana
    - What is Prometheus, how it is used, and why is it cool?
    - What is the general architecture of Prometheus tools?
    - What is PromQl and compare it to SQL with example?

1. Kubeflow
    - What is kubeflow and why it cool?
    - What is the easiest way to run kubeflow?
    - What are the components of kubeflow / architecture?

1. Kafka
    - What is kafka and why is it cool?
    - What is the general architecture of kafka?
    - What are the main use cases of Kafka?

1. Cloud Networking
    - What is a VPC and the different types (default vs custom)?
    - What are the differences between the types of VPCs?
    - What is peering and what are pain points of peering?

1. Logz
    - What is Logz is how is it used?
    - What is the general architecture of logz?
    - How does it compare to other logging tools?
