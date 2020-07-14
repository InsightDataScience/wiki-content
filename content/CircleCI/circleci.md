# CircleCI
After a software repository on GitHub or Bitbucket is authorized and added as a project to circleci.com, every code change triggers automated tests in a clean container or VM. CircleCI runs each job in a separate container or VM. That is, each time your job runs CircleCI spins up a container or VM to run the job in.

This is further achieved through a config.yml file stored in a .circleci/ directory

CircleCI then sends an email notification of success or failure after the tests complete. CircleCI also includes integrated Slack and IRC notifications. Code test coverage results are available from the details page for any project for which a reporting library is added.

CircleCI may be configured to deploy code to various environments, including AWS CodeDeploy, AWS EC2 Container Service (ECS), AWS S3, Google Kubernetes Engine (GKE), Microsoft Azure, and Heroku. Other cloud service deployments are easily scripted using SSH or by installing the API client of the service with your job configuration.

Writing the config file for CircleCI is pretty simple, and you can get an entire pipeline up and running by just hardcoding terminal commands into the config file. 


## How to use 

for CircleCI to to automatically deploy anything it reads all the steps it needs to take in a config.yml file
it does this by creating a docker-like container, cloning the repository then running the commands within the yml file inside of the container.

In the root of your repository create a .circleci folder and within the folder create a config.yml file

for a simple python based environment in the CircleCi container the config.yml file can look like this:

```
version: 2.1

orbs:
  python: circleci/python@0.2.1

jobs:
  build-test-deploy:
    executor: python/default
    steps:
      - checkout

      - run:
          name: pip dependencies
          command: pip install -r requirements.txt

      - run:
          name: Install terraform
          command: sudo bash terraform/install_terraform.sh

      - run:
          name: Terraform Commands
          command: |
              cd terraform/
              terraform init
              terraform apply -auto-approve
workflows:
  main:
    jobs:
      - build-test-deploy
```


The version is the version of CircleCI to use. it will most likely not change.
The orbs portion is like a baked in image specific to CircleCI

and when you get to the jobs: section you can see the name of the job "build-test-deploy" and the steps CircleCI will take.
- checkout is necessary to checkout the code from github.

- run: is running a command in the terminal, which can also do multiple commands at once if you start the command: with a |


Outline common uses of this topic, focusing on real life deployments and examples. Link to articles and videos to provide more information.

Bonus points for making it Insight specific.


## Resources 
- Everyone has to start somewhere, provide a short blurb for ANY turorials you found helpful, link to the tutorial, and any connected Codebases. 
- Youtube videos, Important documentation, etc.
- Please don't include out of date / bad resources.  This should be a best of list with

Example:
- [Some really awesome tutorial](https://towardsdatascience.com/getting-started-with-apache-airflow-df1aa77d7b1b)
    - This tutorial is about XYZ...


## Pain Points 
Identify current problems and paint points surround this topic / tool. What problems are people looking to solve around or with this topic/tool?

Example:
- **Something painful about this topic**
This is really annoying when it happens.  The reason for it is people need to write better code.  In order to get around it, write better code.