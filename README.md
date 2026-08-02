# Static-Website-Hosting-on-S3
Static Website Hosting on AWS S3 using Terraform — This project provisions an S3 bucket with Terraform, enables static website hosting, and deploys index.html and error.html pages. It demonstrates Infrastructure as Code, AWS bucket policies, and hosting a portfolio site via the S3 website endpoint


01
Install Terraform and AWS CLI
You need Terraform to provision infrastructure and AWS CLI to authenticate.

Download Terraform from terraform.io

Install AWS CLI from [aws.amazon.com/cli]

Configure AWS credentials: aws configure

02
Create Terraform Project Folder
Organize your configuration files in a dedicated directory.

Make a folder: mkdir terraform-s3-site

Inside, create main.tf, index.html, and error.html

Place your website files (index.html, error.html) here

03
Write Terraform Configuration
Define resources for S3 bucket, website hosting, and objects.

Add aws_s3_bucket for your site bucket

Add aws_s3_bucket_website_configuration for hosting

Add aws_s3_bucket_policy to allow public read

Add aws_s3_object for index.html and error.html

04
Initialize and Apply Terraform
Run Terraform commands to provision resources.

Run terraform init to set up providers

Run terraform plan to preview changes

Run terraform apply and confirm with yes

05
Verify Website Hosting
Check that your site is live on the S3 endpoint.

Copy the endpoint from Terraform output

Open in browser with http:// (not https)

Confirm index.html loads and error.html shows for invalid paths

06
Enhance with CloudFront and Route 53
Optional step to add HTTPS and custom domain.

Add CloudFront distribution pointing to S3 bucket

Configure Route 53 to map your domain

Request SSL certificate via ACM for HTTPS

-------------------Summary---------------

This project showcases how to host a static website on AWS S3 using Terraform. It provisions an S3 bucket, enables static website hosting, and deploys index.html and error.html pages with automated Infrastructure as Code. The bucket policy is configured for public access, allowing the site to be served via the S3 website endpoint. This project demonstrates practical skills in cloud computing, Terraform automation, and AWS services, making it a strong portfolio example for cloud and DevOps practices. Future enhancements include adding CloudFront for HTTPS and Route 53 for a custom domain.
