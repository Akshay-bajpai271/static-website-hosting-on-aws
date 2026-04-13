
📌 Project Overview :

This project demonstrates how to host a static website using Amazon S3.
The website showcases an Ice Cream Brand, featuring visually appealing images and a simple responsive layout built using HTML and CSS.

The goal of this project is to understand:

Static website hosting on AWS S3
Frontend structure using HTML & CSS
Deployment of web content to the cloud

🚀 Features:

Simple and clean UI design
Responsive image gallery layout
Attractive header section
Static content hosted on AWS S3
Fast and scalable hosting

🛠️ Technologies Used:

HTML5 – Structure of the website
CSS3 – Styling and layout
AWS S3 – Static website hosting

📁 Project Structure :
├── index.html        # Main HTML file
├── style.css         # Styling file
├── canddy.webp       # Image used in gallery
├── candy.webp        # Banner image (optional)



🌐 Website Preview

The website includes:

A header with brand name and description
An image gallery displaying ice cream visuals
☁️ Deployment Steps (AWS S3)
Step 1: Create an S3 Bucket
Go to AWS S3 Console
Click on Create Bucket
Give a unique bucket name
Disable "Block all public access"

Step 2: Upload Files
Upload:
index.html
style.css
images (.webp files)

Step 3: Enable Static Website Hosting
Go to Properties tab
Enable Static website hosting
Set:
Index document: index.html

Step 4: Set Bucket Policy

Add the following policy to make your website public:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::YOUR-BUCKET-NAME/*"]
    }
  ]
}

Step 5: Access Website
Use the S3 website endpoint URL to view your site


