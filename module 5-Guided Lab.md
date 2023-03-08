# 建立 RDS Database

# 實施步驟



# 實施架構

![image](https://user-images.githubusercontent.com/103306835/223628608-c0f66212-9f8e-482b-b73b-0596cb1dad87.png)

# 步驟1：創建 RDS database


1.搜尋RDS

![image](https://user-images.githubusercontent.com/103306835/223628676-5c8318b9-927b-4384-8a73-e91540557ca5.png)

2.點選[RDS]

![image](https://user-images.githubusercontent.com/103306835/223628709-b56196f7-ed21-4355-ab8d-1441972f5e8b.png)

3.點選[Create database]

![image](https://user-images.githubusercontent.com/103306835/223628891-6ec1dc28-a873-429e-8010-718bcf2b6401.png)

4.點選[MySQL]

![image](https://user-images.githubusercontent.com/103306835/223630578-93376058-ac48-4b87-be4e-a45d7b43f228.png)

5.Templates選擇[Dev/Test]

![image](https://user-images.githubusercontent.com/103306835/223630840-f927744e-f8de-4402-8c00-90bcf4a7bf5c.png)

6.Availability and durability選擇[Single DB instance]

![image](https://user-images.githubusercontent.com/103306835/223631051-593f4f56-aaf4-4053-9f10-aa3e20e4e5d6.png)

7.SettingsDB instance identifier: inventory-db

Username: admin

![image](https://user-images.githubusercontent.com/103306835/223631381-94e9bee0-ef3b-4ac7-87b3-f151581bf399.png)

8.Password: lab-password

Confirm password: lab-password

![image](https://user-images.githubusercontent.com/103306835/223631614-49878766-111f-4f3c-9ca2-f587df801ece.png)

9.DB instance class 選擇[Burstable classes (includes t classes)]、[db.t3.micro]

![image](https://user-images.githubusercontent.com/103306835/223632064-aeabc3c4-c2c6-47ec-a859-06030aee0cc0.png)

10.11.選擇[Lab VPC]

![image](https://user-images.githubusercontent.com/103306835/223632941-c8b653e9-c524-46b0-a04b-d08429e92b5c.png)

11.刪除[default security group]

![image](https://user-images.githubusercontent.com/103306835/223632392-e7df3852-3d74-461a-8fed-6b4b2c39a5a7.png)

12.選擇[DB-SG]

![image](https://user-images.githubusercontent.com/103306835/223633307-b5d3314a-7e3b-4ffa-84b9-27f38edb88af.png)

13.Initial database name: inventory

![image](https://user-images.githubusercontent.com/103306835/223633511-960df9b4-ba6e-4543-9706-6386ef155cdb.png)

14.取消點選[Enable Enhanced monitoring]

![image](https://user-images.githubusercontent.com/103306835/223633729-4d986db2-db2f-4692-b7bc-257c5b5952ef.png)

15.點選[Create database]

![image](https://user-images.githubusercontent.com/103306835/223633898-03a98d67-32ec-44e5-b5e0-ffe9df02c11f.png)

# 步驟2：Configuring web application communication with a database instance
