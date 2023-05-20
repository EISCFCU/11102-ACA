混合儲存和數據遷移

# 實施步驟

# 實施架構

# 步驟1：檢查實驗室架構

1.搜尋 S3

2.點選[S3]

3.點選[Create bucket]

4.輸入Bucket name

Region：us-east-2

5.Bucket Versioning: Enable

6.點選[Create bucket]

7.點選[Create bucket]

8.輸入Bucket name

Region: us-west-2

9.Versioning: Enable

10.點選[Create bucket]

# 步驟2：啟動跨區域複製

1.點選在US East的Bucket

2.點選[Management]->[Create replication rule]

3.Replication rule name: crr-full-bucket

Status：Enabled

4.點選[Apply to all objects in the bucket]

5.點選[Choose a bucket in this account]

點選[Browse S3]

6.選擇在US West的Bucket->[Choose path]

7.IAM role: S3-CRR-Role 

8.點選[Save]

9.點選[No]->[Submit]

10.點選在US East的Bucket

11.點選[Upload]

12.點選[Add files]

13.點選[Upload]

14.點選[Close]

上傳的檔案也會複製到US West的Bucket

# 步驟3：配置File Gateway和建立NFS file share


1.[Services]->[Storage]->[Storage Gateway]

2.點選[Create gateway]

3.Gateway name: File Gateway

4.Gateway type: Amazon S3 File Gateway

5.Host platform: choose Amazon EC2

6.點選[Amazon EC2]->[Customize your settings]->[Launch instance]

7.Name: File Gateway Appliance

8.Instance type：t2.xlarge

Key pair:vockey

9.VPC: On-Prem-VPC

Subnet: On-Prem-Subnet

Auto-assign public IP: Enable

Select an existing security group

10.選擇名字有FileGatewayAccess的security group和OnPremSshAccess

11.點選[Add new volume]

12.size ： 150GiB

13.點選[Launch instance]

14.點選[View all instances]

15.複製Public IPv4 address

16.點選[Next]

17.點選[Publicly accessible]

18.點選[Next]

19.點選[Activate gateway]

20.CloudWatch log group: Deactivate logging

21.CloudWatch alarms: No Alarm

22.點選[Configure]

23.點選[File shares]

24.點選[Create file share]

25.AWS region: us-east-2

Access objects using: Network File System (NFS)

26.點選[Next]
