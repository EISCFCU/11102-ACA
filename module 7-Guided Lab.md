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

![image](https://user-images.githubusercontent.com/103306835/226788298-212f9dca-439c-4278-aeda-33e410f2ef73.png)

1.點選[Route Tables]

![image](https://user-images.githubusercontent.com/103306835/226788345-555e160b-7d8b-4621-aa01-e14903f61ddd.png)

2.點選[Lab Public Route Table]

![image](https://user-images.githubusercontent.com/103306835/226788382-b48db351-4b1e-4e07-95aa-ec678a29bb14.png)

3.點選[Routes]

![image](https://user-images.githubusercontent.com/103306835/226788423-a800a86e-767f-4aa1-8af0-669dc28a963e.png)

4.點選[Edit routes]

![image](https://user-images.githubusercontent.com/103306835/226788456-40ca780d-a6a7-4fae-9aa6-60012d4af39b.png)

5.點選[Add route]

![image](https://user-images.githubusercontent.com/103306835/226788498-f05568e1-4186-4ef4-9492-09ceda8a8994.png)

6. Destination： 10.5.0.0/16

Target：Peering Connection->Lab-Peer

![image](https://user-images.githubusercontent.com/103306835/226788599-0e22f738-9b3c-4301-94a7-92c78aa5dcb2.png)

7.點選[Save routes

![image](https://user-images.githubusercontent.com/103306835/226788633-ba68a327-87d2-4dee-b67c-41d9c2b24292.png)

8.點選[Shared-VPC Route Table]

![image](https://user-images.githubusercontent.com/103306835/226788677-29ebe395-54f5-44e6-a253-b8e1d5843647.png)

9.點選[Routes]

![image](https://user-images.githubusercontent.com/103306835/226788707-10f36607-b19e-4a1f-8b93-e80ef5db77b2.png)

10.點選[Edit routes]

![image](https://user-images.githubusercontent.com/103306835/226788757-7d4eba45-f45f-43a9-92ff-4d504901e717.png)

11.點選[Add route]

![image](https://user-images.githubusercontent.com/103306835/226788824-095d6728-ff43-4488-b89e-999d39667740.png)

12. Destination： 10.0.0.0/16

Target：Peering Connection->Lab-Peer

![image](https://user-images.githubusercontent.com/103306835/226788885-eb928e01-fc86-4efd-baa3-e9c73a91d5cd.png)

13.點選[Save routes]

![image](https://user-images.githubusercontent.com/103306835/226788920-ce6677fa-5727-4381-addf-61e8feee69a9.png)


# 步驟3：測試VPC對等連接


1.搜尋EC2

![image](https://user-images.githubusercontent.com/103306835/226789991-df281de4-6913-47b0-9848-5c8246627c47.png)

2.點選[EC2]

![image](https://user-images.githubusercontent.com/103306835/226790012-ff5abc71-bb12-4f8d-b285-998e7fe223ca.png)

3.點選[Instances]

![image](https://user-images.githubusercontent.com/103306835/226789300-94f8acad-f2af-452d-a5e9-e72b8869fba2.png)

4.複製[IPv4 Public IP]

![image](https://user-images.githubusercontent.com/103306835/226789356-d01aa0de-dfff-4070-956e-3489136633e1.png)

5.打開 IPv4 Public IP

![image](https://user-images.githubusercontent.com/103306835/226789382-6246c3fb-8ff3-4f12-80f2-b47b35305587.png)

6.點選[Settings]

![image](https://user-images.githubusercontent.com/103306835/226789410-5593cf19-3ad6-4c49-9711-e319a9b1a79a.png)

7.複製[Endpoint]

![image](https://user-images.githubusercontent.com/103306835/226789434-55260b93-0e56-4ccd-9b80-adf51e89efc7.png)

8. Database: inventory 

Username: admin 

Password: lab-password

![image](https://user-images.githubusercontent.com/103306835/226789602-f648471f-2902-46da-a139-6bbd5c114343.png)

9.點選[Save]

![image](https://user-images.githubusercontent.com/103306835/226789641-66166405-d1db-44f1-85b4-2eb86b418928.png)

![image](https://user-images.githubusercontent.com/103306835/226789668-a185e576-2758-4a36-855d-338b5e199304.png)

10.點選[Submit]

![image](https://user-images.githubusercontent.com/103306835/226789731-40adf31c-a766-4e1d-ada6-bd47d72889ef.png)

11.查看成績

![image](https://user-images.githubusercontent.com/103306835/226789763-c241a1d1-c393-4b9e-af42-6d9a4dabb26e.png)

12. End Lab

![image](https://user-images.githubusercontent.com/103306835/226789816-3f2b4d7f-8fb2-412e-b640-e60cd3fa4706.png)
