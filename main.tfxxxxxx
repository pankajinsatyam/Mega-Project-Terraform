terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = "us-east-1"
}

# 1. Main S3 Bucket Resource
resource "aws_s3_bucket" "my_bucket" {
  bucket        = "my-unique-bucket-name-2026" # Must be globally unique
  force_destroy = false                         # Set to true if you want to delete the bucket even if it contains objects

  tags = {
    Name        = "My Secure Bucket"
    Environment = "Dev"
  }
}
