# 用 AWS CloudFormation自動部署基礎設施

# 實施步驟

![image](https://user-images.githubusercontent.com/103306835/233300013-5fc0ec2f-1ca6-4acd-9da8-332a442c79bb.png)

# 步驟1：部署網路層


1.下載[lab-network.yaml

![image](https://user-images.githubusercontent.com/103306835/233280375-62bf5d62-de4a-415b-bbc4-0ff0b7f7c06b.png)

2.搜尋 CloudFormation

![image](https://user-images.githubusercontent.com/103306835/233280450-7d123789-24bf-4c5f-86a6-6ac558df7c18.png)

3.點選[CloudFormation]

![image](https://user-images.githubusercontent.com/103306835/233280496-8fcd3905-fc69-400a-9e61-69dc34af771b.png)

4.點選[Create stack]->[With new resources(standard)

![image](https://user-images.githubusercontent.com/103306835/233281934-5a08df56-b391-459b-a6ef-3bfd16b20c04.png)

5.Template source：Upload a template file

Upload a template file：Choose file->選擇[lab-network.yaml]

![image](https://user-images.githubusercontent.com/103306835/233285678-4da2f646-33f4-4f73-b665-e9f475cea171.png)

6.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233285788-6c29e2a6-0a6e-4457-b8cd-44edf39c759c.png)

7.Stack name：lab-network

![image](https://user-images.githubusercontent.com/103306835/233285956-28474f12-da41-41a4-8041-427aa6de1354.png)

8.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233286035-1020ef65-92d5-4a4f-bd6c-03571be9beff.png)

9.點選[Add new tag]

![image](https://user-images.githubusercontent.com/103306835/233286236-9acfb860-8137-4353-8f9d-be096bce7014.png)

10.Key: application

Value: inventory

![image](https://user-images.githubusercontent.com/103306835/233286523-784f4434-b0d9-4001-9ad9-bbb6d12729fc.png)

11.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233286641-32debfc9-62be-44f4-a1f4-efb65293c766.png)

12.點選[Submit]

![image](https://user-images.githubusercontent.com/103306835/233287144-abc75332-0432-4a82-8010-6e25a58de7dc.png)

13.點選[Stack info]->等待狀態變成CREATE_COMPLETE

![image](https://user-images.githubusercontent.com/103306835/233288684-664a4012-2df7-4879-8b3a-ee8aa09a3178.png)

14.點選[Resources]

![image](https://user-images.githubusercontent.com/103306835/233289376-34ee915d-ea93-4fbd-94e8-00bffd6fc282.png)

15.點選[Events]

![image](https://user-images.githubusercontent.com/103306835/233289671-c6420daa-22e9-48d4-9cad-1323e25ed072.png)

16.點選[Outputs]

![image](https://user-images.githubusercontent.com/103306835/233290372-7fa6aaea-107f-4d1b-a2c6-1211ed05024c.png)

17.點選[Template]

![image](https://user-images.githubusercontent.com/103306835/233290864-61346e42-c463-4ef9-9fe4-cfc6761730dc.png)

![image](https://user-images.githubusercontent.com/103306835/233290891-bf383ee6-de99-43ed-8588-758441df314c.png)


# 步驟2：部署應用層


1.下載[lab-application.yamll

![image](https://user-images.githubusercontent.com/103306835/233291320-67eea0fc-7c96-413a-9c2e-d3edbf74a4c6.png)

2.點選[Stacks]

![image](https://user-images.githubusercontent.com/103306835/233291439-ab0a3a94-1902-4241-8268-15231b5fae95.png)

3.點選[Create stack]->[With new resources(standard)

![image](https://user-images.githubusercontent.com/103306835/233291696-43dc938e-7eeb-4f18-8148-0fb9d30b8333.png)

4.Template source：Upload a template file

Upload a template file：Choose file->選擇[lab-application.yaml]

![image](https://user-images.githubusercontent.com/103306835/233291749-758d8297-5dc0-4dd8-bab0-6d1c81599e2b.png)

5.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233291923-f4b07ef0-b76e-44e8-bcdd-598e6f0befc9.png)

6.Stack name: lab-application

![image](https://user-images.githubusercontent.com/103306835/233292040-a8c881fa-7eb9-4f27-9bc5-e01c303fddd3.png)

7.NetworkStackName: lab-network

![image](https://user-images.githubusercontent.com/103306835/233292196-9216503d-2d68-411c-bc5e-0f02f0839c34.png)

8.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233292332-b67375da-2525-41e8-a444-3114ff3f8e26.png)

9.點選[Add new tag]

![image](https://user-images.githubusercontent.com/103306835/233292495-8394873a-0d3b-44d9-a421-4abe12d57d0f.png)

10.Key: application

Value: inventory

![image](https://user-images.githubusercontent.com/103306835/233292638-e36423fe-4219-4358-ad39-3aaa95fc47b5.png)

11.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233292712-978ff6c7-36bd-41f8-93b1-680b23997241.png)

12.點選[Submit]

![image](https://user-images.githubusercontent.com/103306835/233292793-df88add3-2f27-4258-be44-6a10f739c587.png)

13.點選[Stack info]->等待狀態變成CREATE_COMPLETE

![image](https://user-images.githubusercontent.com/103306835/233292930-f566b792-ed41-4385-8726-066956f1dad3.png)

14.點選[Outputs]->複製URL

![image](https://user-images.githubusercontent.com/103306835/233293050-ccf808d9-cdd8-49e1-900b-af3cc8c04077.png)

![image](https://user-images.githubusercontent.com/103306835/233293293-93bfb05c-7a7c-4be6-bfd5-b7de15f3eecc.png)


# 步驟3：更新 Stack


1.搜尋 EC2

![image](https://user-images.githubusercontent.com/103306835/233293859-a99e6554-29d2-4f53-952b-073650396818.png)

2.點選[Security Groups]

![image](https://user-images.githubusercontent.com/103306835/233293994-4a08fd98-a4cd-4e1a-8472-588640ff7d4b.png)

3.點選[lab-application-WebServerSecurityGroup....]

![image](https://user-images.githubusercontent.com/103306835/233294124-d42c72e6-d7e7-4584-8ddd-dd2bb9dcad03.png)

4.點選[Inbound rules]

![image](https://user-images.githubusercontent.com/103306835/233294339-c664a973-7e5c-4432-b573-bd9ddc2f1f78.png)

![image](https://user-images.githubusercontent.com/103306835/233294366-b7582ef6-87ee-42eb-9ac6-56194c97164c.png)

5.搜尋 CloudFormation

![image](https://user-images.githubusercontent.com/103306835/233294459-89b7973f-b524-428c-83f3-d47ebe097a7d.png)

6.下載 lab-application2.yaml

![image](https://user-images.githubusercontent.com/103306835/233294529-e0ba0699-b9ad-4855-a44b-95abddabfd99.png)

7.點選[lab-application]

![image](https://user-images.githubusercontent.com/103306835/233294656-e83387c9-64ab-436a-aa89-7f6fa37fafe7.png)

8.點選[Update]

![image](https://user-images.githubusercontent.com/103306835/233294764-c94f6b76-c517-4ae4-8c37-cd2f3df49aa0.png)

9.點選[Replace current template]

![image](https://user-images.githubusercontent.com/103306835/233294868-289636bf-0f6c-4b6f-bf5a-e8be42125a5f.png)

10.點選[Upload a template file]

Choose file->選擇[lab-application2.yaml]

![image](https://user-images.githubusercontent.com/103306835/233295164-20ca3c3b-fb10-40f3-ac11-256e39b9a40e.png)

11.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233295252-386fa5fd-e05b-48b2-96db-96b1b08abb19.png)

12.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233295433-ff97f659-0f97-4039-924b-30483e9b59a3.png)

13.點選[Next]

![image](https://user-images.githubusercontent.com/103306835/233295524-8e2c6d57-ebd6-448e-b47d-89174931688c.png)

14.在Change裡可以看到更新的部分

![image](https://user-images.githubusercontent.com/103306835/233295761-cd3d2b5a-ab92-437c-b71b-d43b92268412.png)

15.點選[Submit]

![image](https://user-images.githubusercontent.com/103306835/233295850-eeac9e64-947c-4eae-b526-e565978b9827.png)

16.點選[Stack info]->等待狀態變成CREATE_COMPLETE

![image](https://user-images.githubusercontent.com/103306835/233295970-1c10392e-83b7-4e72-a711-3b827e7d74b2.png)

17.搜尋 EC2

![image](https://user-images.githubusercontent.com/103306835/233296082-45d79ed1-7485-46ff-a794-2d428c204934.png)

18.點選[Security Groups]

![image](https://user-images.githubusercontent.com/103306835/233296203-d481d834-2b72-4d7f-a959-0145624d7719.png)

19.點選[lab-application-WebServerSecurityGroup]->[Inbound rules]

![image](https://user-images.githubusercontent.com/103306835/233296397-6e7420d6-e14c-456f-84fd-98801e6a2fa9.png)

![image](https://user-images.githubusercontent.com/103306835/233296556-a100eea6-90c6-47ca-b5e1-b401b3f4dba2.png)


# 步驟4：探索範本


1.搜尋 CloudFormation

![image](https://user-images.githubusercontent.com/103306835/233296873-1de5f924-d3e6-42a3-8904-97294c31901c.png)

2.點選[Designer]

![image](https://user-images.githubusercontent.com/103306835/233296967-0257e62c-e723-429d-9cca-2aa978421632.png)

3.點選[Open][Local file]->[lab-application2.yaml]

![image](https://user-images.githubusercontent.com/103306835/233297177-299bf514-0024-413a-8d9b-12cc98b9ec92.png)

4.點選[Local file]

![image](https://user-images.githubusercontent.com/103306835/233297310-c0581c05-1dff-4ef6-afdb-357bae7837ad.png)

5.點選[lab-application2.yaml]

![image](https://user-images.githubusercontent.com/103306835/233297442-8da4c540-7eb7-4241-9098-a19c21270059.png)


# 步驟5：刪除stack


1.點選[Close]

![image](https://user-images.githubusercontent.com/103306835/233297793-438de413-9111-486a-94ed-cd4baf260dd7.png)

2.點選[離開]

![image](https://user-images.githubusercontent.com/103306835/233297903-972d2812-37a8-427b-8012-09e7ff57b0e6.png)

3.點選[lab-application]

![image](https://user-images.githubusercontent.com/103306835/233298023-e5c5088d-ad0d-4a54-9f51-787e1ab65975.png)

4.點選[Delete]

![image](https://user-images.githubusercontent.com/103306835/233298109-dc3e5736-b530-4e08-b21c-67f7fdae6146.png)

5.點選[Delete stack]

![image](https://user-images.githubusercontent.com/103306835/233298192-27b85e61-d023-46a8-8ec0-a10dc567b251.png)

6.等到stack消失

![image](https://user-images.githubusercontent.com/103306835/233298353-03152fbb-9807-4e02-96a9-aa34699d2da6.png)

7.搜尋 EC2

![image](https://user-images.githubusercontent.com/103306835/233298479-5a6d32bc-9799-4447-940a-bacfd16c0396.png)

8.點選[Snapshots]

![image](https://user-images.githubusercontent.com/103306835/233298590-d91ee32c-1df4-49ab-bbc8-52267248c321.png)

9.會看到一個幾分鐘之前建立的Snapshot

![image](https://user-images.githubusercontent.com/103306835/233298759-50a0a22f-dd66-4fbe-95b0-cb4629b17958.png)
