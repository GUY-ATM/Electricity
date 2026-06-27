# 福建财经政法大学宿舍电量查询

<div align="center">

一个简洁高效的宿舍电量查询与数据分析应用

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Android%20%7C%20iOS-lightgrey.svg)](https://github.com)

</div>

## 📖 项目简介

福建财经政法大学宿舍电量查询是一款专为在校大学生设计的宿舍用电管理应用。通过简单的房间信息输入，即可实时查询剩余电量，并自动记录历史数据，生成趋势图表，帮助同学们合理规划用电，避免突然断电的尴尬情况。

<img width="270" height="600" alt="微信图片_20260627165026_359_13" src="https://github.com/user-attachments/assets/5a39981e-af07-43c7-97d8-15dcab32db50" />
<img width="270" height="600" alt="微信图片_20260627165025_358_13" src="https://github.com/user-attachments/assets/f0c127f8-7ee6-48a8-819d-35e801881d2b" />
<img width="270" height="600" alt="微信图片_20260627165220_361_13" src="https://github.com/user-attachments/assets/5fe2c67b-b1da-4b84-a1a7-14209b470018" />

## ✨ 功能特性

### 核心功能

- 🔍 **实时电量查询** - 快速查询宿舍剩余电量
- 📊 **历史数据追踪** - 自动保存近30天的电量记录
- 📈 **可视化图表** - 支持折线图和柱形图展示电量趋势
- 💾 **智能记忆** - 自动保存上次查询的房间信息
- 🏠 **多房间支持** - 不同房间的数据独立存储

### 用户体验

- 🎨 简洁现代的 UI 设计
- 📱 流畅的移动端体验
- 🔄 自动数据缓存
- ⚡ 快速响应，低流量消耗

## 🛠️ 技术栈

- **前端框架**: UniApp
- **开发工具**: HBuilder X
- **图表库**: Chart.js
- **样式**: 原生 CSS + 自定义样式
- **图标**: Font Awesome
- **数据存储**: LocalStorage / uni.setStorageSync

## 📦 项目结构

```
宿舍电量2/
├── index.html              # 主页面
├── manifest.json           # 应用配置文件
├── img/                    # 图片资源
│   ├── 1.png
│   └── 2.png
├── js/                     # JavaScript 库
│   ├── chart.umd.min.js    # Chart.js 图表库
│   └── tailwindcss.js      # Tailwind CSS
├── libs/                   # 第三方库
│   ├── css/               # Font Awesome 样式
│   ├── webfonts/          # Font Awesome 字体
│   ├── forge.min.js       # 加密库
│   └── jsencrypt.min.js   # RSA 加密库
└── unpackage/              # 打包输出目录
    └── release/
        └── apk/
            └── 福建财经政法大学电量分析.apk  # Android 安装包
```

## 🚀 快速开始

### 前置要求

- 已安装 [HBuilder X](https://www.dcloud.io/hbuilderx.html)（推荐）
- 或任何支持静态网页开发的 IDE

### 安装步骤

1. **克隆项目**
   ```bash
   git clone https://github.com/your-username/dormitory-electricity.git
   cd dormitory-electricity
   ```
2. **使用 HBuilder X 运行**
   - 打开 HBuilder X
   - 选择 `文件` -> `导入` -> `从本地目录导入`
   - 选择项目文件夹
   - 点击 `运行` -> `运行到浏览器` 或 `运行到手机或模拟器`
3. **或直接使用浏览器打开**
   ```bash
   # 直接打开 index.html 文件即可
   ```

### APK 安装

如需直接在手机上使用，可直接安装：

- Android: `unpackage/release/apk/福建财经政法大学电量分析.apk`

## 📱 使用指南

1. **输入房间信息**
   - 填写楼号（1-13 号楼会自动映射）
   - 填写楼层
   - 填写房间号
2. **查询电量**
   - 点击"获取电量"按钮
   - 等待查询结果显示
3. **查看趋势**
   - 查询成功后会自动保存数据
   - 切换折线图/柱形图查看历史趋势
   - 数据保存 30 天
4. **自动记忆**
   - 下次打开会自动加载上次查询的房间信息

## 🔧 配置说明

当前代码中，1-13 号楼会自动映射为 28-40：

```javascript
function getMappedBuilding(inputBuilding) {
    const num = parseInt(inputBuilding, 10);
    if (num >= 1 && num <= 13) {
        return num + 27; // 1号楼->28, 2号楼->29, ...
    }
    return inputBuilding;
}
```

可根据实际情况修改映射规则。

## 🤝 贡献指南

欢迎所有形式的贡献！

### 如何贡献

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 提交 Pull Request

### 代码规范

- 保持代码简洁清晰
- 添加必要的注释
- 遵循现有的代码风格

## 📝 更新日志

### v1.0 (当前版本)

- ✅ 基础电量查询功能
- ✅ 30天历史数据存储
- ✅ 图表可视化展示
- ✅ 自动房间信息记忆
- ✅ 支持折线图和柱形图切换

## 🐛 已知问题

- 暂无已知问题

如发现问题，欢迎提交 [Issue](https://github.com/your-username/dormitory-electricity/issues)。

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

***

<div align="center">

**⭐ 如果这个项目对你有帮助，请给一个 Star ⭐**

</div>
