# 雲端簡易辨識應用

# 使用資源

lambda.zip： https://github.com/EISCFCU/s3-reko-dynamodb/blob/main/DetectLabel-96c34899-e979-4c92-b71c-be97f0a9983d.zip


# 使用平台：AWS Academy Learner Lab-Foundation Services

課程代號：18579(只要是Learner Lab皆可學習本實作內容)

# 實施架構

![image](https://user-images.githubusercontent.com/103306835/167802083-16e42066-486a-40b6-8fbd-87115e7cb47e.png)


# 操作步驟

![image](https://user-images.githubusercontent.com/103306835/167802159-13a718ca-94a6-43ae-88c8-8f8caeef84b4.png)

# 步驟1：建立儲存桶(S3) 

1.搜尋S3

![image](https://user-images.githubusercontent.com/103306835/167802291-27f11a38-0ca5-4b04-9e30-1038a0ebe83a.png)

2.點選[建立儲存貯體]

![image](https://user-images.githubusercontent.com/103306835/167802346-08189325-386e-495d-b9b0-7a70c3f966ab.png)

3.輸入儲存貯體名稱(自訂)

![image](https://user-images.githubusercontent.com/103306835/167802395-9c2fecaa-0b2f-44e7-8454-5dcb86dd7add.png)


4.取消勾選封鎖 並勾選我確認…

![image](https://user-images.githubusercontent.com/103306835/167802651-cba4b7b4-1298-4860-9159-b0f0a078d272.png)

5.點選[建立儲存貯體]

![image](https://user-images.githubusercontent.com/103306835/167802695-e1dc5448-479b-45f5-8fa7-26ca279020ca.png)

6.成功建立儲存貯體

![image](https://user-images.githubusercontent.com/103306835/167802737-3fb3a9e6-41d2-4321-9133-4e87d311a1c6.png)

# Step2：建立No sql 資料庫(Dynamodb)

1.搜尋Dynamodb

![image](https://user-images.githubusercontent.com/103306835/167803171-751386ba-392c-473c-ba55-ef7a9c1fea46.png)

2.點選[建立資料表]

![image](https://user-images.githubusercontent.com/103306835/167803217-ee8f3d50-fd11-4e89-a865-a47bf5a88ab4.png)

3.輸入資料表名稱：Images 

分區索引：Image(字串) 

排序索引：Labels(字串)

![image](https://user-images.githubusercontent.com/103306835/167803595-8e6dea0e-2d6c-4d4f-b4b6-7ee4ae62a7d4.png)

4.點選[建立資料表]

![image](https://user-images.githubusercontent.com/103306835/167803640-3f687cf5-919f-42f0-98b4-04742f51d826.png)

5.成功建立Images資料表(狀態：作用中)

![image](https://user-images.githubusercontent.com/103306835/167804044-5412a1d0-f4c4-4c65-8d3d-ae310c37be6a.png)

# Step3：建立 Lambda

1.搜尋Lambda 並點選

![image](https://user-images.githubusercontent.com/103306835/167804391-b92645fd-ba51-4af7-b7be-0fbf0ce18175.png)

2.點選[建立函式]

![image](https://user-images.githubusercontent.com/103306835/167804456-a4382f14-a3c5-44d8-a8dd-8a00bd4e8515.png)

3.點選從頭開始撰寫

![image](https://user-images.githubusercontent.com/103306835/167804503-2d93b1b0-a2f4-428c-b4ec-78eb5135b001.png)

4.函數名稱自訂

![image](https://user-images.githubusercontent.com/103306835/167804556-69ed1199-612b-45b8-a22d-dc67b993fb6e.png)

5.執行時間：Python3.8

![image](https://user-images.githubusercontent.com/103306835/167804599-3a7ab825-8105-4201-92c3-5d0a55e2a3a4.png)

6.選擇使用現有的角色：LabRole

![image](https://user-images.githubusercontent.com/103306835/167804655-dfe9ac3c-e496-4db8-aed3-ebc2c9f5e77b.png)

7.點選[建立函式]

![image](https://user-images.githubusercontent.com/103306835/167804696-3ca76b2c-3161-4d08-8788-53d1bde160b9.png)

8.成功建立函式

![image](https://user-images.githubusercontent.com/103306835/167804740-b5265392-533b-4c77-bedd-020f849b77d5.png)

9.點選[新增觸發]

![image](https://user-images.githubusercontent.com/103306835/167804777-f3528c9e-a62e-4595-923d-ec615d5117bb.png)

10.選擇S3

![image](https://user-images.githubusercontent.com/103306835/167804816-bf1add2d-9986-4eda-b899-42d60c5e683c.png)

11.選擇步驟1建立的S3

![image](https://user-images.githubusercontent.com/103306835/167804862-4f83b741-2ea2-4f01-bb7f-d335090bf17f.png)

12.勾選我確認

![image](https://user-images.githubusercontent.com/103306835/167804929-3f72f9a7-2a1e-4de4-a4c2-3e1553f039fd.png)

13.點選[新增]

![image](https://user-images.githubusercontent.com/103306835/167804973-f620ba9f-ce95-4aa4-8c9d-ba853ede4fbe.png)

14.完成觸發設定

![image](https://user-images.githubusercontent.com/103306835/167805028-618e6994-f99e-4f69-93e0-680457400a99.png)

15.往下滑動視窗

![image](https://user-images.githubusercontent.com/103306835/167805087-5977a15d-40e2-4b08-b39c-d23e1491355c.png)

16.找到上傳按鈕 並點選

檔案連結：https://github.com/EISCFCU/s3-reko-dynamodb/blob/main/DetectLabel-96c34899-e979-4c92-b71c-be97f0a9983d.zip

![image](https://user-images.githubusercontent.com/103306835/167805143-d43fdc58-32d4-446b-8c92-6cea7ec1e2b7.png)

17.選擇.zip 檔案

![image](https://user-images.githubusercontent.com/103306835/167805204-42595a7b-cf67-4c54-9293-1b1a526e6d3d.png)

18.選擇[上傳]

![image](https://user-images.githubusercontent.com/103306835/167805244-29e64ba3-eb67-4476-9e50-bf80b0234e70.png)

19.選擇[儲存]

![image](https://user-images.githubusercontent.com/103306835/168414908-129f2b75-1037-46ec-9899-114562f3a7d5.png)

20.更改第8行資料(S3名稱)

![image](https://user-images.githubusercontent.com/103306835/167805344-b4e644ff-e3d0-4202-b107-eae12470f691.png)




# 參考資料：https://docs.aws.amazon.com/zh_tw/rekognition/latest/APIReference/API_DetectLabels.html

# 教材編制：逢甲大學企業資訊系統研究中心
# 更新日期：2023/02/16(Peggy)
