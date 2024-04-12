# Orchestration-Scaling

## AWS CLI and Boto3 Setup Guide

This guide provides step-by-step instructions on how to set up AWS Command Line Interface (CLI) and Boto3, a Python SDK for AWS. This setup will enable you
to interact with AWS services directly from your command line and Python scripts.

**Prerequisites**

Before you begin, ensure you have:
- An AWS account.
- Python installed on your system.

1. Setting Up AWS CLI

Installation

1. Download AWS CLI: Visit the AWS CLI installation page (https://aws.amazon.com/cli/) and download the appropriate version for your operating system.
2. Install AWS CLI: Follow the installation instructions provided on the download page for your OS.

**Configuration**

1. AWS Credentials: You'll need your AWS Access Key ID and Secret Access Key. You can find these in your AWS Management Console under IAM.
2. Configure AWS CLI:
   - Open your terminal or command prompt.
   - Run the command `aws configure`.
   - Enter your Access Key ID, Secret Access Key, default region name, and default output format when prompted.

2. **Setting Up Boto3**

    Installation

    1. Install Boto3: Run the command `pip install boto3` in your terminal or command prompt.

**Configuration**

  Boto3 uses the credentials stored by AWS CLI. If AWS CLI is configured, no additional steps are required for Boto3.

  3. Containerized using Docker

**Frontend**
1. Clone the repository:
   ```bash
   git clone https://github.com/UnpredictablePrashant/SampleMERNwithMicroservices.git

1. Navigate to SampleMERNwithMicroservices/frontend.
   
2. Use the provided dockerfile to create a container image:
   
   `sudo docker build -t frontendimage .`


**Backend**

1. Navigate to `SampleMERNwithMicroservices/backend/helloService`.

2. Use the provided Dockerfile to create a container image:
   
   `sudo docker build -t backendhelloimg .`

3. Navigate to SampleMERNwithMicroservices/backend/profile.

4. Use the provided Dockerfile to create a container image:

     `sudo docker build -t backendprofileimg .`

**Amazon ECR Setup**
 
>Create an Amazon ECR repository for each image:

1.Hello Microservice: public.ecr.aws/s7f2n3x3/nikhil_backend1

2.Profile Microservice: public.ecr.aws/s7f2n3x3/nikhil_backend2

3.Frontend Microservice: public.ecr.aws/s7f2n3x3/nikhil_frontend1


