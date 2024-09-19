# aws-tf

Install terraform

```
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

Install AWS CLI

```
curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
sudo installer -pkg AWSCLIV2.pkg -target /
```

Create access keys

Go to IAM -> Manage access keys -> Create access key

Configure AWS CLI

```
aws configure
```

Let's create a new project

```
mkdir aws-tf

cd aws-tf
```

Create provider.tf

```hcl
terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "5.67.0"
    }
  }
}

provider "aws" {
  # Configuration options
}
```
