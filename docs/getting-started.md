# 快速开始
## 安装
通过 npm 或 yarn 命令安装 
```bash
# npm
npm install klinecharts klinecharts-pro

# yarn
yarn install klinecharts klinecharts-pro
```
如果是直接通过 script 标签引入，可以使用下面两个 CDN 中的任意一个即可
::: warning 注意
对于生产环境，推荐使用一个明确的版本号，以避免新版本造成的不可预期的破坏。
:::

```html
<!-- unpkg -->
<script src="https://unpkg.com/@klinecharts/pro/dist/klinechartspro.umd.js"></script>

<!-- jsdelivr -->
<script src="https://cdn.jsdelivr.net/@klinecharts/pro/dist/klinechartspro.umd.js"></script>
```

## 使用
### 第一步，创建容器
```html
<div id="container"></div>
```
### 第二步，创建实例
在使用npm, yarn等包管理器中项目中
```javascript
// 引入
import { KLineChartPro, DefaultDatafeed } from 'klinecharts-pro'

// 创建实例
const chart = new KLineChartPro({
  container: document.getElementById('container'),
  // 这里使用默认的数据接入，如果实际使用中也使用默认数据，需要去 https://polygon.io/ 申请 API key
  datafeed: new DefaultDatafeed(`${polygonIoApiKey}`)
})
```

在直接通过 script 标签引入的项目中
```html
<script src="https://cdn.jsdelivr.net/@klinecharts/pro/dist/klinechartspro.umd.js"></script>
<script>
  // 创建实例
  const chart = new klinechartspro.KLineChartPro({
  container: document.getElementById('container'),
  // 这里使用默认的数据接入，如果实际使用中也使用默认数据，需要去 https://polygon.io/ 申请 API key
  datafeed: new klinechartspro.DefaultDatafeed(`${polygonIoApiKey}`)
})
</script>
```
第一个图表就创建完成了