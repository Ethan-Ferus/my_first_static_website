# my_first_static_website

We will be creating a simple static website with an index.html file and a error.html file using Terrafrom deployed to AWS

You are more than welcome to use the terraform registry or ask chatgpt to explain the argument references

# Project layout:

<img width="174" height="629" alt="project file layout" src="https://github.com/user-attachments/assets/525ec3c9-96ba-4412-a351-98ec0388185f" />

# Provider File:

First, create a file and name it provider.tf. This file will hold our provider so that Terraform will recongize who our provider is.

<img width="270" height="119" alt="provider" src="https://github.com/user-attachments/assets/df25eef0-d0f7-4762-a762-8be7cb1d2b12" />

Next, You will use the terraform init command to initialize the project

<img width="565" height="179" alt="terraform init" src="https://github.com/user-attachments/assets/e0481e24-be88-490e-964f-5c82b4e836c8" />
<img width="579" height="177" alt="terraform initialized" src="https://github.com/user-attachments/assets/8374560a-bbcd-4a3f-8391-a584d922fd8d" />

Next, create a index.html file. This file will be displayed on our static website for our users to see.

<img width="401" height="310" alt="index html file" src="https://github.com/user-attachments/assets/af3e1f66-0989-4cee-9f73-0969006944c4" />

Next, create a error.html file. This file will only be displayed when users do not find our static website

<img width="493" height="313" alt="error html file" src="https://github.com/user-attachments/assets/cf33b892-77d7-4b3a-9908-1d1d59d2cf9f" />

# s3.tf file:

Please create a s3.tf file. This is where all our s3 related configurations will be coded

Next, create a s3 bucket resource. We'll be using the bucket to host our website and please remember that all s3 bucket names must be globallly unique 

<img width="569" height="89" alt="s3 bucket" src="https://github.com/user-attachments/assets/fa8a497f-8493-4f45-92e1-c6d9e1dec9e5" />

Next, in the same file create a s3 bucket website configuration website. This resource enables and configures static website hosting on an s3 bucket and tell aws to serve HTML,CSS,JS files as a website

<img width="464" height="229" alt="website configuration" src="https://github.com/user-attachments/assets/932e3493-b861-49b8-b6a3-425d1521eca7" />

Next, in the same file create a s3 public access block resource. This resource is a firewall before your policy. If this says "block", then even a public bucket won't allow access

<img width="532" height="153" alt="public access block" src="https://github.com/user-attachments/assets/4123083b-7f34-40da-9ed0-5cb6940fb4e8" />

Next, in the same file create a s3 bucket policy resource. This resource allows s3 to display our html files and is written in a .json format

<img width="430" height="256" alt="bucket policy" src="https://github.com/user-attachments/assets/58a1c796-cad4-4d04-8edf-d7b84768cbbc" />

Next, in the same file create 2 s3 object resources. This resource uploads a file or raw content into an s3 bucket
<img width="312" height="119" alt="index object" src="https://github.com/user-attachments/assets/6844a985-8a64-4e1a-b52b-039fd92da898" />

<img width="309" height="117" alt="error object" src="https://github.com/user-attachments/assets/af1137a6-4fdd-484d-8651-103890392c8e" />

Next, You will use the terraform plan command to display all the resources that will be built and to check if the configuration is correct

<img width="991" height="76" alt="terraform plan" src="https://github.com/user-attachments/assets/4f354948-9762-4403-86e3-18aa2e32420d" />
<img width="1057" height="110" alt="terraform plans" src="https://github.com/user-attachments/assets/cc0515c4-4c1b-43d3-9235-25404498306b" />

Once you are happy with the configurations and ready to deploy then you will use the terraform apply command to deploy these services into your account

<img width="990" height="616" alt="terraform apply" src="https://github.com/user-attachments/assets/9c6ce2cf-06b6-47ca-afab-4373c9ddd2c9" />
<img width="396" height="550" alt="terraform apply yes" src="https://github.com/user-attachments/assets/48cfcc8a-fcc6-4b05-87db-5f561cf37d4f" />
<img width="731" height="259" alt="terraform apply done" src="https://github.com/user-attachments/assets/54b83b47-d096-4d91-a430-01c56f2f4a48" />

Check for the s3 bucket in your aws account and there should be 2 objects displayed in your bucket
<img width="1076" height="389" alt="aws account s3 bucket" src="https://github.com/user-attachments/assets/56af1755-8c8a-4125-a900-a128e8520a17" />
<img width="1060" height="564" alt="aws account s3 bucket object" src="https://github.com/user-attachments/assets/7f00f10d-4800-4e0c-afa2-757f11ff312a" />

Click onto the objects and check if the files are working

<img width="1366" height="768" alt="aws account index page" src="https://github.com/user-attachments/assets/cd54d532-64e0-4363-8d38-f328efe9540d" />
<img width="1366" height="768" alt="aws account error page" src="https://github.com/user-attachments/assets/c293db49-b798-4d76-9246-9ee89a539066" />

Once you are happy with what you have built then use the terraform destroy command so that you not get billed

<img width="693" height="132" alt="terraform destroy" src="https://github.com/user-attachments/assets/c1240eda-e605-43cc-97c0-42dc2d3db361" />
<img width="645" height="441" alt="terraform destroy yes" src="https://github.com/user-attachments/assets/0acb3a81-d1ac-4ddc-ae80-21a258593c23" />
<img width="641" height="257" alt="terraform destroy done" src="https://github.com/user-attachments/assets/a050f81f-16a3-445e-ae1e-7a557a4466a4" />
