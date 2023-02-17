# 快速建立你的靜態網站(S3)




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


