# 烽火台 GPS异常实时监控 V6.6.24

美团配送烽火台（peisong.meituan.com）GPS 异常实时监控用户脚本。

## 功能
- 实时监控订单配送流程 GPS 点位
- 超 300 米异常报警（严格大于）
- 北京时间分段限速（晨界 / 昼界 / 夜界）
- 多标签页主从选举，避免重复请求
- 身份核实保护与恢复
- 历史补扫、对账、超时单监控
- 面板 UI、CSV 导出、语音/通知

## 安装
1. 安装 [Tampermonkey](https://www.tampermonkey.net/) 或 Violentmonkey。
2. 打开此仓库的原始脚本链接（或下载 `GPS-monitor.user.js`）。
3. 在扩展中新建脚本，粘贴内容，或直接安装。

原始安装链接（启用后可一键更新）：
```
https://raw.githubusercontent.com/xyzdy111zxyzqf-blip/meituan-gps-monitor/main/GPS-monitor.user.js
```

## 使用
- 在烽火台页面加载后，按提示输入启动密码（24 小时授权）。
- 面板可拖动、折叠。
- 全局 API：`GPSMonitor.start()` / `GPSMonitor.stop()` / `GPSMonitor.status()` 等。

## 说明
- 仅匹配 `https://peisong.meituan.com/*`。
- 请求限速按北京时间自动调整。
- 核心业务规则（300 米阈值、报警确认等）为只读基线，不随世界切换改变。
- 本版本基于 V6.6.16 修复稿，语法已通过 Node 检查。

## 注意
此脚本仅供个人学习与内部监控使用，请遵守平台规则，勿用于任何违规用途。
