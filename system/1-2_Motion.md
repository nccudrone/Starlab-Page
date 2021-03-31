# 運動模組

## 區域掃描之路徑規劃

```
2D Coverage Path Planning Algorithm
```

![運動模組](/assets/images/2DPathPlanning.png)

給定一掃描之區域和相機參數，計算出該無人機飛經該區域鏡頭視角之覆蓋式掃描路徑，包含起飛點和一系列航點；完成掃描後會返回起飛點。

### 區域路徑規劃例子 - 棒球場

####  政大河堤棒球場 - 無人機飛行高度：7m
![棒球場](/assets/images/baseball.png)

#### 監控畫面
![監控畫面一](/assets/images/interface.png)

### 區域路徑規劃例子 - 操場

#### 政大操場掃描 - 無人機飛行高度：7m
![操場](/assets/images/stadium.png)

#### 監控畫面
![監控畫面二](/assets/images/interface2.png)


## 三維建築檢視 - 模型簡化

```

Building Inspection - 3D Model Simplification
```

![運動模組](/assets/images/Camera.png)

根據無人機與建物的距離和無人機視角（field of view）​所張出的相機視野範圍（Camera footprint）對欲掃描模型進行模型簡化，以降低後續路徑之計算複雜度，簡化目標為使建物模型的每個面都大於或等於相機視野範圍。

### 模型簡化 - 例子一
![例子一](/assets/images/Example1.png)
### 模型簡化 - 例子二
![例子二](/assets/images/Example2.png)
### 模型簡化 - 例子三
![例子三](/assets/images/Example3.png)

## 三維建築檢視 - 視點取樣

```
Building Inspection - Viewpoints Generation
```

![視點取樣](/assets/images/motion.png)

使用簡化後的模型，整合無人機的相機參數，透過檢視距離與相機視野等資料進行檢視點（Viewpoints）取樣。

## 三維建築檢視 - 路徑生成

```
Building Inspection - Coverage Path Planning
```

![3D 路徑規劃](/assets/images/3DPath.png)

透過預先計算單面檢視路徑規劃，再整合可涵蓋所有建物表面之路徑；無人機對建物距離為 2m，鏡頭視角 Field of View 為 80 度。


## ​機上協同式無人機路徑規劃演算法

![機上協同式無人機路徑規劃演算法](/assets/images/multi.png)

​目前無人機的動態路徑規劃都屬於由無人機上的傳感器(Sensor)蒐集資料，再傳輸回基地台(電腦)運算出全局的(Global)路徑規劃，並將路徑規劃指令傳給無人機做執行。
