# ui-theme

一个用于微前端或多项目共享的主题样式npm包，包含设计原子、基础样式、主题入口和JS变量。

## 目录结构
```
shared-ui-commons/
├── tokens/               # 设计原子
│   ├── colors.css        # 品牌色变量
│   ├── spacing.css       # 边距规范
│   └── radii.css         # 圆角变量
├── base/                 # 基础样式
│   ├── reset.css         # 样式重置
│   └── typography.css    # 字体规范
└── dist/                 # 构建产物
    ├── themes-light.css  # 完整主题入口
    └── variables.js      # JS版变量（供JS使用）
```

## 使用方法

### 1. 安装
```bash
npm install ui-theme
```

### 2. 在项目中引入主题样式
```css
@import 'ui-theme/shared-ui-commons/dist/themes-light.css';
```

### 3. 在JS中使用变量
```js
import { themeVars } from 'ui-theme/shared-ui-commons/dist/variables.js';
console.log(themeVars.colorBrandPrimary);
```

## 设计规范
- 所有变量均采用 Design Token 思路，便于统一管理和扩展。
- 支持 CSS、JS 两种引用方式。

## 发布
1. 修改 `package.json` 信息。
2. 执行 `npm publish` 发布到 npm。

---
如需自定义主题或扩展变量，请在 `tokens` 目录下添加或修改相关文件。
