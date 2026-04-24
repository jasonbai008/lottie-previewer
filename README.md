# Lottie 动画预览器 (Lottie Previewer)

一个轻量级的、基于 Web 的 Lottie 动画预览工具，专门用于快速查看 `.lottie` 格式的文件。

## 🌟 功能特点

- **快速预览**：支持拖拽或点击上传 `.lottie` 文件进行即时预览。
- **响应式设计**：完美适配 PC 端和移动端，PC 端采用贯穿式设计，移动端全屏展示。
- **自动播放**：默认循环播放加载的动画。
- **本地加载**：通过 Blob URL 技术，无需上传服务器即可在浏览器中预览本地文件。

## 🚀 如何使用 Lottie 文件

使用 `.lottie` 文件非常简单，只需在 HTML 中通过 `@dotlottie/player-component` 引入：

### 1. 引入播放器脚本

```html
<!-- 引入官方 dotlottie-player 组件 -->
<script type="module" src="https://unpkg.com/@dotlottie/player-component@latest/dist/dotlottie-player.mjs"></script>
```

### 2. 基础使用

```html
<!-- 自动播放、循环播放 -->
<dotlottie-player
    src="hello.lottie"
    background="transparent"
    speed="1"
    style="width: 300px; height: 300px;"
    loop
    autoplay>
</dotlottie-player>
```

### 3. 参数说明

- **src**: `.lottie` 文件路径。
- **autoplay**: 是否自动播放。
- **loop**: 是否循环播放。
- **speed**: 播放速度。

## 🛠️ 技术细节

- **播放器**：集成了官方的 `@dotlottie/player-component`。
- **本地转换**：使用 `URL.createObjectURL(file) + '#.lottie'` 的技巧，将本地文件转换为播放器可识别的 URL，解决了某些情况下播放器无法识别 Blob 类型的问题。
- **兼容性**：支持主流现代浏览器（Chrome, Edge, Safari, Firefox）。

## 💻 本地运行

由于该项目是纯静态 HTML 页面，你可以通过以下方式运行：

1. **直接打开**：双击 `index.html` 即可运行。
2. **使用 Live Server**：在 VS Code 中右键点击 `index.html` 并选择 "Open with Live Server"（推荐，体验更佳）。

---

*由高级前端工程师精心打造，旨在提供最便捷的 Lottie 预览体验。*
