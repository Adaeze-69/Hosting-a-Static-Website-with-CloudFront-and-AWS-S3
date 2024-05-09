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

### S
