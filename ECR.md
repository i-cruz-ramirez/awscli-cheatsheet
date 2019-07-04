## Get Login Token
```sh
aws ecr get-login --no-include-email
```

## Login ECR 
```sh
$(aws ecr get-login --no-include-email)
```

## Create Repository
```sh
aws ecr create-repository --repository-name REPOSITORY_NAME --region us-west-1
```
