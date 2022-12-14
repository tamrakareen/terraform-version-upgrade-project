# terraform-version-update-project
Upgrading an old version of terraform 

![terraform image](https://opennebula.io/wp-content/uploads/2020/12/Terraform_2-scaled.jpg)

# Upgrading a Repo with a newer version of Terraform

## Introduction

✍️ Terraform has released several versions since the first one in 2014, and the evolution has significantly improved the functionality. It’s important to keep Terraform updated with major releases if we want to make the most of it. The differences between Terraform versions are usually syntax, behavior, and feature-support related. Syntax related changes are the most common ones that you’ll have to deal with when upgrading from Terraform 0.13.x or lower. This is because the HCL (Hashicorp Configuration Language) syntax has gone through significant changes. Also, regardless of the pace of your project/organization to grow or modify its cloud-based infrastructure, you will eventually need to reprovision it, to be able to include new resources or features. If you do this frequently, it is easier to keep up to date with syntax and supported attributes for each new resource you include, since you would be most likely using the latest modules with non-deprecated attributes. On the other hand, if there is no regular provisioning, you might not be aware of the need for an upgrade until you need to include some new feature that require an upgrade. In this scenario, the impact would be a lot larger. (source: encora.com)

## Use Case

- ✍️ My company has many repos that need to be upgraded a couple versions for an upcoming migration.

## Cloud Research

- ✍️ First research was how I upgrade and which version to begin with. Terraform has a [GUIDE](https://www.terraform.io/language/upgrade-guides) on how this should be done. Side note for new engineers- keep terraform's documentation site up all day, all the information you need is there. 

## Try yourself

✍️ Alright, I'm upgrading from 0.11.15 and following Terraform's instructions for v0.12. I'll then do it again for v0.13. 


### Step 1 — Change the .terraform-version file

Change the current version to 0.12.1 (just change the existing text) and run Terraform init. You'll likely get errors:

Error: Invalid output name
│
│   on outputs.tf line 2, in output "subnet.land-west-priv.*.sn_id":        
│    2: output "subnet.land-west-priv.*.sn_id" {
│
│ A name must start with a letter or underscore and may contain only        
│ letters, digits, underscores, and dashes.

and...

Error: Invalid expression
│
│ On variables.tf line 31: Expected the start of an expression, but found an invalid
│ expression token.

You'll go through each error and correct. I use VScode so my code is a different color if it's not correct which makes it easy to find where syntax needs updating. Continue fixes until you are able to successfully run Terraform init.

Last errors had to do with upgrading the AWS version and getting my AWS credentials set up in the non sandbox account. 

updated 8/1, to be continued...

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.
