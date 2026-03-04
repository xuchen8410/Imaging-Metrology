DAQ = 把各种传感器信号（光、电、温度、振动等）实时采集 → 变成数字数据 → 分析系统性能 --- Data acquisition is the process of collecting physical sensor signals, converting them into digital data, and recording them for analysis.
光学系统里，DAQ就是 “所有测试数据的入口”。
## 1. Main Purpose in Imaging Systems
DAQ systems are used for:
- Optical system performance testing
- Environmental testing (thermal / vibration)
- Flight test telemetry
- Hardware-in-the-loop validation
  #####
| 用途      | 说明           |
| ------- | ------------ |
| 系统测试    | 测试光学系统是否达到指标 |
| 环境测试    | 振动、温度对光学影响   |
| 飞行/地面遥测 | 记录系统运行状态     |

## 2. Typical Signals Collected

In imaging EO optical systems, DAQ collects synchronized measurements from multiple sensors.

| Sensor Type | Measurement |
|-------------|-------------|
| Photodiode | Optical power |
| CCD / IR detector | Image signal |
| Thermocouple | Temperature |
| Strain gauge | Structural deformation |
| Accelerometer | Vibration |
| Voltage monitor | Power stability |

DAQ采集的信号

| 传感器               | 采的数据  |
| ----------------- | ----- |
| Photodiode        | 光功率   |
| CCD / IR detector | 图像信号  |
| Thermocouple      | 温度    |
| Strain gauge      | 结构形变  |
| Accelerometer     | 振动    |
| Voltage monitor   | 电源稳定性 |
