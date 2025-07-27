
# yuzi-ui-theme

一个用于微前端或多项目共享的主题样式 npm 包，支持 Vite/Vue/React 等现代前端项目，包含设计原子、基础样式、主题入口和 JS 变量。

## 目录结构
```
yuzi-ui-theme/
├── tokens/               # 设计原子（颜色、间距、圆角等变量）
├── base/                 # 基础样式（reset、typography）
└── dist/                 # 构建产物（主题入口、JS变量）
```

## 安装

```bash
npm install yuzi-ui-theme
```
或本地调试：
```bash
npm install /你的本地路径/yuzi-ui-theme
```

## 使用方法

### 1. 在入口文件引入主题样式

```js
// main.js 或 main.ts
import 'yuzi-ui-theme/dist/themes-light.css';
```

### 2. 按需引入原子样式

```js
import 'yuzi-ui-theme/tokens/colors.css';
import 'yuzi-ui-theme/tokens/spacing.css';
import 'yuzi-ui-theme/tokens/radii.css';
```

### 3. 在 Vue 组件/样式中使用 CSS 变量

```css
color: var(--brand-primary);
background: var(--gray-1);
```

### 4. 在 JS 中使用变量

```js
import { themeVars } from 'yuzi-ui-theme/dist/variables.js';
console.log(themeVars.colorBrandPrimary);
```

### 5. SCSS 支持

```scss
@import 'yuzi-ui-theme/dist/themes-light.scss';
```

## 设计规范

- 采用 Design Token 思路，便于统一管理和扩展。
- 支持 CSS、SCSS、JS 多种引用方式。

## 发布流程

1. 修改 `package.json` 信息。
2. 执行 `npm publish` 发布到 npm。

---

如需自定义主题或扩展变量，请在 `tokens` 目录下添加或修改相关文件。
