# 感知模組

## 基於三維定位之避障

```
Avoidance based on 3D Localization
```

![基於三維定位之避障](/assets/images/GroundPlan.png)

透過 YOLO V3 的物件辨識，利用相機參數和視覺資訊反推無人機所在位置，計算出與障礙物的距離、方向、位置，再使用 RRT-Star 演算法進行動態的路徑規劃，對無人機下達指令進行迴避動作。​

## ​補強低光源影像以增強物件辨識

```
Enhancing Object Detection in Degraded Images
```

![補強低光源影像以增強物件辨識](/assets/images/perception.jpg)

本技術利用卷積神經網路強大的學習能力，還原低亮度且非均勻光源下的影像，並以該神經網路作為前處理，強化現有物件辨識方法的準確度。本技術在真實的 VisDrone (無人機空拍資料集)上進行充分的評估，驗證該技術能增強物件辨識約 5 的召回率，同時本技術亦可被應用於過曝影像的還原。

可廣泛應用於無人載具、監控或需要即時影像追蹤的應用情境，透過將無人載具即時取得的影像進行處理，能提高無人載具在即時運算時的物件辨識率。


## 基於 RGB-D 影像的深度學習技巧在之避障

```
Collision Avoidance Based on RGB-D Images Using Deep Learning Techniques
```

本技術以 RGB-D 影像與深度學習為基礎，分別為沒有搭載深度攝影機的無人機和有搭載深度攝影機的無人機，提出自動避障的方法。

![RGBD迴避障礙](/assets/images/RGBD01.png)

對於沒有搭載深度攝影機的無人機，透過開放的碰撞資料集使用深度估計模型預測出對應的深度資訊，再透過深度資訊在 RGB 影像中分割出危險和安全等區域，並使用即時語義分割模型進行訓練，將從彩色影像中預測出來的區域分布，使無人機找到一個合適的避障方向。

![RGBD迴避障礙2](/assets/images/RGBD2.jpg)

對於搭載深度攝影機的無人機，本研究使用即時語義分割模型和分群演算法，得到物體的類別和位置資訊，接著使用路徑規劃演算法幫助無人機找出最佳的避障路徑。本研究所訓練的深度學習模型可以在嵌入式裝置上進行推論，因此我們提出的避障方法將可應用於運算資源有限的無人機。

## ​河川多頻譜分係

```
Digital Multi-Spectral Video Analysis for River
```

![河川多頻譜](/assets/images/multispectrum.png)

透過無人機的鏡頭及熱影像儀，取得 RGB 影像與熱影像，讓無人機在自動沿著河道飛行時，可透過異常偵測判斷河川水質是否有異常。上圖為已蒐集的 RGB 影像及熱成像，其中有標註河川範圍，並使用現有神經網路對河川資料集進行分割

![河川多頻譜2](/assets/images/segmentation.png)

### 相關研究實驗參數

![資料集 - RGB 影像及熱影像](/assets/images/dataset.png)

- Train/Val/Test: 200/50/50 images
- Image Resize/Crop/Pad to 320*320
- Feature Pyramid Network (FPN)
- Encoder = se_resnext101_32x4d
- Encoder_Weights = imagenet
- Train 40 epoches
