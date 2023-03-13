# 建立VPC

# 實施步驟

# 實施架構

# 步驟1：建立VPC


1.搜尋VPC

![image](https://user-images.githubusercontent.com/103306835/224621509-ceae53a8-6737-4264-9fa6-18d75e8cbeba.png)

2.點選[VPC]

![image](https://user-images.githubusercontent.com/103306835/224621530-febf10c2-f735-4021-882c-7610cb0d0bbf.png)

3.點選[Your VPCs]

![image](https://user-images.githubusercontent.com/103306835/224621730-9f723c91-6c61-4a69-b30c-c6dd61bcabfa.png)

4.點選[Create VPC]

![image](https://user-images.githubusercontent.com/103306835/224621859-37ca99c3-2af3-4009-9a8f-a63b462bc667.png)

5.Name tag: Lab VPC

IPv4 CIDR block: 10.0.0.0/16

![image](https://user-images.githubusercontent.com/103306835/224622436-fa4bfee7-906c-4f85-bf1e-171a9f47b4db.png)

6.點選[Create VPC]

![image](https://user-images.githubusercontent.com/103306835/224622546-05b1e633-ba33-4d9f-8775-f0a630da5657.png)

7.點選[Tags]

![image](https://user-images.githubusercontent.com/103306835/224622733-27f2bb1c-770f-48ef-89ff-c0def7047a71.png)

8.點選[Actions]->[Edit VPC settings]

![image](https://user-images.githubusercontent.com/103306835/224623284-0888dc8e-0e9d-41e6-8f2b-735e6e9c6a54.png)

9. 點選[Enable DNS hostname]

![image](https://user-images.githubusercontent.com/103306835/224623529-92621229-9349-4fb7-8cb5-073b75450e1c.png)

10. 點選[Save]

![image](https://user-images.githubusercontent.com/103306835/224623686-60919442-fe78-4d62-bbc2-01f629f0440b.png)


# 步驟2：建立子網
# 建立公有子網
1.點選[Subnets]

![image](https://user-images.githubusercontent.com/103306835/224623927-3ec0734e-9ff6-499c-962c-1ba270bdd0a5.png)

2.點選[Create subnet]

![image](https://user-images.githubusercontent.com/103306835/224624076-8a623be8-45a7-4446-ba8c-c8c2bec4bf8e.png)

3.VPC ID: Lab VPC

Subnet name: Public Subnet

![image](https://user-images.githubusercontent.com/103306835/224624613-b9112afe-7bc1-465d-9db4-826baa9418eb.png)

4.Availability Zone: 點選第一個 AZ

![image](https://user-images.githubusercontent.com/103306835/224624922-afa7c772-0076-49f6-a94e-0acd974d2821.png)

5.IPv4 CIDR block: 10.0.0.0/24

![image](https://user-images.githubusercontent.com/103306835/224625345-fdbac872-d3f7-4e68-a3c4-69ad8a9a873f.png)

6.點選[Create subnet]

![image](https://user-images.githubusercontent.com/103306835/224625510-4229be12-4121-46d1-b6a6-eaf08f2db3fa.png)

7.點選[Public Subnet]

![image](https://user-images.githubusercontent.com/103306835/224625671-6d77f3d2-6831-426f-bbe9-341373d71e8c.png)

8.點選[Actions]->[Edit subnet settings]

![image](https://user-images.githubusercontent.com/103306835/224625847-39f5a671-f9e5-48f2-9a4c-75c5bab4cf66.png)

9.點選[Enable auto-assign public IPv4 address]

![image](https://user-images.githubusercontent.com/103306835/224626020-3a2bbe1c-3340-4098-85e5-884b71c5ec24.png)

10.點選[Save]

![image](https://user-images.githubusercontent.com/103306835/224626142-f5cb6238-a957-4c22-b407-c947c82a3113.png)

# 建立私有子網
9.點選[Create subnet]

![image](https://user-images.githubusercontent.com/103306835/224626476-260e3e57-4182-4572-8b58-4686f7c3fd70.png)

10.VPC ID: Lab VPC

Subnet name: Private Subnet

![image](https://user-images.githubusercontent.com/103306835/224626933-212a7c67-0fe6-42c1-86ea-a45f18eee786.png)

11.Availability Zone: 點選第一個 AZ

![image](https://user-images.githubusercontent.com/103306835/224627211-95d9b09e-a7b8-4829-aac4-e88eb74c8e76.png)

12.IPv4 CIDR block: 10.0.2.0/23

![image](https://user-images.githubusercontent.com/103306835/224627510-0b64ec2e-90bc-42cd-9bef-9ff147173c05.png)

13.點選[Create subnet]

![image](https://user-images.githubusercontent.com/103306835/224627714-e0a6bff4-0ea7-4eb6-9802-60eca5101758.png)


# 步驟3：建立internet gateway


1.點選[Internet Gateways]

![image](https://user-images.githubusercontent.com/103306835/224628799-dc429158-c569-40bc-85de-4a348649e08a.png)

2.點選[Create internet gateway]

![image](https://user-images.githubusercontent.com/103306835/224629030-aeb5f89c-90ab-4897-9b21-d8a2bd0b615d.png)

3.Name tag: Lab IGW

![image](https://user-images.githubusercontent.com/103306835/224629667-3104ce1f-5e01-4f30-80f0-ba7d65ea9c01.png)

4.點選[Create internet gateway]

![image](https://user-images.githubusercontent.com/103306835/224629888-860bbd01-42f9-4f52-84f0-e267e0188bb8.png)

5.點選[Actions]->[Attach to VPC]

![image](https://user-images.githubusercontent.com/103306835/224630087-fedb2baf-a808-4281-b19c-6a47068cdb6f.png)

6.點選[Lab VPC]

![image](https://user-images.githubusercontent.com/103306835/224630273-f6d5580c-f07c-47c7-8f76-c5b179e03345.png)

7.點選[Attach internet gateway]

![image](https://user-images.githubusercontent.com/103306835/224630468-0b092141-2ae8-41b0-81a1-fb8dc371cfff.png)


# 步驟4：配置路由


1.點選[Route Tables]


2.查看 Route Tables

3.點選使用 Lab VPC 的 Route Tables

4.編輯 Name->[Private Route Table]

5.點選[Routes]

6.點選[Create route table]

7.Name: Public Route Table

VPC: Lab VPC

8.點選[Create route table]

9.
