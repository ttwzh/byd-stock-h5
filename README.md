# 比亚迪 2023 后复权行情复盘（移动端 H5）

基于 `比亚迪后复权历史行情数据.xlsx`（2023 全年 242 个交易日）的复盘分析，
以移动端 H5 静态页面呈现「分析过程 + 结果」，UI 采用 TDesign Mobile 风格，图表用 ECharts。

## 快速运行

```bash
cd byd-stock-h5
python3 -m http.server 8123
# 浏览器打开 http://localhost:8123/index.html
```

> 直接双击 index.html 会因 fetch 本地 JSON 被浏览器拦截，请走本地 http 服务。

## 目录结构

```
byd-stock-h5/
├── AGENTS.md              # 背景信息 + 技术选型约束（必读）
├── README.md
├── index.html             # 单文件 H5（TDesign 风格 + ECharts）
├── data/byd_2023.json     # 预处理后的统计/月度/K线数据
└── assets/
    ├── echarts.min.js     # 本地 ECharts 5.4.3
    └── screenshot.png     # 移动端页面截图
```

## 核心结论

| 指标 | 数值 |
|---|---|
| 全年后复权收益 | **-23.43%**（261.73 → 200.40） |
| 年内最高 / 最低 | 307.38（02-02）/ 185.25（12 月） |
| 最强 / 最弱单日 | +6.46%（02-01）/ -5.18%（11-24） |
| 年化波动率 | 26.42% |
| 涨 / 跌天数 | 102 / 140 |
| 最佳 / 最差月份 | 1 月 +11.41% / 11 月 -16.16% |

> 仅为历史数据复盘，不构成投资建议。
