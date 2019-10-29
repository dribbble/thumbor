Make sure you have `awscli` installed, if not: `brew install awscli`.

To log in to AWS ECR with docker, run the following command:
```
$(aws ecr get-login --no-include-email --region us-east-1)
```

Build the latest version:
```
docker build -t thumbor .
```

Tag the new image:
```
docker tag thumbor:latest 893671114314.dkr.ecr.us-east-1.amazonaws.com/thumbor:latest
```

If that succeeds, push the repository:
```
docker push 893671114314.dkr.ecr.us-east-1.amazonaws.com/thumbor
```
