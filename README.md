# (EBS) Elastic Beanstalk
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
