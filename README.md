* ローカルでDockerビルド
```sh
docker build -t XXXXXXXXXXXX.dkr.ecr.ap-northeast-1.amazonaws.com/mynavi-sample-ecs-backend .
```

* ローカルでDocker実行（ProfileをdevでSpringBoot実行）
```sh
docker run -d -p 8080:8080 --name samplebackend --env ENV_TYPE=dev XXXXXXXXXXXX.dkr.ecr.ap-northeast-1.amazonaws.com/mynavi-sample-ecs-backend
```

* ECRプッシュ
```sh
aws ecr get-login-password --region ap-northeast-1 | docker login --username AWS --password-stdin XXXXXXXXXXXX.dkr.ecr.ap-northeast-1.amazonaws.com
docker push XXXXXXXXXXXX.dkr.ecr.ap-northeast-1.amazonaws.com/mynavi-sample-ecs-backend:latest
```