# Overview
![image](images/overview.svg?raw=true "Overview") <br />
<br />
## 使用說明

### 1. Build docker image
```
docker build -t uploader docker
```
### 2. 存儲桶上的跨域資源共享 (CORS) 配置
```
gsutil cors set cors.txt gs://< GCS bucket >
```

### 3. 授予服務帳戶GCS存取權限,並下載金鑰,命名為 key.json

### 4. 修改docker-compose.yml
```
BUCKET_NAME: < GCS bucket >
```
### 5. 啟動uploader
```
docker-compose up -d
```

### 6. 訪問網頁
```
http://< IP >:8080
```
![image](images/example-1.jpg?raw=true "example-1") <br />
![image](images/example-2.jpg?raw=true "example-2") <br />