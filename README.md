# django-github-actions-aws
Demonstrates how to set up a CI/CD Pipeline with GitHub Actions and AWS in a Django project

# Step 1
clone this repo into your local system 
create a virtual environment for python if your using mac

```
cd django-github-actions-aws
```
### Once you are inside the project's directory, create a virtual environment by running the following command:

```
python3 -m venv devenv
```
### Activate the virtual environment. The process for activating a virtual environment differs depending on your operating system:
```
For Windows:
myenv\Scripts\activate
```
```
For macOS and Linux:
source myenv/bin/activate
```
### after activation your terminal prompt will look like this indicating your in your virtual environment
```
(devenv) macs-MacBook-Air:django-github-actions-aws
```
### install the projects requirements by running the following command.
```
pip install -r requirements.txt
```
### Login to your aws plaform create an elastic beanstalk Env using the following parameters
click on the "Create a New Environment" prompt
- Select Web server environment 
- Application name:django-github-actions-aws
- Enviroment will be auto generated
- platform:managed
          - python
          - python 3.9 running on 64bit amazon linux 2023
- click on next steps until environment has been created 
  ### the rest settings should be default do not enable some options as they come with charges or cost
Copy your aws cli keys and create a secret value in github clicking settings --> secrets and valuables --> Actions -->new repository secrets
Any PR push in your github environment will trigger a build and deploy cicd Workflow.

