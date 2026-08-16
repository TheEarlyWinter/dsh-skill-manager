# dsh-skill-manager (📖 技能管理器)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub release](https://img.shields.io/github/v/release/TheEarlyWinter/dsh-skill-manager?color=orange)](https://github.com/TheEarlyWinter/dsh-skill-manager/releases)
[![DeepSeek Harness](https://img.shields.io/badge/DeepSeek%20Harness-Plugin-brightgreen)](https://github.com/deepseek-ai/deepseek-harness)

为 [DeepSeek Harness (dsh)](https://github.com/deepseek-ai/deepseek-harness) Web GUI 提供的轻量纯粹版**技能包管理器（Skill Manager）**插件。

> **致谢与上游说明**：
> 本插件基于 [statem-li/Kr-DSH](https://github.com/statem-li/Kr-DSH) 中的 `dsh-usage-skill` 进行精简重构，剥离了与技能管理无关的用量/余额监控逻辑，仅专注于提供干净、纯粹、好用的技能（Skill）与技能包（Bundle）可视化管理功能。

---

## ✨ 功能特性

- 📖 **侧边栏独立入口**：在 DSH 侧边栏底部添加独立的「📖 技能」按钮，告别杂乱。
- 📦 **技能包（Bundle）分组管理**：支持新建、重命名、删除自定义技能包，随心分类与批量开关。
- 🧩 **散装技能与拖拽安装**：支持浏览已安装的所有本地 Skill，支持拖拽安装新的技能包。
- 🌐 **原生双语支持**：中文 / 英文跟随 DSH 语言设置自动切换。
- 🚀 **开箱即用**：零额外配置，即装即用。

---

## 📦 安装方法

### 方式一：克隆到本地插件目录安装（推荐）

1. 将本项目克隆或下载到本地 profile 的 `node_modules` 目录：
   ```bash
   # Windows 默认路径示例
   cd %USERPROFILE%\.dsh\profiles\node_modules
   git clone https://github.com/TheEarlyWinter/dsh-skill-manager.git
   ```

2. 在 `%USERPROFILE%\.dsh\profiles\web\cordis.patch.yml` 中添加插件配置：
   ```yaml
   - insert:
       - id: skill-manager
         name: dsh-skill-manager
   ```

3. 重启 `dsh web` / 客户端，并在浏览器页面按下 `Ctrl + F5` 强制刷新即可！

---

## 🛠️ 项目结构

```
dsh-skill-manager/
├── lib/
│   ├── client.js       # Web 前端 UI 渲染（侧边栏按钮与技能管理面板）
│   └── index.js        # Node 服务端技能管理 API 路由
├── cordis.patch.yml    # DSH Cordis 插件注册声明
├── package.json
├── README.md
└── LICENSE
```

---

## 📄 License & Attribution

- 本项目基于 [MIT License](./LICENSE) 开源。
- 核心技能管理器逻辑衍生自上游开源项目 [statem-li/Kr-DSH](https://github.com/statem-li/Kr-DSH)。感谢原作者 [statem-li](https://github.com/statem-li) 的开源贡献！
