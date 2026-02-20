# 🐍 Snake Game Enhanced

> 基于 HTML5 Canvas 的经典贪吃蛇游戏，支持多模式、iPad 触摸控制、滑动手势和响应式设计

![Snake Game](https://img.shields.io/badge/Snake-Game-HTML5%2BCanvas-green?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![Deployment](https://img.shields.io/badge/Vercel-Deployed-black?style=flat-square)

---

## 🎮 功能特性

### 游戏模式
- **Classic** - 经典模式（撞墙或撞自己死亡）
- **No Walls** - 无墙模式（穿墙不死亡）
- **Obstacles** - 障碍模式（随机生成障碍，难度增加）
- **Endless** - 无尽模式（不会死亡）

### 速度设置
- **Slow** - 适合新手，移动速度慢
- **Medium** - 标准速度
- **Fast** - 挑战高玩，移动速度快

### 画布尺寸
- **Small** - 300x300（手机端）
- **Medium** - 400x400（标准）
- **Large** - 600x600（大屏）

### 控制方式
- **PC/Mac** - 键盘方向键（↑ ↓ ← →）或 WASD
- **iPad/iPhone** - 虚拟 D-pad 触摸按钮
- **手势控制** - 在 Canvas 上滑动控制方向
- **响应式** - 自动适配 portrait/landscape

### 性能优化
- **LocalStorage** - High Score 本地持久化
- **requestAnimationFrame** - 平滑的动画循环
- **触摸优化** - 防止双击缩放和意外滚动

---

## 🚀 在线体验

### Vercel 部署
**访问链接**: https://snake-game-rust-three.vercel.app

### GitHub Pages（备用）
**访问链接**: https://jiangbingo.github.io/snake-game/

---

## 🎯 如何游玩

### 开始游戏
1. 点击 **START** 按钮开始游戏
2. 使用方向键或触摸控制蛇的移动方向
3. 吃到食物（红色方块）得分，蛇会变长
4. 撞到墙壁、障碍物或自己则游戏结束

### 控制说明

#### PC/Mac
- **方向键**: ↑ ↓ ← →
- **WASD**: W A S D

#### iPad/iPhone
- **虚拟方向键**: 点击 ↑ ↓ ← → 按钮
- **滑动控制**: 在 Canvas 上向上下左右滑动
- **多点触摸**: 支持同时操作多个按钮

#### 游戏模式
- **Classic**: 撞墙或撞自己死亡
- **No Walls**: 撞墙不死亡（穿墙）
- **Obstacles**: 随机生成障碍，需要避开
- **Endless**: 不会死亡，适合休闲游玩

---

## 💻 技术栈

- **HTML5** - Canvas API
- **CSS3** - Flexbox、媒体查询、动画
- **JavaScript** - ES6+、LocalStorage API
- **Performance** - requestAnimationFrame、触摸优化

---

## 📱 响应式设计

### iPad Portrait（竖屏）
- 画布大小：90vw × 90vw
- 虚拟按键：70px × 70px
- 字体大小：18px

### iPad Landscape（横屏）
- 画布大小：70vw × 70vw
- 虚拟按键：90px × 90px
- 字体大小：20px

### 桌面端（> 768px）
- 画布大小：400px × 400px（默认）
- 虚拟按键：80px × 80px
- 字体大小：16px

---

## 🛠️ 本地开发

### 克隆项目
```bash
git clone https://github.com/jiangbingo/snake-game.git
cd snake-game
```

### 运行游戏
```bash
# 使用本地服务器
python -m http.server 8000

# 或使用 PHP
php -S localhost:8000

# 或使用 Node.js
npx serve .

# 然后在浏览器打开
open http://localhost:8000
```

---

## 📊 游戏策略

### 得分系统
- **基础分**: 每吃一个食物 +10 分
- **High Score**: 自动保存到 LocalStorage
- **挑战模式**: 尝试在 Fast 模式下获得更高分数

### 不同模式攻略
- **Classic**: 控制蛇的长度，不要撞墙
- **No Walls**: 利用穿墙特性快速移动
- **Obstacles**: 优先避开障碍物，然后寻找食物
- **Endless**: 放松游玩，专注于收集食物

---

## 🔧 自定义设置

### 修改游戏参数
编辑 `index.html` 中的 `config` 对象：

```javascript
const config = {
    speeds: {
        slow: { fps: 8, interval: 150 },    // 修改 fps 和 interval 调整速度
        medium: { fps: 15, interval: 67 },
        fast: { fps: 25, interval: 40 }
    },
    sizes: {
        small: { width: 300, height: 300 },  // 修改画布尺寸
        medium: { width: 400, height: 400 },
        large: { width: 600, height: 600 }
    }
};
```

### 修改颜色主题
编辑 `index.html` 中的 CSS：

```css
body {
    background-color: #1a1a1a;  /* 修改背景色 */
    color: #00ff00;  /* 修改文字色 */
}

#gameCanvas {
    border: 3px solid #00ff00;  /* 修改边框色 */
    box-shadow: 0 0 20px rgba(0, 255, 0, 0.3);  /* 修改阴影 */
}
```

---

## 📝 更新日志

### v1.0.0 (2026-02-20)
- ✅ 初始发布
- ✅ 4 种游戏模式
- ✅ 3 种速度设置
- ✅ 3 种画布尺寸
- ✅ iPad 触摸控制
- ✅ 滑动手势控制
- ✅ 响应式设计
- ✅ 本地 High Score

---

## 🤝 贡献

欢迎贡献！请随时提交 Issue 或 Pull Request。

### 如何贡献
1. Fork 本项目
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

### 建议的改进方向
- 🎨 添加更多主题（暗黑模式、赛博朋克等）
- 🎵 添加音效和背景音乐
- 🐍 添加不同蛇的皮肤
- 🏆 添加在线排行榜
- 📊 添加游戏统计数据
- 🔧 添加难度自适应

---

## 📄 License

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

---

## 👨‍💻 开发者

**Bingo** - [GitHub](https://github.com/jiangbingo) - [Email](mailto:jiangbingo@hotmail.com)

---

## 🙏 致谢

- 感谢所有测试和提供建议的用户
- 感谢开源社区的贡献
- 感谢 HTML5 Canvas 技术支持

---

## 📮 联系方式

- **GitHub**: https://github.com/jiangbingo/snake-game/issues
- **Email**: jiangbingo@hotmail.com

---

**开始游玩吧！🐍**
