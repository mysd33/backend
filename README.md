* ローカルでDockerビルド
```sh
docker build -t 523530166249.dkr.ecr.ap-northeast-1.amazonaws.com/mynavi-sample-ecs-backend .
```

* ローカルでDocker実行（ProfileをdevでSpringBoot実行）
```sh
docker run -d -p 8080:8080 --name samplebackend --env ENV_TYPE=dev 523530166249.dkr.ecr.ap-northeast-1.amazonaws.com/mynavi-sample-ecs-backend
```