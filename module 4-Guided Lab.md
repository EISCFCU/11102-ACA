# Amazon Elastic File System (Amazon EFS)

# 實施步驟

# 實驗室目前架構

# 步驟1：建立安全群組


1.搜尋EC2

2.點選[EC2]

3.點選[Security Groups]

4.複製 Security GroupsID

5.點選[Create security group]

6.輸入[Security group name]、[Description]

7.選擇[Lab VPC]

8.點選[Add rule]

9.Type: NFS

Source:Custom



10.點選[Create security group]


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
