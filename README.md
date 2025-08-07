# YC Mind - 智能职业发展助手

YC Mind 是一个集成了 Dify AI 的智能职业发展助手，帮助用户发现职业机会、分析简历并提供个性化的职业建议。

## 功能特性

- 🤖 **AI 对话**: 基于 Dify 平台的智能对话功能
- 📄 **简历分析**: 上传 PDF 简历获得专业分析和建议
- 💬 **会话管理**: 保存和管理多个对话会话
- 🔐 **用户认证**: 简单的用户登录系统
- 📱 **响应式设计**: 适配各种设备屏幕

## 环境配置

### 1. 克隆项目并安装依赖

```bash
npm install
```

### 2. 配置 Dify API

创建 `.env` 文件并配置以下环境变量：

```env
# Dify API 配置
VITE_DIFY_API_KEY=app-your-api-key-here
VITE_DIFY_BASE_URL=https://api.dify.ai
VITE_DIFY_APP_ID=your-app-id-here
```

### 3. 获取 Dify API 密钥

1. 访问 [Dify 控制台](https://dify.ai)
2. 创建或选择一个应用
3. 在应用设置中找到 API 密钥
4. 将密钥复制到 `.env` 文件中

### 4. 启动开发服务器

```bash
npm run dev
```

## 项目结构

```
src/
├── components/          # React 组件
│   ├── ChatArea.tsx    # 聊天区域
│   ├── ChatInput.tsx   # 输入组件
│   ├── Header.tsx      # 头部组件
│   ├── LoginPrompt.tsx # 登录提示
│   └── Sidebar.tsx     # 侧边栏
├── config/             # 配置文件
│   └── dify.ts        # Dify 配置
├── hooks/              # 自定义 Hooks
│   └── useDify.ts     # Dify API Hook
├── services/           # 服务层
│   └── difyApi.ts     # Dify API 服务
├── types/              # TypeScript 类型定义
│   └── index.ts
└── App.tsx            # 主应用组件
```

## 主要功能

### AI 对话
- 支持流式响应，实时显示 AI 回复
- 自动保存对话历史
- 支持多轮对话上下文

### 简历分析
- 支持 PDF 文件上传
- AI 自动分析简历内容
- 提供改进建议和职业发展建议

### 会话管理
- 自动创建和保存会话
- 支持会话重命名和删除
- 本地存储会话历史

## 技术栈

- **前端框架**: React 18 + TypeScript
- **样式**: Tailwind CSS
- **图标**: Lucide React
- **构建工具**: Vite
- **AI 平台**: Dify

## 部署

### 构建生产版本

```bash
npm run build
```

### 预览生产版本

```bash
npm run preview
```

## 注意事项

1. **API 密钥安全**: 请确保不要将 API 密钥提交到版本控制系统
2. **CORS 配置**: 如果遇到跨域问题，请检查 Dify 应用的 CORS 设置
3. **文件上传**: 目前仅支持 PDF 格式的简历文件
4. **浏览器兼容性**: 建议使用现代浏览器以获得最佳体验

## 故障排除

### 常见问题

1. **API 连接失败**
   - 检查 API 密钥是否正确
   - 确认 Dify 服务是否正常运行
   - 检查网络连接

2. **文件上传失败**
   - 确认文件格式为 PDF
   - 检查文件大小是否超出限制
   - 验证 Dify 应用是否支持文件上传

3. **会话历史丢失**
   - 检查浏览器本地存储是否被清除
   - 确认用户是否已登录

## 贡献

欢迎提交 Issue 和 Pull Request 来改进这个项目。

## 许可证

MIT License