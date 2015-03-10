# Deploying a containerized app with Weave on AWS with Ansible #

## What you will build ##

Weave allows you to focus on developing your application, rather than your infrastructure.

In this example we will demonstrate how Weave allows you to quickly and easily deploy HAProxy as
a load balancer for a simple php-fpm application running in containers on multiple nodes in [Amazon 
Web Services](http://aws.amazon.com), with no modifications to the application and minimal docker 
knowledge.

## What you will use ##

* [Weave](http://weave.works)
* [Docker](http://docker.com)
* [Ansible](http://ansible.com)
* [HAProxy](http://haproxy.org)
* [PHP-FPM](http://php.org)
* [Ubuntu](http://ubuntu.com)
* [Amazon Web Services](http://aws.amazon.com)

## What you will need to complete this guide ##

This getting started guide is self contained. You will use Weave, Docker, Ansible, HAProxy, PHP-fpm, 
Ubuntu and Amazon Web Services.  

You will need to have a valid [Amazon Web Services](http://aws.amazon.com) (AWS) account and to know your AWS acess key id and secret. Please refer to [AWS Identity and Access Management documentation] (http://docs.aws.amazon.com/IAM/latest/UserGuide/IAM_Introduction.html#IAM-credentials-summary) for details on how to retrive your credentials. If you have already installed the [AWS CLI](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-set-up.html) these details will be accesible to Ansible.

You will need to have [Ansible installed](http://docs.ansible.com/intro_installation.html). Interacting with the AWS via Ansible also requires [boto](http://docs.pythonboto.org/en/latest/), which provides a Python interface to AWS.  

* 15 minutes
* [Git](http://git-scm.com/downloads)
* [Ansible >= 1.8.4](http://docs.ansible.com/intro_installation.html)

It may be helpful to have the [AWS CLI]((http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html) installed, but this is optional.
 
* [AWS CLI > 1.7.12 ](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html)

## Configuring and setting up your Instances ## 

All of the code for this example is available on [github](http://github.com/fintanr/weave-gs), and you first clone the 
getting started repository.

```bash
git clone http://github.com/fintanr/weave-gs
cd weave-gs/weave-ansible-haproxy-aws
```

### AWS Regions ### 

The ansible playbook associated with this guide use the `eu-west-1` region by default, and an [AMI](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) from the same region. You can change the region and AMI to your preferred option by calling `./check-region.sh -r <your region>`.

Alternatively if you have the [AWS CLI](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html) installed you can call `./check-region.sh` which will select an AMI in your region.

In both cases this will create a file `ansible_aws_variables.yml` which our Ansible playbook will use.

```bash
cat ansible_aws_variables.yml 
---
aws_region: eu-west-1
template: ami-a9cb5dde
```

## Step ##


## What has happened ##


## Summary ##


## Credits ##

The Ansible playbook used here was heavily based on the work of [Sebastien Goasguen](http://sebgoa.blogspot.com/) in his
 [ansible-rancher playbook](). 
