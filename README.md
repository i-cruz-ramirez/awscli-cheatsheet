# AWS Command Line Interface Cheatsheet

### Aws configure

```sh
$ aws configure
AWS Access Key ID [****************OMLQ]: ********
AWS Secret Access Key [****************BQWW]: ***********
Default region name [us-east-1]: eu-west-1
Default output format [json]: json
```

### Update a Specific Property
```sh
$ aws configure
AWS Access Key ID [****************1234]: 
AWS Secret Access Key [****************1234]: 
Default region name [eu-west-1]: 
Default output format [json]: table
```

### AWS Configure a Named Profile
```sh
aws configure --profile administrator
AWS Access Key ID [None]: 12334567890
AWS Secret Access Key [None]: ABCDEFGHIJKLMNOPQRSTUVWXYZ
Default region name [None]: eu-west-1
Default output format [None]: json
```

### List Config Data

```sh
$ aws configure list
      Name                    Value             Type    Location
      ----                    -----             ----    --------
   profile                <not set>             None    None
access_key     ****************1234 shared-credentials-file    
secret_key     ****************1234 shared-credentials-file    
    region                eu-west-1      config-file    ~/.aws/config
```

### AWS Configuration Files

```sh
$ cat ~/.aws/credentials
[default]
aws_access_key_id=1234567890
aws_secret_access_key=ABCDEFGHIJKLMNOPQRSTUVWXYZ

[user2]
aws_access_key_id=0987654321
aws_secret_access_key=ZYXWVUTSRQPONMLKJIHGFEDCBA
```

```sh
$ cat ~/.aws/config
[default]
region=us-west-2
output=json

[profile user2]
region=us-east-1
output=text
```

# (EBS) Elastic Beanstalk
## Creating Application
```sh
eb init
```

## Creating environment
```sh
eb create
```

## Opening Elastic Beanstalk Dashboard
```sh
eb console
```

## Show current environment
```sh
eb list
```

## Switch environment
```sh
eb use
```

## Logs Checking
```sh
eb logs
```

## Deployment
```sh
eb deploy
```
