# Houseprice_Predict 房價預測模型
Using the Actual Selling Price of Real Estate Data to predict the price of Estate

ALOT Final Project
---
此專案是藉由 政府提供的 實價登錄 資料 來訓練一個Auto-Sklearn Model 藉此預測出 某縣市某一地區 大樓或套房的價格
將Train好的Model 用 FastApi & HTML 建立 Web Application

![image](https://github.com/HankyStyle/Houseprice_Predict/blob/master/demo.gif)


### 架構圖
![image](https://user-images.githubusercontent.com/70362842/151114798-f10a1a11-760f-43c5-95b3-46b232489a25.png)

更多FastAPi 介紹 可以參考:https://minglunwu.github.io/notes/2021/fast_api_note_1.html


## Quick Start

1. fork the repositories

   ```shell
   git clone https://github.com/HankyStyle/Houseprice_Predict.git
   ```


2. Follow Colab in training to training Model


3. Start development
   +  FastAPi 與 Flask 不同的是，如果直接執行此 main.py 不會啟動服務。需要透過 ASGI Server gvicorn 來啟用
      

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

### DataSet 下載連結: https://plvr.land.moi.gov.tw/DownloadOpenData
下圖為台北市資料範例
![image](https://user-images.githubusercontent.com/70362842/150983418-62a262be-cfc5-4d64-9450-6c37c65422cc.png)

1. 從政府的實價登錄資料 整理 挑選有興趣的特徵
  + 建材 e.g., 鋼筋、鋼骨
  + 地區 e.g., 南區、西屯區
  + 坪數
  + 主要用途 e.g., 住宅、辦公室

2. 把類別型資料 轉換為數值參數

 ![image](https://user-images.githubusercontent.com/70362842/150988438-453fe780-71a7-4aeb-9e67-2e006c7059ec.png)

3.  將所有參數與成交價做成資料集，並使用Autosklearn尋找最好的模型和參數 或是挑選幾個較好的模型堆疊，獲得一個效果不錯的模型。

### Result
![image](https://user-images.githubusercontent.com/70362842/150989149-1fce2cda-c7a1-4f10-994c-41eb89e22210.png)


## Credit

- [HankyStyle](https://github.com/HankyStyle)
- [ioveeagle](https://github.com/ioveeagle)
- [Rayching](https://github.com/Rayching)
- [huang624](https://github.com/huang624)
- [ms0004284](https://github.com/fcu-d0589769)
