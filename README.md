# ansible-playbook-assessment
It's a public repository, which i created for my Assignment work
# Ansible Playbook Deployment Guide

This guide provides step-by-step instructions for setting up Ansible and deploying a playbook to install Apache on your servers. 

## Firstly Install Git

Git which helps me for arranging, repositories & pushing my code to GitHub.

### Windows(Using Windows for this)
1. Download Git
2. Run the Installation according to the given steps.

## Secondly Create a GitHub Account

If you don't have a GitHub account, create one:

1. Sign up.
2. Confirm Email.

## Third one Create a GitHub Repository according to the given details

1. Login to GitHub.
2. Create a New Repository:
   - Click on the "+" icon in the top-right corner and select "New repository".
   - Fill the below details:
     - Repository name: Enter_name
     - Description: Add description.
     - Public: Make it Public.
     - Check "README" box
   - Click "Create repository".

## Fourth Set Up Git Locally

1. Run git bash as an Administrator.
2. Configure Git user.name & user.email by using these below 2 commands
   git config --global user.name "your_name"
   git config --global user.email "your_email"

## Fifth Make a Clone Repository Locally

## Fetch Repository URL
Go to your GitHub repository page and click on the green "Code" button to copy the repository URL.

## Clone Repository
Run the following command in gitBash
In my case it is: git clone https://github.com/AnanTariq/ansible-Playbook-assessment.git


## Step 6: Create and Push the Ansible Playbook

### Playbook Structure

The Ansible playbook should be defined with the following sections:

- **hosts:** Defines the groups of machines the playbook will apply to.
- **tasks:** Lists the series of actions the playbook will perform.
- **handlers:** Lists the actions that should be triggered by task notifications.

#### Example Playbook

```yaml
---
- name: Example Playbook
  hosts: all
  tasks:
    - name: Ensure Apache is installed
      apt:
        name: apache2
        state: present
      notify:
        - Restart Apache

  handlers:
    - name: Restart Apache
      service:
        name: apache2
        state: restarted



##### Create A Notebook .yml file & save it
write down .yml file according to the above given structure

##### Add commit,and push changes to github
used to add git add playbook.yml(Nmae of Playbook).
commit it by using  git commit -m"change commit"
Push the code to github git oush origin main
