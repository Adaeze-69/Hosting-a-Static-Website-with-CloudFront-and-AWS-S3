# Hosting-a-Static-Website-with-CloudFront-and-AWS-S3

## Overview
Create a static website on Amazon S3 bucket(private bucket) but with public read policy assigned, using cloud front for Content Delivery Network.

## Introduction

### Amazon S3

Amazon Web Services (AWS) provides scalable, high-performance object storage with its Amazon S3 (Simple Storage Service) offering. A key element of Amazon S3 is an S3 bucket, which serves as a container for objects (files and the metadata that goes with them) in a flat namespace. 

### Static Website

Without any dynamic server-side processing, a static website is one that is made up of fixed, pre-built HTML, CSS, and JavaScript files that are sent straight to the user's web browser. This indicates that during a user's session, the content on the website remains unchanged regardless of user interactions or input from outside sources. Businesses and individuals looking for a quick, safe, and simple way to maintain an online presence for informative content, including landing pages, blogs, or portfolios, should consider using static websites.

### Amazon CloudFront

A service offered by Amazon Web Services (AWS) is Amazon CloudFront, a content delivery network (CDN). Its goal is to provide high transfer speeds and minimal latency in content delivery to end consumers globally. Application data and both static and dynamic content can be delivered more quickly to users in various geographical locations when using CloudFront. 
Employing Amazon CloudFront enables businesses to deliver their apps and content closer to end users, improving speed and availability and resulting in quicker load times and an improved user experience.

## Prerequisite

1. An AWS account
2. The files to upload for your static website.

## Steps 

### Step 1: Create a Bucket on Amazon S3

i. Log into your AWS console and use the search bar to search for **S3** and click on it.

![S3](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/9ec43daa-1ede-496c-852e-fa36d570c081)

ii. Click on **create bucket** so as to input your bucket name.

![bucket](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/60f3d487-3437-49b4-8c83-e3b537d1df86)

iii. Input a bucket name in the **Bucket name** with a unique name which has not been used before. Go ahead and untick **Block all public access**

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/f1fa2ded-6659-4d5d-99ea-b72ac321e03f)

iv. Scroll down and click the **acknowledgment** box.

![acknowledgment](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/097104e0-9fc0-4a04-850f-2f859568728d)

iv. Leave every other thing as default and scroll down and click **create bucket**.

![create bucket](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/8072c6f8-fb78-41b1-8ab7-ef9c824d61f9)

### Step 2: Upload Website files to S3 Bucket

i. Click on the bucket name so you can upload your website files into the bucket.

![my wedding invitation](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/a78a6759-43ed-4549-97f3-ee53da2b29c6)

ii. Click on **upload** and select the files from your local file storage. Do well not to upload the overall folder carrying the other folders. Upload the folders one after the other so it opens on your browser along the line.

![upload](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/5753c604-1914-4e47-91a5-5e219b0bda3d)

iii. Click on **upload folders** and upload your folders from there. You can upload a file if that is what you have.

![upload folders](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/83eceb19-8b4c-47f2-81ad-a21a7e645ea2)

iv. After uploading the folders from your local file storage, click on **Upload**.

![upload](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/dcd58e92-6c6c-4ada-98a4-8663e63da07a)

v. Give it some time to populate and upload. You will eventually see a small green banner after a while to indicate that it was successful.

![populatw](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/a3072693-a99b-46e5-a753-18a312f41fa9)
![successful](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/fdf2c8cf-2a2d-4a1e-8f0a-ff95498cc8d1)

### Step 3:Enable Static Website Hosting on S3 Bucket Created

i. Click on the **close** button and see all your files or folders. Click on the **Properties** tabs and scroll down to **Static website hosting**

![Static website hosting](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/71fb0efe-4f2c-41e4-b71d-7ff721af1830)

ii. Click on **Edit** on **Static website hosting**

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/fd3f19e7-a597-4112-bc00-5384b67c1350)

iii. Click on the radio button **Enable**. Under **hosting type**, click on **Host a static website**. Under **Index document**, type *index.html* in it.

![Static website hosting](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/c47d1f79-a154-4026-80b8-652d2b86d751)

iv. Leave every other thing as default and scroll down and click on **save changes**

![save changes](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/e739ef18-4c73-486d-85e6-df316bc4f338)

### Step 4 - Attach a Bucket Policy

i. Click on **Permissions** tab and scroll down to **Bucket policy**

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/638dddb4-1ee1-426b-bad2-6002a868b699)

ii. Click on **Edit** under **Bucket policy** to input your bucket poilicy to allow access the website on the S3 bucket.

![Bucket policy](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/d75c5092-6d0c-45a7-860e-86d1df4c6383)

iii. Attach the policy below and replace *bucket name* with your bucket name. Scroll down and click on **save changes**.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::<bucket name>/*"
        }
    ]
}
```

![policy](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/c4ef00f0-4d65-4b83-b34d-32fbba9d8e21)

iv. Click on the **Properties** tabs and scroll down to **Static website hosting** and copy  the link there to open on your browser.

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/e282912a-17af-4320-9d87-e1873e05bfb8)

v. When you open it if you everything right, you should see the static website here. This is what mine looks like.

![wedding invite](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/ace028dc-8d5c-42c7-9cbd-3b42fd72de57)

