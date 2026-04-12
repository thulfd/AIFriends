# AIFriends

一个基于 AI 的社交平台 Web 应用，支持创建 AI 角色、与角色聊天、语音交互等功能。

## 技术栈

### 前端
- **Vue 3** - 渐进式前端框架
- **Vite** - 快速构建工具
- **Tailwind CSS + DaisyUI** - 原子化 CSS 框架
- **Pinia** - 状态管理
- **Vue Router** - 路由管理
- **Axios** - HTTP 客户端
- **VAD Web** - 语音活动检测
- **Croppie** - 图片裁剪

### 后端
- **Django 6** - Python Web 框架
- **Django REST Framework** - RESTful API
- **SimpleJWT** - JWT 认证
- **SQLite** - 轻量级数据库

## 项目结构

```
AIFriends/
├── backend/                 # Django 后端
│   ├── backend/            # 项目配置
│   └── web/              # 应用代码
├── frontend/              # Vue 前端
│   ├── src/
│   │   ├── components/   # 公共组件
│   │   ├── views/       # 页面视图
│   │   ├── stores/     # Pinia 状态
│   │   ├── router/    # 路由配置
│   │   └── js/        # 工具函数
│   └── public/         # 静态资源
└── README.md
```

## 功能特性

- 用户账户（登录/注册）
- 创建 AI 角色
- 与角色聊天
- 语音输入
- 用户资料管理
- 响应式设计

## 快速开始

### 前置要求

- Node.js >= 20.19.0
- Python >= 3.10
- pip

### 安装

```bash
# 1. 安装后端依赖
cd backend
pip install -r requirements.txt

# 2. 安装前端依赖
cd ../frontend
npm install
```

### 运行

#### 开发模式（推荐）

```bash
# 终端1：启动后端
cd backend
python manage.py runserver

# 终端2：启动前端
cd frontend
npm run dev
```

- 前端：http://localhost:5173
- 后端：http://127.0.0.1:8000

#### 生产模式

```bash
# 构建前端
cd frontend
npm run build

# 启动后端
cd ../backend
python manage.py runserver
```

访问 http://127.0.0.1:8000

## API 端点

| 端点 | 方法 | 描述 |
|------|------|------|
| `/api/token/` | POST | 获取 JWT Token |
| `/api/token/refresh/` | POST | 刷新 Token |

## 许可证

MIT