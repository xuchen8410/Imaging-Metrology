```text
Sensor Input
  ├─ LWIR wide-FOV stream
  ├─ MWIR narrow-FOV stream
  ├─ Optional visible / laser / IMU
  ↓
Radiometric & Image Correction
  ├─ NUC / gain-offset correction
  ├─ bad-pixel correction
  ├─ denoise
  ├─ local contrast enhancement
  └─ multi-band registration
  ↓
Target Detection
  ├─ full-frame thermal candidate detection
  ├─ clutter suppression
  └─ candidate ROI extraction
  ↓
Tracking
  ├─ track initialization
  ├─ KCF / Kalman / DeepSORT / JPDA
  ├─ track maintenance
  └─ re-detection on target loss
  ↓
Discrimination / Classification
  ├─ spectral features
  ├─ spatial morphology features
  ├─ temporal motion features
  ├─ context features
  └─ rule-based / ML / deep fusion classifier
  ↓
Decision Output
  ├─ target type
  ├─ confidence
  ├─ trajectory
  ├─ threat level
  └─ handoff to operator / fire-control / higher-level fusion

```

## Thermal Imaging Sensors Comparison

| Sensor | Size | Weight | Resolution | Frame Rate | Radiometric | Power | Platform | Cost | Year |
|------|------|------|------|------|------|------|------|------|------|
| Thermal-Eye 2000B | 282×279×290 mm | 4.54 kg | 320×240 | 12.5 Hz | No | 28 W | UGV | n/a | early |
| Gobi-640-GigE | 49×49×79 mm | 263 g | 640×480 | 50 Hz | No | 4.5 W | UGV | n/a | 2008 |
| Miricle 307K | 45×52×48 mm | 95 g | 640×480 | 15 Hz | No | 3.3 W | UAV | n/a | 2006 |
| FLIR Tau2 | 44.5×44.5×30 mm | <70 g | 640×480 | 60 Hz | Yes | 1 W | UAV | $6500 | 2015 |
| FLIR A65 | 120×125×280 mm | 200 g | 640×512 | 30 Hz | Yes | 3.5 W | UAV | $7895 | 2016 |

| 参数          | 典型范围              | 结论                 |
| ----------- | ----------------- | ------------------ |
| Resolution  | 320×240 – 640×512 | UAV导航需要 ≥ VGA      |
| Frame rate  | 15–60 Hz          | SLAM需要更高帧率         |
| Weight      | 70 g – 4.5 kg     | UAV payload <800 g |
| Power       | 1–28 W            | 小型无人机需低功耗          |
| Radiometric | yes/no            | Radiometric更适合计算   |

### Infrared physics
Thermal sensors measure emitted radiation rather than reflected light.

Infrared wavelength range used:
8 – 15 µm

Key properties:
- emitted radiation depends on temperature
- emissivity affects measurement
- less affected by smoke / dust than visible light

### Discrimination feature
| Feature Category | Features |
|---|---|
| spectral | MWIR / LWIR intensity ratio |
| spatial | area, aspect ratio |
| temporal | flicker, heat variation |
| motion | velocity, acceleration |
| context | sky / ground background |

Models:
Constant Velocity Model
Constant Acceleration Model
Coordinated Turn Model
  
| Algorithm Category | Description | Typical Use |
|---|---|---|
| SLAM | map-based navigation using thermal features | autonomous navigation |
| Optical Flow | motion estimation between frames | odometry |
| Neural Networks | deep learning for perception | object detection |

### SLAM
| 技术                 | 说明               |
| ------------------ | ---------------- |
| Visual SLAM        | thermal camera建图 |
| EKF                | 状态估计             |
| feature extraction | thermal feature  |

### Optical Flow
| 方法                    | 作用      |
| --------------------- | ------- |
| frame-to-frame motion | 运动估计    |
| navigation            | UAV姿态估计 |

### Neural Networks
| 方法              | 作用                       |
| --------------- | ------------------------ |
| CNN             | thermal feature learning |
| deep perception | object recognition       |


### System Requirements for Navigation
| Navigation type     | Requirement |
| ------------------- | ----------- |
| SLAM                | 高分辨率 + 高帧率  |
| Map-less navigation | 低计算成本       |
| UAV navigation      | 轻量传感器       |



---

### Reference

1. https://pmc.ncbi.nlm.nih.gov/articles/PMC8540138/
2. https://www.researching.cn/ArticlePdf/m00009/2022/51/8/0851516.pdf
3. 
