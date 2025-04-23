# RAGFlow 部署教程

## 前置条件
在开始部署 RAGFlow 之前，请确保以下条件已满足：
- 已安装 Python 3.8 或更高版本。
- 已安装 Git。
- 已安装 Docker 和 Docker Compose。

## 步骤

### 1. 克隆项目代码
使用以下命令克隆 RAGFlow 的 Git 仓库：
```bash
git clone https://github.com/your-repo/ragflow.git
cd ragflow
```
- 若无法克隆 RAGFlow 的 Git 仓库则需要外部通过XFTP等工具导入然后cd ragflow到目录下

### 3. 配置环境变量

```bash
编辑文件 /etc/sysctl.conf
更改或加入 ：vm.max_map_count=262144
修改文件 docker/.env/
默认配置为： RAGFLOW_IMAGE=infiniflow/ragflow:v当前版本号-slim
修改为国内镜像： RAGFLOW_IMAGE=registry.cn-hangzhou.aliyuncs.com/infiniflow/ragflow:v当前版本号
进入Docker 文件 
![Uploading 91ba83d4-60a2-44c6-add1-06f045f274a9.png…]()

```
编辑 `.env` 文件，填写必要的 API 密钥和数据库连接信息。

### 4. 启动 Docker 服务
确保 Docker 服务已启动，然后运行以下命令启动所需的容器：
```bash
docker-compose up -d
```

### 5. 初始化数据库
运行以下命令以初始化数据库：
```bash
python3 manage.py migrate
```

### 6. 启动应用
运行以下命令启动 RAGFlow 应用：
```bash
python3 manage.py runserver
```
应用将默认运行在 `http://127.0.0.1:8000`。

### 7. 测试部署
打开浏览器访问 `http://127.0.0.1:8000`，确保应用正常运行。

## 常见问题
### 1. Docker 容器无法启动
- 检查 Docker 是否已正确安装并运行。
- 确保端口未被占用。

### 2. 数据库连接失败
- 检查 `.env` 文件中的数据库配置是否正确。
- 确保数据库服务已启动。

## 参考
- [RAGFlow 官方文档](https://example.com)
- [Docker 官方文档](https://docs.docker.com)
