
ECR 로그인
```bash
aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS --password-stdin 533267446521.dkr.ecr.ap-northeast-2.amazonaws.com
```
<br/>

이미지 빌드
```bash
cd ekssampleboot ## 프로젝트 디렉터리로 이동
ECR_URL=533267446521.dkr.ecr.ap-northeast-2.amazonaws.com IMAGE_TAG=v0.0.1 ./gradlew jib
```
<br/>

helm 차트 install
