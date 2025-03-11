# Docker

## Kali 安裝 Docker

### 更新套件
```
sudo apt update
```

### 安裝 docker.io 
```
sudo apt install -y docker.io
```

### 執行 docker
```
sudo systemctl enable docker --now
```

### 加入 dcoker 權限
```
sudo usermod -aG docker $USER
newgrp docker
```

### 測試權限
```
docker images
```

### 安裝 dvwa
```
docker run -it –p 80:80 vulnerables/web-dvwa
```

### 執行 dvwa
```
docker run -p 80:80
```

### dvwa
```
http://localhost/
```

### 進入容器
```
docker exec -it 容器id /bin/bash
```

### 輸入帳號密碼
```
    admin / password
```

### 設定預設 mysql 帳號密碼
```
    Create / Reset Database
```