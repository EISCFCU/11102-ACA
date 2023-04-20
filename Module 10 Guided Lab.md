# 用 AWS CloudFormation自動部署基礎設施

# 實施步驟

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

5.
