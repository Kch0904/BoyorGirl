<!-- 底下標籤來源參考寫法可至：https://github.com/Envoy-VC/awesome-badges#github-stats -->

![](https://img.shields.io/github/stars/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/forks/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues-pr/hsiangfeng/README-Example-Template.svg)｜![](https://img.shields.io/github/issues/hsiangfeng/README-Example-Template.svg)


# 專案介紹

![專案封面圖](https://img.freepik.com/premium-photo/flat-lay-composition-with-toy-stroller-words-boy-girl-light-blue-pink-background-background_98774-398.jpg)

> 本專案為國立中央大學111學年度開設課程，課號：IM5033 資料科學和機器學習課程的課堂競賽。

- [競賽連結](https://www.kaggle.com/competitions/boy-or-girl-2024-new/overview)

## 目標

### 介紹

目標是預測線上問卷中特定受訪者的性別。有關資料集的詳細資訊，請參閱“資料”標籤。
本次比賽為團體賽。每個小組可以由三個參與者組成，小組所作之實驗務求其他人能夠遵循和複製您的過程的方式為原則。

在這個競賽中，我們將詳細研究如何解決資料處理中的三個主要問題，分別是：缺失值、資料集不平衡、字元選擇和擷取。 我們將重點放在預處理技術、模型訓練技術和文字處理技術，以專注於正確的資料。在這份報告中，我們不僅將展示我們選擇的方法及其背後的原因，還將探討我們已經實施的改進以及這些改進如何幫助我們更準確地預測性別。

### 關鍵字
Random Forest; SMOTE; TF-IDF; Decision Tree; SVM; 四分位數

## 資料

> 下面的多個資料集是本課程第一屆Kaggle比賽中使用的資料集。

[boy or girls 2024 train_missingValue.csv]是本比賽的訓練集，[boy or girls 2024 test no ans_missingValue.csv]是測試集。 [Boy_or_girl_test_sandbox_sample_submission.csv] 是範例提交格式。

由於技術問題，訓練集和測試集都存在一些缺失值。

在本次比賽中，參賽者需要在訓練集上訓練一個模型，然後使用該模型來預測測試集中的性別列。 將預測結果提交到比賽頁面後，您看到的分數僅基於一半的訓練資料集，基於整個測試資料集的完整分數只有在比賽結束後才會揭曉。

### 資料內容

資料集中的欄位包含課程開始時問卷中的項目
* boy or girl 2024 train_missingValue.csv - the training set
* boy or girl 2024 test no ans_missingValue.csv - the test set
* Boy_or_girl_test_sandbox_sample_submission.csv - a sample submission file in the correct format

### 免責聲明

數據是在受訪者同意的情況下收集的，並且數據集不包含任何 PII 或個人識別資訊。
## 取得資料集

### Kaggle 模組
```bash
!pip install kaggle
```
### 下載資料集
```bash
### 建立資料夾
!mkdir ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
### 下載資料集
!kaggle competitions download -c boy-or-girl-2024-new
!unzip boy-or-girl-2024-new.zip
```
## 競賽評分方式

### 分類準確率

本次比賽使用分類準確性來評估結果。它衡量正確預測的百分比，公式如下。 

正確預測數/（正確預測數+錯誤預測數）

例如：

正確答案：[1,1,2,1,1]

預測：[1,2,2,1,1]

分類準確度為 4/5 = 0.8。

## 競賽提交格式

對於資料集中的每個樣本，提交文件應包含兩列：id 和性別。 

需確保 id 列的順序與測試集中的順序相同，並且性別列只允許 1 = 男孩，2 = 女孩。

該文件應包含標頭並具有以下格式：

``` ID,性別 1,1 2,2 3,2 4,1 5,1 ... ```

| ID | 性別 |
| --- | --- | 
| 1 | 1 |
| 2 | 2 |
| 3 | 2 |
| 4 | 1 |

## 資料夾說明

- views - 畫面放置處
- controllers - 控制器放置處
- modules - 模組放置處
- assets - 靜態資源放置處
  - scss - scss 檔案放置處
  - images - 圖片放置處
...

## 專案技術

- Python 3.10.12
- Tensorflow 2.15.0
- Numpy
- Pandas
- Scikit-Learn 1.4.2

## 第三方服務

- Google Colab

## 致謝

我們感謝所有受訪者花時間填寫問卷。
