# Redash
- Fork Redash to fix AWS ECR vulnerability
- Add volume to work with AWS ECS Fargate.
- Build and Push to the AWS ECR for each environment
- Example for dev:
  - aws ecr get-login-password --region ap-northeast-1 | docker login --username AWS --password-stdin xxxx.dkr.ecr.ap-northeast-1.amazonaws.com
  - docker build -t api-redash-dev .
  - docker tag api-redash-dev:latest xxxxx.dkr.ecr.ap-northeast-1.amazonaws.com/api-redash-dev:latest
  - docker push xxxxx.dkr.ecr.ap-northeast-1.amazonaws.com/api-redash-dev:latest
