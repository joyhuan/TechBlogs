# Terraform

- automate and manage your infra
- your platform
- and services that run on that platform

- oepn source
- decalarative

## Tool for infra provisioning

![Terraform Architecture](https://github.com/joyhuan/TechBlogs/blob/master/images/TerraformArchitecture.png)
Terraform is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage hundreds of cloud services. Terraform codifies cloud APIs into declarative configuration files.

Terraform's configuration language is declarative (describes the desired end-state for your infra), verses procedural/imperative PL that require step-by-step instructions to perform tasks. 

Terraform providers automatically calculate dependencies between resources to create or destroy them in the correct order.


To deploy infrastructure with Terraform:

- Scope - Identify the infrastructure for your project.
- Author - Write the configuration for your infrastructure.
- Initialize - Install the plugins Terraform needs to manage the infrastructure.
- Plan - Preview the changes Terraform will make to match your configuration.
- Apply - Make the planned changes.

Terraform keeps track of your real infrastructure in a state file, which acts as a source of truth for your environment. Terraform uses the state file to determine the changes to make to your infrastructure so that it will match your configuration.

