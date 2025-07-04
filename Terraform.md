- What is Terraform and how it is different from other IaaC tools?
Ans:-> Terraform is an open-source Infrastructure as Code (IaC) tool developed by HashiCorp. It lets you define, provision, and manage cloud and on-prem infrastructure using a declarative language called HCL (HashiCorp Configuration Language).

it support multi cloud :-> AWS, GCP, AZURE etc.
it has state menagement also
strong community.

2. How do you call a main.tf module?
You call a main.tf module using the module block in another Terraform configuration.

module "example" {
  source = "./path-to-module"
}

3. What exactly is Sentinel? Can you provide few examples where we can use for Sentinel policies?
Sentinel is a policy-as-code framework by HashiCorp used to enforce fine-grained governance and compliance rules in Terraform Enterprise and Cloud.

Restrict resource types
Enforce tagging
Cost control 


4. You have a Terraform configuration file that defines an infrastructure deployment. However, there are multiple instances of the same resource that need to be created. How would you modify the configuration file to achieve this? 

You can create multiple instances of the same resource in Terraform using the count or for_each meta-arguments.

resource "aws_instance" "example" {
  count         = 3
  ami           = "ami-123456"
  instance_type = "t2.micro"
}

5. Below command will destroy everything that is being created in the infrastructure. Tell us how would you save any particular resource while destroying the complete infrastructure. 

when running terraform destroy, use the -target flag only for the resources you want to destroy, not the whole infrastructure.
terraform destroy -target=aws_instance.example

6. Which module is used to store .tfstate file in S3? 
Ans :-> The backend "s3" module is used to store the .tfstate file in an S3 bucket.

7.How do you manage sensitive data in Terraform, such as API keys or passwords?
Ans :-> In Terraform, sensitive data like API keys or passwords can be managed using:

We use Environment varaibles
Hashicrop vault  to store the senstivte data.

9. You are working on a Terraform project that needs to provision an S3 bucket, and a user with read and write access to the bucket. What resources would you use to accomplish this, and how would you configure them?

Ans :_> aws_s3_bucket – to create the bucket, aws_iam_user – to create the user, aws_iam_policy – to define S3 read/write permissions, aws_iam_user_policy_attachment – to attach the policy to the user

10. Who maintains Terraform providers?
Ans :-> Terraform providers are maintained by HashiCorp, cloud vendors (like AWS, Azure, GCP), and the open-source community.

11. 





