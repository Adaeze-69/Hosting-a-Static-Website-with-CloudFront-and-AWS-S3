# Hosting-a-Static-Website-with-CloudFront-and-AWS-S3


![Hosting-a-Static-Website-with-CloudFront-and-AWS-S3](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/5e62e28b-14db-48c7-888e-725ce3d9bf0e)


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

https://www.loom.com/share/752de16b21684e0aa3d04fbcbfa3a5d4?sid=3dacffd6-399b-4813-a268-e8d52a8bb145

![wedding invite](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/ace028dc-8d5c-42c7-9cbd-3b42fd72de57)

### Step 5 - Create a CloudFront Distribution to make your AWS S3 bucket private

i.Search for **Cloudfront** in your AWS console and click on it.

![cloudfront](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/014b8f20-4a98-4a2b-b6f5-672ee978d5c0)

ii. Click on **Create a CloudFront distribution** and populate it.

![CloudFront distribution](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/52c1afae-76b2-4f81-86d0-d8ab8ae9bcc5)

iii. There is no existing Origin Access Control (OAC) so we need to create one. Click on **Create new OAC**

![Origin Access Control (OAC)](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/9c1b4c3e-5f61-4631-8dd0-cd3670131c63)


iii. Under **Origin domain**, input the url you used in opening the your website which is found in your created  S3 bucket under **Properties** >> **Static website hosting**. If you see the **use website endpoint** in yours, do not click on it. If you do,you will not see the **Origin access control settings** which you need to set to make your bucket private.

![Origin domain](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/6c543aa3-47b0-4fbc-a8b9-87f198ffd494)

iv. You should get a page like this. Leave everything as default especially the **origin type** as S3. Then click **create**

![s3](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/1049aa08-440f-461d-900f-1e5b0cec5259)

v. Under **Web Application Firewall (WAF)**, click on the radio button **Do not enable security protections**. We just want to keep it simple.

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/cf075dc4-168d-4294-9016-f5911d7be1e6)

vi Leave everything as default and click **create distribution**
![create distribution](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/ebce8f5f-f104-4c06-9f5d-4778b737007f)

vii. Click on **create policy** and click on the circled url to paste the policy.

![create policy](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/c953f8b3-aeb3-494d-b05a-9d4ff89b004d)

viii. Navigate to **permissions** under your bucket and scroll to **bucket policy** and click **edit**. Delete the policy you pasted before which you used to see if your bucket was publicy accessible before we used cloudfront to make it private.Paste the copied policy in here. Scroll down and click on **save changes**. The policy can be found below also.

```
{
        "Version": "2008-10-17",
        "Id": "PolicyForCloudFrontPrivateContent",
        "Statement": [
            {
                "Sid": "AllowCloudFrontServicePrincipal",
                "Effect": "Allow",
                "Principal": {
                    "Service": "cloudfront.amazonaws.com"
                },
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::my-wedding-invitation/*",
                "Condition": {
                    "StringEquals": {
                      "AWS:SourceArn": "arn:aws:cloudfront::154334184944:distribution/E22OCAT2YCY14Z"
                    }
                }
            }
        ]
      }
```

![image](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/dbd33f6c-a2c1-44ba-bd05-901f6f075047)

ix. Navigate back to your cloudfront tab and copy the **Distribution domain name**. Paste it on your browser and add /index.html to it. i.e https://d3fvr8swd8au27.cloudfront.net/index.html Make sure to use your own **Distribution domain name**.

![Distribution domain name](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/aec88bdb-eb61-4507-b376-e522dbc842b7)

x. It would bring out your website page for you just like mine.

![website](https://github.com/Adaeze-69/Hosting-a-Static-Website-with-CloudFront-and-AWS-S3/assets/66219475/a694df26-16a8-451c-a3f7-48e7ae4b83f1)


## Conclusion

Based on the steps we have taking to achieve this, it can be implied that the tutorial describes how to set up a private static website with Amazon S3 and CloudFront. Enabling static website hosting with a public read policy and setting up an S3 bucket to store website files are among the procedures. For global access, fast transfer rates and minimal latency are therefore guaranteed by creating a CloudFront distribution for content delivery.

For the CloudFront distribution to control access to the S3 bucket, establishing an Origin Access Control (OAC) is an essential step in the procedure. To further make the S3 bucket private, the guide outlines how to remove the existing public read policy and change the bucket policy to limit access to only the CloudFront service.

The documentation concludes by showing you how to use CloudFront to enhance the security and performance of your static website hosted on S3, all the while keeping it private and only available via the CloudFront distribution.
