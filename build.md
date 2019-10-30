Make sure you have `awscli` installed, if not: `brew install awscli`.

Build the latest version:
```
docker build -t thumbor .
```

Tag the new image:
```
docker tag thumbor:latest 893671114314.dkr.ecr.us-east-1.amazonaws.com/thumbor:latest
```

Log in to AWS ECR with docker with the following command:
```
$(aws ecr get-login --no-include-email --region us-east-1)
```

Push the repository to ECR
```
docker push 893671114314.dkr.ecr.us-east-1.amazonaws.com/thumbor
```
