# 介面模組

## 基於 ROS 之無人機地面站

```
Ground Control Station based on ROS#
```

![運動模組](/assets/images/interface.png)

整合了 ROS 的 Topic 訂閱與發送，透過影像視覺、狀態回報、快捷指令、飛行路徑繪製等功能達成監控無人機任務之地面站；並可依據情況進行任務終止，空中系統重設（Aeriel Reset）、空中讀取狀態繼續任務（State Recover）、切入手動遙控模式。

## 基於 AirSim 之系統整合環境模擬器

```
System Integration Simulator based on ROS and AirSim
```

![AirSim](/assets/images/airsim.png)

將實體無人機系統整合的應用，轉換成能夠在 AirSim 模擬環境裡進行飛前演算和測試，降低實際飛行測試時的成本，更便於進行演算法的實驗；系統整合環境功能包括：ROS、Behavior Tree、Learning-based visual computing and computer vision、Task Environment Setup。

## 強化學習之資料視覺化分析

```
Data Visualization Analysis on Reinforcement Learning to understand and explain AI Learning Behavior
```

![強化學習之資料視覺化分析](/assets/images/dpdv.png)

理解 AI 的學習行為，將 AI 所關注的重點與決策的依據透過視覺化的方式呈現使其更容易理解；圖為對最後一層 Hidden Layer 的 Feature map 做 T-sne 降維，根據選擇行為或分群結果以不同顏色視覺化，藉著對相同群的場景做疊加，觀察 AI 於場景歸納和決策。
