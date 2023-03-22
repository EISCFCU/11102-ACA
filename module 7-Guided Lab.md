# 建立VPC對等連接

# 實施步驟

![image](https://user-images.githubusercontent.com/103306835/226787513-63ab9269-5c29-4e82-be16-231d172689e9.png)

# 實施架構

![image](https://user-images.githubusercontent.com/103306835/226787546-b4cf37f4-b895-4c7a-aedd-adac8b89ef33.png)

# 步驟1：建立VPC對等連接

![image](https://user-images.githubusercontent.com/103306835/226787598-9f76ac0b-c1e7-4871-a1d0-1731bfbe5a59.png)

1.搜尋VPC

![image](https://user-images.githubusercontent.com/103306835/226787653-1f2784ce-45b7-4b6a-83e0-b6935493e7e9.png)

2.點選[VPC]

![image](https://user-images.githubusercontent.com/103306835/226787694-30544297-f214-4e9f-9e4f-ce2e75229520.png)

3.點選[ Peering Connection]

![image](https://user-images.githubusercontent.com/103306835/226787729-58e2d1f3-ef33-419e-92b1-835a3b12a71c.png)

4.點選[Create Peering Connection]

![image](https://user-images.githubusercontent.com/103306835/226787778-cbe5b187-273f-46cf-b47c-247b3f1c2f7e.png)

5. Peering connection name tag：Lab-Peer

VPC (Requester)： Lab VPC 

VPC (Accepter)：Shared VPC

![image](https://user-images.githubusercontent.com/103306835/226787867-45f9bf90-63ef-44bf-a4c1-964d4f9da8fb.png)

6.點選[Create Peering Connection]

![image](https://user-images.githubusercontent.com/103306835/226787912-63fd2d5e-c83a-4135-8e7b-59fb6f17df75.png)

7.點選[Lab-Peer]

![image](https://user-images.githubusercontent.com/103306835/226787955-3f1b09b7-9a37-4ea1-8750-c20d4641663c.png)

8.點選[Actions]->[Accept Request]

![image](https://user-images.githubusercontent.com/103306835/226787996-0ac00c27-7cc3-4117-994c-8064318c1c59.png)

9.點選[Accept request]

![image](https://user-images.githubusercontent.com/103306835/226788074-82db3303-6095-4af7-b2b4-a727ecae5c90.png)


# 步驟2：配置路由表

