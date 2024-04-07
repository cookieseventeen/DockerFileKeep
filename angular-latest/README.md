# Angular 最後一主要版本

儲存改過的 dockerFile

## dockerfile 的目錄下 build image 並 tag 為字的帳號

```
docker image build --tag ckman18/angular-latest .
```

## 在想開發的地方啟 container 連結本地路徑到 container 路徑$PWD:/var/sandbox

```
docker run -d -it -v $PWD:/var/sandbox --name angular-latest ckman18/angular-latest
```

## 同上，差別利用環境變數指定版本

```
docker build --build-arg NODE_VERSION=14.21.3 --build-arg ANGULAR_CLI_VERSION=11.0.7 -t neux-angular .
```

## dockerfile 的目錄下 build image 並 tag 為自己的帳號

```
docker image build --tag ckman18/angular-latest . 
```

## push 到自己的 Hub

```
docker push ckman18/angular-latest
```
