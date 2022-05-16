# Backend Server to Develop

The backend server to develop Using Docker, Docker Compose, and AWS ECR.

### Prerequisites

- docker, docker-compose
- AWS CLI
- AWS credentials

### Setup

1. `git clone git@github.com:TeamGrabit/Grabit-backend-dev.git`
2. `cd Grabit-backend-dev`

### Deploy

- `docker-compose up`
- Run to Image from aws ECR: latest tag

### Destroy

- `docker-compose down`

---

## Additional Infomation

### AWS Credentials for pulling images from ECR

- `aws ecr get-login-password --region ap-northeast-2 | docker login --username AWS --password-stdin 476190904340.dkr.ecr.ap-northeast-2.amazonaws.com`
- "Login Succeeded" is printed

### DB Image
- There is nothing in the inital DB because it uses MYSQL image.
- If you put the data in the DB, it will continue to be saved.
- **If you delete the image, the data disappears.**

