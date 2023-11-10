# Static Website Hosting with Terraform and S3

This repository contains the necessary Terraform configurations to deploy a static website on AWS S3. The static website includes an `index.html` file for the main content and an `error.html` file for custom error pages.

## Prerequisites

Before you begin, ensure that you have the following:

- [Terraform](https://www.terraform.io/downloads.html) installed on your machine.
- AWS credentials configured on your local environment.

## Terraform Configuration

### `main.tf`

```hcl
provider "aws" {
  region = "us-east-1" # Change this to your desired AWS region
}

resource "aws_s3_bucket" "static_website" {
  bucket = "your-unique-bucket-name" # Change this to a globally unique bucket name
  acl    = "public-read"

  website {
    index_document = "index.html"
    error_document = "error.html"
  }
}

**### `variables.tf`**

variable "region" {
  description = "AWS region for S3 bucket"
  default     = "us-east-1" # Change this to your desired AWS region
}

variable "bucket_name" {
  description = "Name of the S3 bucket"
  default     = "your-unique-bucket-name" # Change this to a globally unique bucket name
}

