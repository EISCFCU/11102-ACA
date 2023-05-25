# 混合儲存和數據遷移

# 實施步驟


# 實施架構

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/f796522b-5075-47ac-a380-481761dc400c)

# 步驟1：檢查實驗室架構

1.搜尋 S3

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/b85f17dc-4cf0-4823-bd56-e8e95da9bda5)

2.點選[S3]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/2758530a-8f42-499f-b90a-de21425a5b9b)

3.點選[Create bucket]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/61552567-89ac-4cc1-8c87-29029f689049)

4.輸入Bucket name

Region：us-east-2

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/51a1d75e-54ae-44cd-8967-fcdfba5a81db)

5.Bucket Versioning: Enable

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/db39b67f-6372-4c61-a49e-bc099ce77c86)

6.點選[Create bucket]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/8a1c9194-4f27-4a04-9fdd-e9f688bd16c5)

7.輸入Bucket name

Region: us-west-2

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/e4d922ef-b37e-4e10-8ca5-6e311cf11900)

8.Versioning: Enable

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/78811535-889c-49b7-a32b-7589adf5cec1)

9.點選[Create bucket]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/664f8df6-3049-4ef8-b180-3c3793008c05)


# 步驟2：啟動跨區域複製

1.點選在US East的Bucket

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/6ee880f3-f56e-436d-a1be-9cccd51cef19)

2.點選[Management]->[Create replication rule]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/96d08044-f8fa-44c8-b116-83521a5dd9f5)

3.Replication rule name: crr-full-bucket

Status：Enabled

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/aedc1bf2-d9a0-4aa1-8a11-f176f8c28aec)

4.點選[Apply to all objects in the bucket]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/e4ac0430-867a-4d35-9aed-0024c6366032)

5.點選[Choose a bucket in this account]

點選[Browse S3]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/d6e67c04-7c1a-4471-afb2-523ea4868f77)

6.選擇在US West的Bucket->[Choose path]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/bd4f3664-1c62-4ecc-a03d-15196d248676)

7.IAM role: S3-CRR-Role 

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/c10267d2-3e7c-4ebd-ba9e-557ab33a42aa)

8.點選[Save]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/fc3468e9-6167-4df7-8d64-1b6e3c546429)

9.點選[No]->[Submit]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/b16f5f8c-4af8-4b4a-b5a6-90772f916ff7)

10.點選在US East的Bucket

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/06311c5d-a4c5-4b69-be1b-e34ed27169b1)

11.點選[Upload]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/3dd2b7e5-6ae0-445b-986d-3582fcfbca74)

12.點選[Add files]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/70ab35da-f833-4bd2-9993-470843ff9294)

13.點選[Upload]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/dd3b3ce4-7498-446e-9744-978460e5ce58)

14.點選[Close]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/cc8b6dde-72c7-4683-8c57-fcf566ad2e8e)

15.上傳的檔案也會複製到US West的Bucket

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/1a2dcd44-5c4a-4d64-a774-9cc42386eab4)

# 步驟3：配置File Gateway和建立NFS file share


1.點選[Storage Gateway]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/11d6861c-71fc-4e6b-9f09-9db4141b74b8)

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/546ba6a8-a1b1-4cb6-8047-87c2283e1e69)

2.點選[Create gateway]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/94529297-3117-4871-a198-dd16550891ae)

3.Gateway name: File Gateway

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/61bcc053-9e87-4eb0-9432-095c8ec54b9a)

4.Gateway type: Amazon S3 File Gateway

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/e8a4970d-ee5a-48bd-99c0-61581d7d1daa)

5.Host platform: choose Amazon EC2

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/bb9a1c03-67b2-4b4c-86ca-229438a20136)

6.點選[Launch instance]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/6e725608-bbcc-4c6c-9e4b-4547853f6cc1)

7.Name: File Gateway Appliance

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/afee0bb8-7b1e-4788-9bfc-0dd425860672)

8.Instance type：t2.xlarge

Key pair:vockey

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/ee6470b4-fbee-48c1-9b0e-7d2a125b5a4f)

9.VPC: On-Prem-VPC

Subnet: On-Prem-Subnet

Auto-assign public IP: Enable

Select an existing security group

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/20011953-cdf0-4742-a013-4a2ee55e9c5a)

10.選擇名字有FileGatewayAccess的security group和OnPremSshAccess

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/73f999aa-421e-4686-9119-93a5e6ca7b48)

11.點選[Add new volume]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/d15b8c80-80c5-4fd2-8757-a5cb56ba531c)

12.size ： 150GiB

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/7d9de9eb-0165-4369-8299-06c9d9ea4ade)

13.點選[Launch instance]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/90cae737-ecdf-4e84-81ae-5e919e79a631)

14.點選[View all instances]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/dadb14e7-97b3-4b2f-8d46-3fe2732d972f)

15.複製Public IPv4 address

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/5d664af6-6a4e-4cf3-a352-c04094be2412)

16.點選[Next]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/1ff90075-11e6-4c07-bcda-4f31c48cb9b0)

17.點選[Publicly accessible]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/c776f907-08ee-4e01-8b64-75f946f84cc5)

18.點選[Next]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/211f6800-10b8-4a9d-aab8-cc3cda86e84c)

19.點選[Activate gateway]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/f19b5640-48ce-41d4-a4c0-9f47c26933dc)

20.CloudWatch log group: Deactivate logging

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/3b89dd99-05e7-4c2f-95a4-28a73a3bd4d5)

21.CloudWatch alarms: No Alarm

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/2231c36f-6343-45b0-b3ce-7c4a86bff756)

22.點選[Configure]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/e6a185d2-8622-48eb-a840-53cce244c09e)

23.點選[File shares]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/ca4c5267-89d0-460e-a158-ba3f19d7e7b5)

24.點選[Create file share]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/b7974d1d-39cf-49fe-b98d-c542ed150461)

25.AWS region: us-east-2

Access objects using: Network File System (NFS)

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/6974a8d9-51e4-4541-83b4-76822475cb09)

26.點選[Customize configuration]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/e5aa5327-e224-4bbb-977f-357e000081c8)

27.AWS region: US East (Ohio) us-east-2

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/308e4da7-e5fa-42fa-87a6-cf7eb02fd89f)

28.點選[Save]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/a00711f0-7df0-4a68-b2c4-06dc5a4a7201)

29.Object metadata:Guess MIME type、Give bucket owner full control

Access your S3 bucket: Use an existing IAM role

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/b3efdff0-0597-4c16-8281-0b24491fb9bc)

30.IAM role:複製FgwIamPolicyARN value

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/1d9ee2c0-fba2-404e-9c10-89541ca33fa7)

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/7cbebb9a-e8a1-4cbc-939f-1f7a6a989317)

31.點選[Save]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/a44b7935-7deb-43a5-ac3e-862d4a19934a)

32.點選[Creat]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/4692c44a-b537-4891-80eb-f7174e284909)

33.點選剛才建立的file share

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/146a9aba-ef78-4260-b8dd-8567b6077a33)

# 步驟4：將file share安裝在Linux實例上並遷移數據


1.點選[Details]->[Show]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/f4fded32-361c-4fc5-aca9-8d6b0bdabd10)

2.點選[Download PPK]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/20477b9f-c145-42e9-b2b3-33a85bdacc9b)

3.複製[OnPremLinuxInstance address]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/6fbe60a5-78d5-4a56-87cd-d555d66e2c8c)

4.下載PuTTY

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/d8b3b3c7-56a8-4a26-a182-dc32e97e4ad8)

5.打開[putty.exe]

![image](https://github.com/EISCFCU/11102-ACA/assets/103306835/fcf55b28-5c0a-4d2e-9b13-e0f2d2b8da5f)

6.
