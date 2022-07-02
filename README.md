# Backend Server to Develop

The backend server to develop Using Docker, Docker-Compose.

### Prerequisites

- docker, docker-compose
- "grabit.env" file

### Setup

1. `git clone git@github.com:TeamGrabit/Grabit-backend-dev.git`
2. `cd Grabit-backend-dev`

### Deploy

- `docker-compose up`
- Run to Image from public registry for development.

### Destroy

- `docker-compose down`

</br>

# Additional Infomation

### grabit.env file

- This file is stored Github OAuth information such as client_id, client_secret, and redirect_uri.

### Check to Server live

- `curl -l http://localhost:8080/api/actuator/health` is check to server live
- If server live, "{Status: UP}" is printed

### DB Image
- There is nothing in the inital DB because it uses MYSQL image.
- If you put the data in the DB, it will be saved to `grabit-db` directory.
- If delete `grabit-db` directory, data will be cleared.

