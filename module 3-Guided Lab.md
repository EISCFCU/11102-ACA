# 快速建立你的靜態網站(S3)

![image](https://user-images.githubusercontent.com/103306835/219964924-90022019-92b4-424d-9b8f-979e00349239.png)


# 實施步驟

![image](https://user-images.githubusercontent.com/103306835/172282245-df7b6c48-5437-4886-9b6b-86295e4ff3b9.png)

# 步驟1：新增S3 Bucket


1.搜尋[S3]

![image](https://user-images.githubusercontent.com/103306835/219597448-de8778d6-48dc-4c75-9e7c-3d722deead05.png)

2.點選[S3]

![image](https://user-images.githubusercontent.com/103306835/219598105-8b57b0a2-0bdd-44c2-b1aa-387ea0b7fe85.png)

3.點選[Create bucket]

![image](https://user-images.githubusercontent.com/103306835/219598701-db3fc5a0-7abb-42e6-b4e9-f6bc9168c02a.png)

4.輸入Bucket Name

Bucket name：website-<123>

<123>請用其他數字替換
* S3 Bucket name需為唯一值

![image](https://user-images.githubusercontent.com/103306835/219601816-20449000-ead3-4ff7-a464-d5c5d4758daa.png)

5.點選ACLs enabled；Object Ownership選擇Bucket owner preferred

![image](https://user-images.githubusercontent.com/103306835/219603364-23a5017e-d7d0-4995-8493-5faa5f7bdc07.png)

6.取消勾選Block all public access

![image](https://user-images.githubusercontent.com/103306835/219604756-e72fb900-ad4a-4a98-859a-2bde4fd215c6.png)

7.勾選[I acknowledge..]

![image](https://user-images.githubusercontent.com/103306835/219605690-3a3e01d7-f783-48d8-a2e0-7f3380d6724d.png)

8.點選[Create bucket]

![image](https://user-images.githubusercontent.com/103306835/219606315-3baee2e6-ac0c-4483-a678-37bc6be69017.png)

9.點選剛才建立的S3 Bucket

![image](https://user-images.githubusercontent.com/103306835/219607357-6d6cf184-d2c4-49ce-8573-a01adf758c6f.png)

10.點選[Properties]

![image](https://user-images.githubusercontent.com/103306835/219608152-8d556b34-2743-4aed-839e-34c833513fd3.png)

11.點選[Tags] 的[Edit]

![image](https://user-images.githubusercontent.com/103306835/219609177-db9e9b55-ae20-4d93-b4c1-2210056b46c5.png)

12.點選[Add Tag] 

![image](https://user-images.githubusercontent.com/103306835/219609718-f6d66bee-5332-4abb-85c6-991a56867783.png)

13.輸入Key：Department; Value: Marketing

![image](https://user-images.githubusercontent.com/103306835/219612580-58256316-ba3f-4e76-9f16-ff272a756d59.png)

14.點選[Save changes] 

![image](https://user-images.githubusercontent.com/103306835/219612652-ed74ad7f-a222-4f2f-aa4c-d5c09f798580.png)

15.點選[Static website hosting] 的[Edit]

![image](https://user-images.githubusercontent.com/103306835/219613181-5c76193d-bb74-40a0-8e9e-5e640f36b876.png)

16.勾選[Enable]、[Host a static website]

![image](https://user-images.githubusercontent.com/103306835/219615765-51f2228f-0c60-4efd-8200-8c2b350793a2.png)

17.輸入index document：Index.html

Error document: error.html

![image](https://user-images.githubusercontent.com/103306835/219616923-8517971f-37c5-472d-a4de-ae6800daa333.png)

18.點選[Save changes]

![image](https://user-images.githubusercontent.com/103306835/219617243-2c915005-8e4f-48b9-af88-c368a2cbebd2.png)

19.成功變更

![image](https://user-images.githubusercontent.com/103306835/219617765-bab38b56-7f99-4a03-b913-493e51d0add9.png)

20.點選[Static website hosting] 的連結

![image](https://user-images.githubusercontent.com/103306835/219962843-81bf6eec-a404-4936-865e-908fe721831d.png)

21.會出現403 Forbidden

![image](https://user-images.githubusercontent.com/103306835/219962877-bdf0ef83-42c1-49e1-a2ac-6c966aee9478.png)

# 步驟2：上傳網頁資料


1.下載網頁資料

![image](https://user-images.githubusercontent.com/103306835/219963080-7ce9ea0d-3fa8-489e-b720-776955516ce5.png)

2.點選新增的Bucket

![image](https://user-images.githubusercontent.com/103306835/219963247-69c28ce6-bc1a-41f7-9d03-775a394dddce.png)

3.點選[Upload]

![image](https://user-images.githubusercontent.com/103306835/219963328-666b31c2-80ac-478c-ad07-fe1ee6000fa5.png)

4.將網站資料拖曳到下方畫面

![image](https://user-images.githubusercontent.com/103306835/219963492-83abf469-106b-4cb6-82e4-dcc296f989b4.png)

5.點選[Upload]

![image](https://user-images.githubusercontent.com/103306835/219963775-1e0ae9eb-36fe-4ee9-a18c-234328dee489.png)

6.成功上傳

![image](https://user-images.githubusercontent.com/103306835/219963815-442ccffe-75f6-4152-88d6-ff8bb354ac63.png)

7.點選[Close]

![image](https://user-images.githubusercontent.com/103306835/219963854-75a77db9-b670-4651-936d-20444ebe3687.png)

# 步驟3：設定對外瀏覽權限


1.返回網頁頁面按刷新仍會出現403 Forbidden

![image](https://user-images.githubusercontent.com/103306835/219964397-aa7aea25-b7d6-49bd-87bc-a9988b584ccc.png)

2.勾選所有物件

![image](https://user-images.githubusercontent.com/103306835/219964535-b3cd3776-4806-480a-b260-9f78790214fc.png)

3.點選[Actions]

![image](https://user-images.githubusercontent.com/103306835/219964620-4c632ca0-12e2-45b8-ad2c-e0178c71117f.png)

4.點選[Make public using ACL]

![image](https://user-images.githubusercontent.com/103306835/219964683-5cc40723-becb-4485-ac34-77750a2bcec6.png)

5.點選[Make public]

![image](https://user-images.githubusercontent.com/103306835/219964746-17d7687e-5dbf-4992-a89a-787b80dbe7b8.png)

6.變更成功

![image](https://user-images.githubusercontent.com/103306835/219964786-7687a79b-8f99-4d26-8925-2db2a0fa413b.png)

7.回到網頁頁面刷新

![image](https://user-images.githubusercontent.com/103306835/219964874-2b2f97a0-9133-4d4b-bd07-73e175e1681c.png)

8.重新瀏覽網頁

![image](https://user-images.githubusercontent.com/103306835/219965097-a9e49ac0-1c1a-4e5d-a666-f7362d6e28dc.png)

# 步驟4：更新網站


1.將index檔以文字檔開啟

![image](https://user-images.githubusercontent.com/103306835/219965306-8ce60279-c1c2-4012-b4ca-2e77a5a4afa4.png)

2.找到[Served from Amazon S3]

![image](https://user-images.githubusercontent.com/103306835/219965421-3962e477-7118-4e06-a387-86190470c93f.png)

3.替換為 Created by [YOUR-NAME]

![image](https://user-images.githubusercontent.com/103306835/219965574-a19913aa-8225-4f40-9cca-70ce80427c7a.png)

4.儲存檔案
  
![image](https://user-images.githubusercontent.com/103306835/219965659-1da891eb-56f4-478d-8b7b-2dbc90da3f7f.png)
  
5.點選[Upload]

![image](https://user-images.githubusercontent.com/103306835/219965827-959334a2-66e4-4d5c-be28-d583e81e43d3.png)

6.將剛才編輯的index檔拖曳到下方畫面
  
![image](https://user-images.githubusercontent.com/103306835/219965928-a6a4883f-969e-4fff-9b4c-79611b60cd30.png)

7.點選[Upload]
  
![image](https://user-images.githubusercontent.com/103306835/219966067-7ee38def-5f77-483c-b50b-e2ea9ee8ff89.png)

8.點選[index]
  
![image](https://user-images.githubusercontent.com/103306835/219966126-5a4d34bb-6e92-48a0-a00b-062168e58a2f.png)
  
9.點選[Actions]→[Make public using ACL]
  
![image](https://user-images.githubusercontent.com/103306835/219966201-6e3e887e-2482-4f32-95f1-2446479acad0.png)

10.點選[Make public]
  
![image](https://user-images.githubusercontent.com/103306835/219966326-f4b6e874-5770-413d-b71b-a8f45e979820.png)

11.回到網頁刷新
  
![image](https://user-images.githubusercontent.com/103306835/219966364-edabba0b-17c9-45f3-8057-bb08b67c8ec4.png)

# 步驟5：Submitting your work


1.點選[Submit]

![image](https://user-images.githubusercontent.com/103306835/219966543-28056617-9f6d-4a8e-b1f2-ec40c45cb598.png)

2.點選[Yes]

![image](https://user-images.githubusercontent.com/103306835/219966653-e7cbbff2-4f61-4ae1-ba96-6cfb30627aa2.png)

3.點選[Grades]

![image](https://user-images.githubusercontent.com/103306835/219966719-572ea09b-bec8-46a0-8a8f-df4ec9098b4b.png)

4.查看分數

![image](https://user-images.githubusercontent.com/103306835/219966788-c3562bdc-71e1-4b97-bcab-234031ff2cdf.png)
