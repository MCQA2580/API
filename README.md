# RandomBeautyVideo 项目说明

## 项目简介

RandomBeautyVideo 是一个在线视频播放器网站，专注于提供随机视频内容的观看体验。网站采用现代化的前端技术构建，具有响应式设计，可在各种设备上良好显示。

## 核心功能

### 视频播放
- 随机视频播放功能
- 自动播放下一个视频
- 视频循环播放选项
- 全屏播放支持
- 视频完整显示，无裁剪问题

### 统计功能
- 观看次数计数
- 下载次数计数
- 分享次数计数
- 本地存储，数据持久化

### 收藏管理
- 视频收藏/取消收藏
- 收藏列表管理
- 收藏视频快速播放
- 批量删除收藏

### 历史记录
- 自动记录观看历史
- 历史记录管理
- 历史视频快速播放
- 批量清除历史

### 分享功能
- 支持Web Share API
- 复制链接到剪贴板
- 分享成功后自动计数

### 下载功能
- 视频下载支持
- 下载成功后自动计数

## 技术特点

### 前端技术
- **HTML5**：使用最新的HTML5视频标签
- **CSS3**：应用CSS3特性，如渐变、阴影、动画等
- **JavaScript**：使用现代JavaScript语法
- **响应式设计**：支持各种屏幕尺寸

### 性能优化
- **本地存储**：使用localStorage存储用户数据
- **内联CSS/JS**：减少HTTP请求，提高加载速度
- **代码压缩**：优化代码结构，减少文件大小
- **懒加载**：视频按需加载，节省带宽

### 用户体验
- **现代化界面**：采用深色主题，视觉效果出色
- **流畅动画**：添加了各种微交互和动画效果
- **错误处理**：完善的错误处理机制
- **加载状态**：清晰的加载状态提示

## 项目结构

```
API/
├── index.html          # 主页面
├── assets/             # 资源文件夹
│   ├── style.css       # 样式文件（已内联到HTML）
│   └── f.txt           # 其他资源
└── README.md           # 项目说明文件
```

## 使用方法

### 本地部署
1. 下载项目文件到本地
2. 使用现代浏览器打开 `index.html` 文件
3. 开始使用网站功能

### 服务器部署
1. 将项目文件上传到网站服务器
2. 确保服务器支持静态文件访问
3. 通过域名访问网站

## 配置说明

### 视频API地址
默认视频API地址为：
```javascript
https://api.mmp.cc/api/ksvideo?type=mp4&id=jk
```

如需修改API地址，请编辑 `index.html` 文件中的以下部分：
```javascript
function playNext() {
    loading.style.display = 'block';
    errorMessage.style.display = 'none';
    player.src = 'https://api.mmp.cc/api/ksvideo?type=mp4&id=jk&_t=' + Math.random();
    player.play().catch(err => {
        console.error('播放失败:', err);
        errorMessage.style.display = 'block';
    });
}
```

同时修改HTML中的初始视频地址：
```html
<video id="player" src="https://api.mmp.cc/api/ksvideo?type=mp4&id=jk" controls webkit-playsinline playsinline></video>
```

## 浏览器兼容性

- **Chrome**：支持
- **Firefox**：支持
- **Safari**：支持
- **Edge**：支持
- **Opera**：支持

## 响应式支持

- **桌面端**：最佳体验，充分利用宽屏空间
- **平板设备**：自动调整布局，保持良好体验
- **移动设备**：优化触摸交互，适配小屏幕

## 注意事项

1. 本项目使用本地存储存储用户数据，请确保浏览器支持localStorage
2. 视频播放功能依赖于HTML5视频标签，请使用现代浏览器
3. 分享功能在不同浏览器中可能有不同表现
4. 请确保网络连接正常，以获得最佳视频播放体验

## 许可证

本项目仅供学习和参考使用，请勿用于商业用途。

## 更新日志

### v1.0.0
- 初始版本发布
- 实现核心视频播放功能
- 添加统计功能
- 实现收藏和历史记录功能
- 优化响应式设计
- 修复视频显示不全问题

---

**RandomBeautyVideo** - 发现每一刻的美好，感受视觉的极致体验