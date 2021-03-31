# 認知模組

## 任務導向之決策模型

```
Mission-oriented Decision Making Model
```

![任務導向之決策模型](/assets/images/BT.png)

使用行為樹（Behavior Tree）為框架，透過節點執行和切換不同子任務，並依需求動態啟用或關閉模組，使無人機能自動完成任務。

## 空間資訊模型

```
Space Information Model
```

![空間資訊模型](/assets/images/SLAM.png)

使用無人機影像透過 SLAM 建立建築點雲模型，可搭配任務導向模型進行各種模型掃描或避障。

## 精準立面線條跟隨

```
Line Detection and Following Model
```

![精準立面線條跟隨](/assets/images/LineFollowing.png)

透過兩層方形 / 圓弧機率方格模型進行立面線條跟隨，並加入速度抑制等方式加強控制；經直線、折線、方形和曲線測試，具備高精準度及低線條偏出誤差。

## 區域巡邏及特點掃描

```
UAV Patrol and Statistical Collection on Pedestrians and Vehicles
```

![區域巡邏及特點掃描](/assets/images/Patrol.png)

搭配行為樹使其自動控制化減少人力上控制的需求，再藉由低成本微型無人機在指定區域自動巡邏，同時透過鏡頭使用深度學習模型來偵測物件，並透過電腦視覺和鏡頭參數計算出其定位，統計出其數量及物件在無人機視線範圍的移動軌跡。

## 河川巡檢系統與圖資對應

```
River Inspection System and Mapping on Satellite Map
```

![河川巡檢系統與圖資對應](/assets/images/River.png)

河川巡檢任務整合了河川視覺導航及物件定位等功能，能協助偵測出河川週遭的物件，並藉由空間定位技術和雲端衛星圖資的整合，在地圖上標記出物件位置，使巡檢人員無需親自巡邏，亦可透過地圖介面和影片截圖了解河川狀況。

## 階層式手勢控制架構

```
Hierarchical Gesture Control Architecture for UAV
```

![階層式手勢控制架構](/assets/images/Hand.png)

無論是自主或半自主控制，由於操作人員對任務理解比系統更全面，但因距離的關係操作人員往往對無人機周遭環境在認知有誤差，若進行修正控制將耗費時間影響任務執行效率，因此好的遠程操作仍十分重要。

本技術透過電腦視覺分析手和手指的各個節點，計算節點間的關係，藉以判斷每一隻手指當前的伸直與彎曲狀態，並且區分所屬的左右手，構建出階層式的手勢控制架構，讓使用者能透過不同層級的手勢下達不同層級的指令，藉此控制無人機執行較複雜的任務；同時，也加入視覺里程計(Visual Odometry)，獲取更多的空間資訊，以增強控制系統的情境意識。
