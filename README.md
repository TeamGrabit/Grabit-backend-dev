# Backend Server to Develop

The backend server to develop Using Docker, Docker Compose, and AWS ECR.

### Prerequisites

- docker, docker-compose
- AWS CLI
- AWS credentials
- "grabit.env" file

### Setup

1. `git clone git@github.com:TeamGrabit/Grabit-backend-dev.git`
2. `cd Grabit-backend-dev`

### Deploy

- `docker-compose up -d`
- Run to Image from aws ECR: latest tag

### Destroy

- `docker-compose down`

</br>

# Additional Infomation

### grabit.env file

- This file is stored Github OAuth information such as client_id, client_secret, and redirect_uri.

### AWS Credentials for pulling images from ECR

- `aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS --password-stdin 476190904340.dkr.ecr.ap-northeast-2.amazonaws.com`
- "Login Succeeded" is printed

### Check to Server live

- `curl -l http://localhost:8080/api/actuator/health` is check to server live
- If server live, "{Status: UP}" is printed

### DB Image
- There is nothing in the inital DB because it uses MYSQL image.
- If you put the data in the DB, it will be saved to `grabit-db` directory.
- If delete `grabit-db` directory, data will be cleared.

