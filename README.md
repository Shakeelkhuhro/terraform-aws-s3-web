# AWS S3 Static Website Portfolio

This project provisions an AWS S3 bucket to host a static portfolio website using Terraform. It includes infrastructure-as-code for S3 bucket creation, public access configuration, website hosting, and deployment of static assets (HTML, CSS, and image files).

🔗 **Live Site**: [http://shakeel-bucket00.s3-website-us-east-1.amazonaws.com/](http://shakeel-bucket00.s3-website-us-east-1.amazonaws.com/)

## Features

- **Infrastructure as Code**: All AWS resources are managed via Terraform.
- **Static Website Hosting**: S3 bucket configured for static website hosting with custom index and error pages.
- **Public Access**: Proper ACLs and ownership controls for public-read access.
- **Easy Deployment**: Just run `terraform apply` to deploy or update your site.

## Project Structure

```

.
├── main.tf                # Main Terraform configuration
├── provider.tf            # AWS provider configuration
├── output.tf              # Terraform outputs
├── varaibles.tf           # Terraform variables
├── index.html             # Main website page
├── error.html             # Custom error page
├── profile.png            # Profile image for the site
├── .terraform.lock.hcl    # Terraform dependency lock file
├── terraform.tfstate\*     # Terraform state files (should not be committed)
└── ...

````

## Prerequisites

- [Terraform](https://www.terraform.io/downloads.html) v1.12.2 or later
- [AWS CLI](https://aws.amazon.com/cli/) configured with appropriate credentials
- An AWS account with permissions to manage S3

## Usage

1. **Clone the repository**
   ```sh
   git clone https://github.com/Shakeelkhuhro/terraform-aws-s3-web.git
   cd terraform-aws-s3-web

```
```

2. **Initialize Terraform**

   ```sh
   terraform init
   ```

3. **Review and apply the plan**

   ```sh
   terraform plan
   terraform apply
   ```

4. **Access your website**

   * Visit the live S3 URL:
     [http://shakeel-bucket00.s3-website-us-east-1.amazonaws.com/](http://shakeel-bucket00.s3-website-us-east-1.amazonaws.com/)

## Customization

* Edit `index.html`, `error.html`, and `profile.png` to personalize your site.
* Change the bucket name in [`varaibles.tf`](varaibles.tf) if needed.

## Clean Up

To destroy all resources created by this project:

```sh
terraform destroy
```

## License

This project is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/).

```
