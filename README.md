# SG5 Digital Gauge

为 Subaru Forester SG5 制作的圆形数字仪表与像素风开机动画实验项目。

> 个人非官方项目，与 Subaru、Waveshare 无隶属或授权关系。目前界面数值均为模拟数据，不应替代原车仪表或安全警告。

## 预览

### 开机成功流程

![Boot success](media/boot-success.gif)

### 连接失败流程

![Boot failure](media/boot-failure.gif)

### 仪表界面

![Gauge preview](media/gauge-preview.png)

仪表设计包含：

- 转速、车速、节气门开度和温度显示
- 左右弧形能量槽
- `SYSTEM CHECK → CONNECTING → LIVE DATA` 开机流程
- 成功双闪、失败表情动画
- 480 × 480 圆形屏幕布局

## 当前状态

- 开机成功/失败动画：已在开发板上运行
- 仪表界面：已完成模拟数据版本
- 真实车辆 OBD 数据：尚未接入
- 发动机内部机械动画：暂停开发；实验代码仅供过程记录，不代表正确的机械仿真

## 硬件

- Waveshare ESP32-S3-Touch-LCD-2.1
- 480 × 480 ST7701 圆形 LCD
- ESP32-S3，16 MB Flash，8 MB OPI PSRAM
- Arduino ESP32 Core 3.0.7
- LVGL 8.3.10

## 目录

```text
firmware/
  SG5_Boot_Demo/              已验证的开机动画演示
  SG5_Gauge_V4_experimental/  仪表与发动机动效实验版本
media/                        README 使用的预览图和 GIF
docs/                         项目状态与说明
```

## 烧录提示

使用 Arduino IDE 打开对应目录内的 `.ino` 文件。开发板设置和已知限制见 [docs/STATUS.md](docs/STATUS.md)。

## 注意

- 代码当前只使用模拟车辆数据。
- 不发送改变 ECU 设置的指令。
- 驾驶中不要操作或调试设备。
- 视觉素材和车辆图像保留作者权利；第三方驱动与商标归各自权利人所有。
