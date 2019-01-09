# AWS Commands

## Creating Application
```sh
aws elasticbeanstalk create-application --application-name avengers --region eu-west-3
```

## Creating Enviroment
```sh
aws elasticbeanstalk create-environment --application-name avengers \
    --environment-name staging \
    --solution-stack-name "64bit Amazon Linux 2017.09 v2.9.2 running Docker 17.12.0-ce" \
    --option-settings file://options.json \
    --region eu-west-3
```

# EB Commands (Inside Folder)

## Creating Application
```sh
eb init
```

## Creating environment
```sh
eb create
```
Take note:
- When we create environment via the eb cli, the environment created are by default auto-scale, load-balanced environment.
- The default instance type is t2.micro.

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

// Switching and deploying to staging
eb use helloeb-staging
eb deploy

// Switching and deploying to production
eb use helloeb-production
eb deploy
```

## Logs Checking
```sh
eb logs
```

## Deployment
```sh
eb deploy
```
