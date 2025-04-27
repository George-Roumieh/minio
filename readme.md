# 🚀 MinIO Server - Local Setup

This guide helps you quickly run a **MinIO** server locally using Docker Compose.

## 📄 Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

## 📂 Project Structure

```bash
.
├── docker-compose.yml
├── minio-data/   # This folder will be created automatically to store your data
└── README.md
```

## 🛠️ How to Run

1. **Clone this repository** (if applicable) or make sure your `docker-compose.yml` is in a directory.

2. **Start the MinIO server**:
   
   ```bash
   docker-compose up -d
   ```

3. **Access MinIO**:
   - **Console UI**: [http://localhost:9001](http://localhost:9001)
   - **S3 API**: [http://localhost:9000](http://localhost:9000)

4. **Login Credentials**:
   - **Username**: `minioadmin`
   - **Password**: `minioadmin123`

## ⚙️ Configuration Details

- **Ports**:
  - `9000`: MinIO server (S3 API compatible)
  - `9001`: MinIO Web Console
- **Data Persistence**:
  - Data is stored locally inside the `./minio-data` folder.
- **Environment Variables**:
  - `MINIO_ROOT_USER` and `MINIO_ROOT_PASSWORD` set the admin credentials.

## 📛 How to Stop

To stop the running containers:

```bash
docker-compose down
```

If you also want to **remove volumes** (all stored data):

```bash
docker-compose down -v
```

## 📚 Useful MinIO Commands

- **View running containers**:
  ```bash
  docker ps
  ```
- **View logs**:
  ```bash
  docker-compose logs -f
  ```
