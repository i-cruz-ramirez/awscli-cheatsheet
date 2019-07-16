# Check the status given instance identifier

```sh
$ aws --region us-west-1 rds describe-db-instances \
  --db-instance-identifier INSTANCE_IDENTIFIER \
  --query 'DBInstances[].{DBInstanceStatus:DBInstanceStatus}'
```

# Grab instance address

```sh
$ aws --region us-west-1 rds describe-db-instances \
  --db-instance-identifier INSTANCE_IDENTIFIER \
  --query 'DBInstances[].{Address:Endpoint.Address}'
```
