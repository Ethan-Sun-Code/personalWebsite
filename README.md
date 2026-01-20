# 个人学术网站 & 博客

这是一个基于 Django (后端) + Vue 3 (前端) + MySQL (数据库) 的前后端分离项目。
项目使用 Docker 和 Docker Compose 进行容器化管理。

## 项目结构

- `backend/`: Django 后端代码
- `frontend/`: Vue 3 前端代码
- `docker-compose.yml`: Docker 编排文件

## 快速开始

### 前置要求

- 确保本地已安装 [Docker](https://www.docker.com/products/docker-desktop/) 和 Docker Compose。

### 运行项目

1. 打开终端，进入项目根目录。
2. 运行以下命令构建并启动容器：

   ```bash
   docker-compose up --build
   ```

3. 等待容器启动完成。

### 访问服务

- **前端页面**: [http://localhost:5173](http://localhost:5173)
- **后端 API**: [http://localhost:8000](http://localhost:8000)
- **Django 管理后台**: [http://localhost:8000/admin](http://localhost:8000/admin)

## 开发指南

### 后端 (Django)

后端运行在 `backend` 容器中。
如果需要安装新的 Python 包：
1. 修改 `backend/requirements.txt`。
2. 重新运行 `docker-compose up --build`。

### 前端 (Vue)

前端运行在 `frontend` 容器中。
代码修改后通常会自动热重载 (Hot Reload)。

### 数据库 (MySQL)

数据库数据持久化存储在 Docker Volume `db_data` 中。
连接信息配置在 `docker-compose.yml` 和 `backend/backend/settings.py` 中。
