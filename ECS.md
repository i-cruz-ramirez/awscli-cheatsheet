### Create ECS Cluster
ecs-cli up --keypair name-pem --instance-type t2.micro --size 2 --cluster demo --capability-iam --verbose

### Delete ECS Cluster
ecs-cli down --cluster demo
