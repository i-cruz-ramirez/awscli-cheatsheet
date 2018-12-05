# awscli-cheatsheet

### First time aws

```sh
# aws configure
AWS Access Key ID [****************OMLQ]: ********
AWS Secret Access Key [****************BQWW]: ***********
Default region name [us-east-1]: eu-west-1
Default output format [json]: json
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
