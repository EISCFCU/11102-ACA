# 用 AWS CloudFormation串流動態內容

# 實施步驟

# 實施架構

![image](https://user-images.githubusercontent.com/103306835/234769385-024cb114-499d-4e6a-b8f2-4938bf377c8c.png)


# 步驟1：實驗室準備


1.搜尋 S3

![image](https://user-images.githubusercontent.com/103306835/234769416-bc21ea62-27e7-442d-b30a-9f5ce52a152b.png)

2.點選[S3]

![image](https://user-images.githubusercontent.com/103306835/234769437-444ba654-7b34-44af-b562-4c9abe91c4ab.png)

3.點選 bucket

![image](https://user-images.githubusercontent.com/103306835/234769462-2bcecdfe-fcf4-4251-a83a-8871e36d3edf.png)

4.點選[input]

![image](https://user-images.githubusercontent.com/103306835/234769512-3d417226-14a3-4b30-b474-8bc1a5b1c08e.png)

![image](https://user-images.githubusercontent.com/103306835/234769588-f27fbee0-7242-437e-948f-a64da72c9130.png)


# 步驟2：建立CloudFront Distribution


1.搜尋 CloudFormation

![image](https://user-images.githubusercontent.com/103306835/234770368-7b06654e-424c-45f5-aff8-d8302a65f8ef.png)

2.點選[CloudFormation]

![image](https://user-images.githubusercontent.com/103306835/234770404-e89ee38d-8f0c-4dea-82c2-50e2f631d44e.png)

3.點選[Create Distribution]

![image](https://user-images.githubusercontent.com/103306835/234791535-447ec9f6-bc1c-4e81-9d22-cbc81250a552.png)

4.Origin Domain Name：選擇S3 bucket的名稱

![image](https://user-images.githubusercontent.com/103306835/234792979-a93ae4ec-6bc9-4a5c-818c-acf2a921ebd2.png)

5.Restrict viewer access：No

![image](https://user-images.githubusercontent.com/103306835/234792867-5fce2f87-5e71-4096-8c1b-d4e8c07d002e.png)

6.點選[Create Distribution]

![image](https://user-images.githubusercontent.com/103306835/234793357-6bfcd524-2162-4b88-814d-c4ad187d17ce.png)


 # 步驟3：建立Elastic Transcoder
 
# 建立Pipeline

1.搜尋 Elastic Transcoder
 
 ![image](https://user-images.githubusercontent.com/103306835/234793969-b018973f-0e77-453b-acd7-929d3ed61642.png)

2.點選[Elastic Transcoder]
 
 ![image](https://user-images.githubusercontent.com/103306835/234794009-a3bde7f6-bb92-4cff-9ed3-b39facd0d796.png)

3.點選[Create a new Pipeline]

![image](https://user-images.githubusercontent.com/103306835/234794723-4414838b-62db-42ae-8f55-32182e1be3d5.png)

4.Pipeline Name：InputPipeline

Input Bucket：選擇awstrainingreinvent S3 bucket

IAM Role：Other roles->AmazonElasticTranscoderRole

![image](https://user-images.githubusercontent.com/103306835/234795508-bc161717-a8dd-4d50-8438-a38f0aca93cc.png)

5.[Configuration for Amazon S3 Bucket for Transcoded Files and Playlists]

Bucket：awstrainingreinvent S3 bucket

Storage Class：Standard

![image](https://user-images.githubusercontent.com/103306835/234795941-c75c92be-924a-41a7-b53a-482c68f4925e.png)

6.[Configuration for Amazon S3 Bucket for Thumbnails]

Bucket：awstrainingreinvent S3 bucket

Storage Class：ReducedRedundancy

![image](https://user-images.githubusercontent.com/103306835/234796396-372557ab-5ab2-481b-a7ad-b5b835128897.png)

7.點選[Create Pipeline]

![image](https://user-images.githubusercontent.com/103306835/234813823-3cf0a5d7-48d7-4f09-9ee4-d3606ab3df94.png)

# 建立Job

8.點選[Create New Job]

![image](https://user-images.githubusercontent.com/103306835/234814607-f106ce23-9297-4eba-9e9b-c27c71e174fe.png)

9.Pipeline：InputPipeline

Output Key Prefix：output/

Input Key：input/AmazonS3Sample.mp4

![image](https://user-images.githubusercontent.com/103306835/234815249-60c0211e-c63c-455b-b03d-a32b8070b6d1.png)

# 配置輸出細節

10. Preset：System preset: HLS 2M

Segment Duration：10

Output Key：HLS20M

![image](https://user-images.githubusercontent.com/103306835/234816492-a6328b9b-41c9-4314-ae70-b9eec2a99803.png)

11.點選[+ Add Another Output]

![image](https://user-images.githubusercontent.com/103306835/234816983-e3c99dbb-327e-4724-ba88-e6f1c358c1fd.png)

12. Preset：System preset: HLS 1.5M

Segment Duration：10

Output Key：HLS15M

![image](https://user-images.githubusercontent.com/103306835/234817838-3fe718f2-101a-4172-9ca9-cd80da2cd1e8.png)

13.Preset：System preset: HLS 1M

Segment Duration：10

Output Key：HLS10M

![image](https://user-images.githubusercontent.com/103306835/234818232-14d8dbae-50ce-444a-a451-c212beead031.png)

# 配置Playlist

14.點選[Add Playlist]

![image](https://user-images.githubusercontent.com/103306835/234818714-3128afcd-dd35-4ee9-9c8b-63b0a6d40720.png)

15.Playlist Name：primary

Playlist Format：HLSv3

![image](https://user-images.githubusercontent.com/103306835/234819297-53bf445a-52c7-4996-9fa0-f5a24255badc.png)

16.點選[Create New Job]

![image](https://user-images.githubusercontent.com/103306835/234819592-e720f236-6797-4aa7-9ecf-70f98e623cac.png)

# 步驟4：Test Playback

# 獲得雲端域名

1.點選[CloudFront]

![image](https://user-images.githubusercontent.com/103306835/234820716-98e6f0d9-8813-4b8b-ad9e-2c1f1df9ec36.png)

2.等待Status變成Deployed

