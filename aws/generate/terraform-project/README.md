# Aws generate terraform project

## Premisses

- [Golang](https://golang.org/doc/install) installed

## Command

- Prompt

```bash
rit aws generate terraform-project
```

- Stdin

```bash
echo '{"project_name":"my-terraform-project", "project_location":"/home/user/projects", "bucket_name":"my-aws-bucket", "bucket_region":"us-east-1"}' | rit aws generate terraform-project --stdin
```

## Description

This formula allows the user to generate a terraform based project. The user has to provide 4 different inputs:

- The project name

- The path to the directory in wich the project will be created

- The name of the bucket the will be used as backend

- The AWS region of the bucket

The folders and files generated by this commands are as follows:

- A **main.tf** file containing the provider and inicial configuration

- A **.tfbackend** file containing the backend configuration

- Folders for terraform modules, templates and different environment variables

- **README.md** and **.gitignore** files

- A **Jenkisfile**

- A **.circleci** to run tests with terraform commands

- A **Makefile** with commands to run *terraform init/plan/apply/destroy*


## Demonstration

- Command execution

<img src="demo.gif">

- Generated folder

<img src="tree-image.png">
