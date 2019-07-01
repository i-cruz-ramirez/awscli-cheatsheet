## Get Login Token

```sh
aws ecr get-login --no-include-email
```

## Login ECR 
```sh
$(aws ecr get-login --no-include-email)
```

```sh
aws ecs create-cluster --cluster-name production
```

```sh
aws ecs register-task-definition --cli-input-json file://photo-filter.json | jq
```

```sh
aws ecs list-task-definitions | jq
```

aws ecs list-services --cluster production
aws ecs create-service --cluster production --service-name my-service 
    --task-definition taskname-revision --desired-count 1 --launch-type "FARGATE" 
    --network-configuration "awsvpcConfiguration={subnets=[...],securityGroups=[...]}"
aws ecs describe-services --cluster production --service my-service


# scale up 
aws ecs update-service --cluster production --service photo-filter desired-count 2
# scale down
aws ecs update-service --cluster production --service photo-filter desired-count 1
# rollback or upgrade
aws ecs update-service --cluster production --service photo-filter --task-definition photo-filter:18
