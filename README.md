这是一个**自包含的单文件 HTML 网页**，面向完全零基础的编程初学者——尤其是即将进入大学数学系（如 UCL Mathematics）的学生。
我在Claude Code, Gemini, 和deepseek的帮助下才完成的网页

不需要安装任何软件，用浏览器打开就能：
- 📚 阅读 7 大章节、25+ 小节的 Python 教程
- 🖥️ 在网页中**直接运行真正的 Python 代码**（基于 Pyodide / CPython 3.12 → WebAssembly）
- ✏️ 完成 10 道基础练习 + 6 道 Debug 纠错挑战
- 📥 下载 6 个 UCL 大一数学课可直接使用的 Python 工具

---

## ✨ 特性

| 特性 | 说明 |
|:--|:--|
| 🐍 **真实 Python 运行时** | Pyodide（CPython 3.12 编译到 WebAssembly），支持完整标准库 |
| 📱 **移动端优化** | 独立移动版，微信分享友好，iPad/手机触屏优化 |
| 🎨 **Apple 风格设计** | 毛玻璃导航、SF 字体栈、流畅动画、卡片式布局 |
| 📊 **SVG 图解** | 韦恩图、变量模型、条件分支图等可视化教学内容 |
| 🎓 **数学专区** | 数值微积分、蒙特卡洛模拟、牛顿迭代法、数论工具 |
| 📥 **可下载工具** | 6 个完整 `.py` 文件（数值方法、线性代数、统计、微积分、数论、绘图） |
| 🌐 **离线可读** | 所有文字内容不依赖网络，仅运行代码需联网加载 Pyodide |
| 🌍 **中英双语字体** | 系统原生字体栈，iOS/Android/Windows/macOS 完美渲染 |

---

## 📁 文件结构

```
Python/
├── python_tutorial.html          # 桌面版（119KB，侧边栏导航）
├── python_tutorial_mobile.html   # 移动版（68KB，顶部栏+抽屉菜单）
└── README.md                     # 本文件
```

两个文件内容相同，仅 UI 布局适配不同设备。

---

## 🚀 快速开始

### 方式一：直接打开（推荐）

1. 下载 `python_tutorial.html` 或 `python_tutorial_mobile.html`
2. 双击用浏览器打开
3. 等待左侧状态灯变为 🟢 **"Python 3.12 就绪"**
4. 开始学习！

### 方式二：微信分享

1. 将 `python_tutorial_mobile.html` 发送到微信
2. 接收方点击文件 → 选择"用浏览器打开"
3. 即可在手机上学习

### 方式三：GitHub Pages

```bash
git clone https://github.com/你的用户名/仓库名.git
# 将 python_tutorial.html  Push 到仓库
# 在 Settings → Pages 中启用 GitHub Pages
```

---

## 📚 课程大纲

| 章节 | 内容 | 练习 |
|:--|:--|:--|
| 🔰 **一、Python 基础** | 变量、数据类型、运算符、输入输出 | 4 道 |
| 🔀 **二、控制流程** | if/elif/else、for/while、break/continue | 2 道 |
| 📦 **三、数据结构** | 列表、字典、集合、字符串操作 | 1 道 |
| 🔧 **四、函数与模块** | def、参数、return、import | 1 道 |
| 📐 **五、进阶基础** | 列表推导式、Lambda、文件读写、异常处理 | 1 道 |
| 🏗️ **六、面向对象** | 类与对象（Vector2D 示例） | — |
| 🎓 **七、数学技能** | math 模块、数值微积分、蒙特卡洛、牛顿迭代 | 1 道 |
| 🐛 **进阶 Debug** | 6 道纠错挑战（类型/缩进/作用域/逻辑错误） | 6 道 |

---

## 🛠️ UCL 数学工具集

内嵌 6 个可下载的完整 Python 脚本，覆盖大一核心课程：

| 工具 | 内容 | 对应课程 |
|:--|:--|:--|
| `numerical_methods.py` | 牛顿法、二分法、数值积分 | MATH0003 Numerical Methods |
| `linear_algebra_utils.py` | 向量运算、矩阵乘法、高斯消元 | MATH0006 Linear Algebra |
| `statistics_utils.py` | 均值、方差、线性回归 | MATH0007 Statistics |
| `calculus_tools.py` | SymPy 符号微积分、泰勒展开 | MATH0004 Calculus |
| `number_theory.py` | Miller-Rabin 素性检测、RSA 演示 | 数论基础 |
| `function_plotter.py` | Matplotlib 函数可视化模板 | 数学绘图 |

每个文件都可直接在 IDLE / VS Code / PyCharm 中运行（`calculus_tools.py` 需 `pip install sympy`，`function_plotter.py` 需 `pip install matplotlib numpy`）。

---

## 🔧 技术栈

| 层 | 技术 |
|:--|:--|
| **内容** | 纯 HTML（无框架依赖） |
| **样式** | 原生 CSS（Apple 风格设计系统，CSS 变量 + 毛玻璃效果） |
| **交互** | 原生 JavaScript（无 jQuery/Vue/React） |
| **Python 运行时** | [Pyodide](https://pyodide.org) v0.26.1（CPython 3.12 → WebAssembly） |
| **字体** | 系统原生字体栈（`-apple-system` / `PingFang SC` / `Segoe UI`） |
| **代码高亮** | CSS 手动实现（`.syn-k` / `.syn-s` / `.syn-f` 等类名） |

### 为什么选择 Pyodide？

- ✅ 真正的 CPython，不是模拟器——`print`、`f"{x:.2f}"`、`import math`、`//` 整除……100% 兼容
- ✅ 支持完整 Python 标准库
- ✅ 可安装第三方包（NumPy、SymPy、Matplotlib）
- ❌ 首次加载 ~10MB（浏览器缓存后无需重新下载）

---

## 📱 移动端优化细节

移动版 (`python_tutorial_mobile.html`) 针对以下场景特别优化：

- **微信内置浏览器**：添加腾讯 X5 内核元标签
- **iPad Safari**：`viewport-fit=cover` + `safe-area-inset` 安全区域适配
- **触摸交互**：所有按钮最小 36px 触摸区域，移除悬停效果改用 `:active`
- **滑动体验**：`-webkit-overflow-scrolling: touch` 平滑滚动
- **字体加载**：不依赖 Google Fonts CDN，使用系统原生字体

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 待改进方向

- [ ] 添加更多数学可视化（Plotly 交互图表）
- [ ] 增加音视频讲解
- [ ] 支持 Pyodide 离线包（Service Worker 缓存）
- [ ] 添加学习进度云同步
- [ ] 多语言支持（English version）

### 本地开发

本项目是纯静态 HTML，无需构建工具。修改任一 `.html` 文件后直接用浏览器打开即可预览。

---

## 📄 许可证

MIT License © 2026

---

## 🙏 致谢

- [Pyodide](https://pyodide.org) — 让 Python 运行在浏览器中
- [UCL Mathematics](https://www.ucl.ac.uk/maths/) — 课程灵感来源
- 所有为 Python 教育做出贡献的开源社区
- Claude Code 和 deepseek的强大帮助

---

> Built with ❤️ for future mathematicians. 祝你学习顺利！🐍
> 
