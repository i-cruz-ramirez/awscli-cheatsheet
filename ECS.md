### Create ECS Cluster
```sh
ecs-cli up --keypair name-pem --instance-type t2.micro --size 2 --cluster demo --capability-iam --verbose
```

### Delete ECS Cluster
```sh
ecs-cli down --cluster demo
```

### Register Task definition
```sh
aws ecs register-task-definition --cli-input-json file://photo-filter.json | jq
```

```sh
aws ecs list-task-definitions | jq
```

```sh
aws ecs list-services --cluster production
```

```sh
aws ecs create-service --cluster production --service-name my-service 
    --task-definition taskname-revision --desired-count 1 --launch-type "FARGATE" 
    --network-configuration "awsvpcConfiguration={subnets=[...],securityGroups=[...]}"
```

```sh
aws ecs describe-services --cluster production --service my-service
```

# scale up 
```sh
aws ecs update-service --cluster production --service photo-filter desired-count 2
```

# scale down
```sh
aws ecs update-service --cluster production --service photo-filter desired-count 1
```

# rollback or upgrade
```sh
aws ecs update-service --cluster production --service photo-filter --task-definition photo-filter:18
```
