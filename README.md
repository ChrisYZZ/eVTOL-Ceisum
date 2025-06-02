# eVTOL-Ceisum
基于Cesium的城市eVTOL 3D可视化系统


<div align="center">
  <img src="https://img.shields.io/badge/Vue-3.5.13-green" alt="Vue">
  <img src="https://img.shields.io/badge/Vite-6.3.1-purple" alt="Vite">
  <img src="https://img.shields.io/badge/Cesium-Latest-blue" alt="Cesium">
  <img src="https://img.shields.io/badge/license-MIT-yellow" alt="License">
</div>

## 📋 项目简介

基于Vue 3 + Vite + Cesium构建的3D城市噪声监测可视化系统，旨在通过无人机飞行路径模拟和噪声传播建模，实现城市环境噪声的实时监测和可视化展示。

### ✨ 主要特性

- 🏙️ **3D城市模型** - 基于3DTiles的真实城市场景
- 🚁 **飞行路径模拟** - 无人机巡航路线可视化
- 🌡️ **噪声热力图** - 实时噪声分布展示
- 🎯 **多图层支持** - POI、热力图、噪声瓦片等
- 📊 **噪声分级** - 40-80分贝六级可视化
- 🌪️ **风场模拟**（计划中）- 粒子效果展示

## 🚀 快速开始

### 环境要求

- Node.js >= 16.0.0
- npm >= 7.0.0
- 现代浏览器（Chrome/Firefox/Edge最新版）

### 安装步骤

1. **克隆项目**
```bash
git clone https://github.com/yourusername/urban-noise-monitoring-3d.git
cd urban-noise-monitoring-3d
```

2. **安装依赖**
```bash
npm install
```

3. **配置资源文件**
   
   由于文件大小限制，以下资源需要单独配置：
   - 下载 [Cesium库文件](https://cesium.com/downloads/) 到 `public/Cesium/`
   - 下载 [项目资源包](链接待补充) 包含：
     - `GZ3dtile/` - 广州3D瓦片数据
     - `tiles/` - 噪声瓦片数据

4. **启动开发服务器**
```bash
npm run dev
```

5. **访问项目**
   
   打开浏览器访问 `http://localhost:5173`

## 📁 项目结构

```
├── public/
│   ├── Cesium/              # Cesium库文件（需单独下载）
│   ├── GZ3dtile/            # 3D城市瓦片数据
│   ├── tiles/               # 噪声瓦片数据
│   ├── cesium-heatmap-es6.umd.js
│   ├── CesiumDrone.glb     # 无人机模型
│   └── *.geojson            # 地理数据文件
├── src/
│   ├── components/
│   │   └── Map.vue          # 地图核心组件
│   ├── App.vue              # 应用主组件
│   ├── main.js              # 应用入口
│   └── style.css            # 全局样式
├── fastserver/              # Python后端（开发中）
├── vite.config.js           # Vite配置
└── package.json
```

## 🛠️ 技术栈

### 前端
- **Vue 3** - 渐进式JavaScript框架
- **Vite** - 下一代前端构建工具
- **Cesium** - 3D地球和地图可视化
- **cesium-heatmap-es6** - Cesium热力图插件
- **Axios** - HTTP客户端

### 后端（计划中）
- **FastAPI** - 现代Python Web框架
- **Python 3.9+** - 后端开发语言

## 📊 功能模块

### 已实现
- ✅ 3D城市场景加载与展示
- ✅ 无人机飞行路径动画
- ✅ POI点位标注
- ✅ 基础热力图渲染
- ✅ 多图层切换控制
- ✅ 噪声等级图例

### 开发中
- 🔧 FastAPI后端接口
- 🔧 实时噪声计算算法
- 🔧 噪声传播物理模型
- 🔧 风场粒子效果
- 🔧 GPU加速渲染优化

## 🔌 API文档

### 后端接口（规划中）

```python
GET  /api/flight-routes       # 获取飞行路线列表
POST /api/flight-routes       # 创建新飞行路线
GET  /api/noise-data          # 获取噪声数据
POST /api/noise/calculate     # 计算噪声分布
GET  /api/wind-field         # 获取风场数据
```

## 🚧 开发路线图

- **Phase 1** (当前)
  - [x] 基础3D场景搭建
  - [x] 飞行路径可视化
  - [ ] FastAPI后端框架

- **Phase 2** (2025 Q1)
  - [ ] 噪声传播算法实现
  - [ ] 实时数据处理
  - [ ] 数据持久化

- **Phase 3** (2025 Q2)
  - [ ] 风场效果集成
  - [ ] GPU加速优化
  - [ ] 多机协同展示

## 🤝 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 提交 Pull Request

### 开发规范

- 遵循 Vue 3 Composition API 规范
- 使用 ESLint 进行代码检查
- 提交信息遵循 Conventional Commits
- 保持代码注释清晰

## 📝 更新日志

### [0.1.0] - 2025-06-01
- 🎉 项目初始化
- ✨ 实现基础3D场景
- ✨ 添加飞行路径模拟
- ✨ 集成热力图功能

## 🐛 已知问题

- 远程访问时加载速度较慢（大型3DTiles数据）
- 热力图在数据量大时性能下降
- 噪声数据目前为模拟数据

## 📞 联系方式

- 项目维护者：[Chris Guo]
- Email：
- Issues：[GitHub Issues](https://github.com/yourusername/urban-noise-monitoring-3d/issues)

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- [Cesium](https://cesium.com/) - 3D地球可视化引擎
- [Vue.js](https://vuejs.org/) - 渐进式JavaScript框架
- [Vite](https://vitejs.dev/) - 前端构建工具

---

<div align="center">
  <p>如果这个项目对您有帮助，请给一个 ⭐️ Star！</p>
</div>
