# Terraform Static Website Hosting with S3

This repository provides Terraform configurations to deploy a static website on Amazon S3. The static website content is assumed to be hosted on GitHub.

## Prerequisites

Before you begin, ensure you have the following:

1. [Terraform](https://www.terraform.io/) installed on your machine.
2. AWS credentials configured with appropriate permissions.
3. A GitHub repository containing your static website files.

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/terraform-s3-static-website.git
Change into the project directory:

bash
Copy code
cd terraform-s3-static-website
Create a new Terraform configuration file (e.g., terraform.tfvars) and provide the required variables:


# terraform.tfvars

aws_access_key = "your-aws-access-key"
aws_secret_key = "your-aws-secret-key"
aws_region     = "us-east-1"
bucket_name    = "your-unique-bucket-name"
github_repo    = "your-username/your-repo"
Make sure to replace the placeholder values with your actual AWS and GitHub information.

Initialize the Terraform configuration:
terraform init

Apply the Terraform configuration:
terraform apply
Review the changes and type yes to apply them.

**Deploying the Static Website**
After applying the Terraform configuration, your static website will be deployed to the specified S3 bucket. You can access the website using the following URL:

http://your-unique-bucket-name.s3-website-us-east-1.amazonaws.com/

Cleaning Up
To remove the resources created by Terraform, run:
terraform destroy
Review the changes and type yes to confirm.

**Additional Notes**
Ensure that your GitHub repository has the necessary static website files (e.g., index.html, css, js).
Make sure your S3 bucket name is globally unique, as it is used in the website URL.
Customize the Terraform configuration as needed, such as updating the S3 bucket configuration or adding custom domain settings.
Feel free to reach out if you encounter any issues or have questions!

csharp
Copy code

You can copy and paste this content into a file named `README.md` in your project repository. Adjust the content as needed for your specific use case.
