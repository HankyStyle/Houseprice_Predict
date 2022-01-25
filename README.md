# Houseprice_Predict
房價預測系統

ALOT Final Project
---
此專案是藉由 政府提供的 實價登錄 資料 來訓練一個Auto-Sklearn Model 藉此預測出 某縣市某一地區 大樓或套房的價格
將Train好的Model 用 FastApi & HTML 建立 Web Application

![image](https://github.com/HankyStyle/Houseprice_Predict/blob/master/demo.gif)


## Quick Start

1. fork the repositories

   ```shell
   git clone https://github.com/HankyStyle/Houseprice_Predict.git
   ```


2. Follow Colab in training to training Model


3. Start development
   


## Development

- Setup virtual environment

```shell
python -m venv your-awesome-venv-name
source your-awesome-venv-name/bin/activate
pip install -r requirements.txt
```

- Start Dev Server

```shell
uvicorn app:app --reload
```

### File Description
```
.
├── requirements.txt 
├── app.py  // 專案中的主要組件，所有頁面都在app.py下執行
├── static\js
│   └── test.js
├── templates
│   ├── Home.html  // 網頁首頁
│   ├── Kaohsiung.html  // 高雄
│   ├── NewTaipei.html // 新北
│   ├── Taichung.html  // 台中
│   ├── Tainan.html  // 台南
│   ├── Taoyuan.html  // 桃園
│   └── Taipei.html // 台北
└── training  
    ├── Aiot_model.ipynb  // 訓練模型Colab
    ├── all_data.csv  // 訓練資料
    └── train.py // 練習範本Colab
```

## Training

### DataSet
![image](https://user-images.githubusercontent.com/70362842/150983418-62a262be-cfc5-4d64-9450-6c37c65422cc.png)

1. 從政府的實價登錄資料 整理 挑選有興趣的特徵
  + 建材 e.g., 鋼筋、鋼骨
  + 地區 e.g., 南區、西屯區
  + 坪數
  + 主要用途 e.g., 住宅、辦公室

2.  把類別型資料 轉換為數值參數

3.  


## Credit

- [HankyStyle](https://github.com/HankyStyle)
- [ioveeagle](https://github.com/ioveeagle)
- [Rayching](https://github.com/Rayching)
- [huang624](https://github.com/huang624)
- [ms0004284](https://github.com/fcu-d0589769)
