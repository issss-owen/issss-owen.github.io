# 基於深度學習之茶葉生長環境預測
## 本專題基於物聯網（IOT）和模型運算技術用於智慧監測茶園的資料預測，使用土壤溼度感測器、土壤溫度測量裝置、環境溫度感測器、土壤酸鹼度計、EC 值檢測計，遠端監控土壤溫溼度、pH 值、EC 值，最後根據收集到的數據進行分析，給出最適當的農耕決策。
## 材料與方法
### 數據搜集
環境計測土壤溫度、土壤濕度、pH 值、EC 值等資料，計測時間從2020年11月06號到2021年03年15號，每小時計測一筆，傳到環境監控系統，以供紀錄，資料共計2987筆。
### ![螢幕擷取畫面 2024-09-05 194727](https://github.com/user-attachments/assets/02b14a6d-7d21-46e1-a7c0-4c62da6de008)
### 模型建置
使用語法 Python 作為模型建置環境，透過 Keras 建置 LSTM、BiLSTM 模型，並進行修正。
## LSTM
### ![螢幕擷取畫面 2024-09-05 195233](https://github.com/user-attachments/assets/b6000951-2a51-4a84-a1e6-34ed7aead4e6)
## Bi-LSTM
### ![螢幕擷取畫面 2024-09-05 195425](https://github.com/user-attachments/assets/9d0e27f0-87c2-4137-a7f1-b6f06363dfad)
## GRU
### ![螢幕擷取畫面 2024-09-05 195532](https://github.com/user-attachments/assets/55a344b2-d4ef-435a-8af6-888cd5869d9f)
## Stacking model
### ![螢幕擷取畫面 2024-09-05 195642](https://github.com/user-attachments/assets/8adc0d85-021e-421d-94f9-7debbd9e8af7)
## 結果與討論
本研究使用了多種深度學習模型來預測影響茶葉生長的環境條件，具體包括LSTM、Bi-LSTM、GRU 和多尺度特徵融合模型（Stacking Model）。結果顯示這些模型在預測準確性方面存在差異，具體表現在 RMSE（均方根誤差）的比較上。
### 模型性能比較：
#### 預測準確性：從 RMSE 值來看，Multi-scale feature fusion model 多尺度特徵融合模型在所有模型中整體表現最佳，其次是 GRU，最後是 LSTM 和Bi-LSTM。這顯示堆疊模型在預測茶葉生長的環境條件方面最為精確，GRU也具有不錯的表現。模型選擇：選擇合適的模型對於提高預測精度非常重要。研究結果顯示，雖然 LSTM 和 Bi-LSTM 能夠有效處理時間序列數據，但在本研究中，GRU相較於多尺度特徵融合模型的性能更優。
![螢幕擷取畫面 2024-09-05 195859](https://github.com/user-attachments/assets/984c7bc3-2ad6-48a6-b3b8-9c28d5a44d41)
![螢幕擷取畫面 2024-09-05 200007](https://github.com/user-attachments/assets/0f441953-8f8e-49d8-8083-79611bb292a7)

