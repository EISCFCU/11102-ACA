# Amazon Elastic File System (Amazon EFS)

# 實施步驟

# 實驗室目前架構

# 步驟1：建立安全群組


1.搜尋EC2

![image](https://user-images.githubusercontent.com/103306835/222338960-2dd218a9-567c-4db9-8e15-dbd7b45a8981.png)

2.點選[EC2]

![image](https://user-images.githubusercontent.com/103306835/222339040-1e90de29-5606-476d-a7aa-88b54c7263ea.png)

3.點選[Security Groups]

![image](https://user-images.githubusercontent.com/103306835/222339123-ac289c0d-1566-48d0-aea0-63d1606056be.png)

4.複製 Security GroupsID

![image](https://user-images.githubusercontent.com/103306835/222339226-bcb7c231-0af0-4bec-a3ea-9ea7450bc65c.png)

5.點選[Create security group]

![image](https://user-images.githubusercontent.com/103306835/222339294-6a3bc37b-e73b-444f-b0f5-3ffdf8f00db6.png)

6.輸入[Security group name：EFS Mount Target]

[Description：Inbound NFS access from EFS clients]

![image](https://user-images.githubusercontent.com/103306835/222339579-ab36a231-a9e9-45c4-b617-d28614cab5df.png)

7.選擇[Lab VPC]

![image](https://user-images.githubusercontent.com/103306835/222339701-6fe630fa-874c-4341-acca-340fdbe19b85.png)

8.點選[Add rule]

![image](https://user-images.githubusercontent.com/103306835/222339775-93be1a65-574f-4d1b-98ff-9214f7b92cdb.png)

9.Type: NFS

Source:Custom

![image](https://user-images.githubusercontent.com/103306835/222339902-f37ad064-0437-448d-a4e5-eb8e0e984e9e.png)

10.點選[Create security group]

![image](https://user-images.githubusercontent.com/103306835/222339992-b0b54d51-9155-48f7-ba84-5eb88a5d9b55.png)

# 步驟2：建立 EFS file system


1.點選[EFS]


2.點選[Create file system]

3.點選[Customize]

4.取消選取[Enable automatic backups]

5.Lifecycle management 選擇 None

6.Key: Name

Value: My First EFS File System



7.點選[Next]

8.點選[Lab VPC]

9.刪除default security group

10.點選[Next]

11.點選[Next]

12.點選[Create]


# 步驟3：連接EC2


1.點選[Details]->[Show]

2.點選[Download PPK]

3.複製 EC2PublicIP

4.打開[putty.exe]

5.點選[Connection]->Seconds between keepalives: 30

6.點選[Session]

7.輸入Host Name

8.點選[Credentials]

9.上傳[ labsuser.ppk]

10.點選[Open]

11.點選[Accept]

12.輸入[ec2-user]


# 步驟4：連接EC2


1.輸入[sudo mkdir efs]

2.點選[My First EFS File System]

3.點選[Attach]

4.複製 Using the NFS client

5.輸入[sudo df -hT]

6.輸入[df -hT]


# 步驟5：
