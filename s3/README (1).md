
# Hosting static website on AWS S3 Bucket 

This README affords step-by way of-step instructions on how to host a static website the usage of Amazon Web Services (AWS) Simple Storage Service (S3). Hosting a static website on S3 is a value-effective and scalable answer that permits you to serve HTML, CSS, JavaScript, and other static files with high availability and low latency.


## How to create s3 Bucket

- Log in to your AWS Management Console.
- Navigate to the S3 Dashboard.
- Click the "Create bucket" button.
- Choose a unique and descriptive name for your bucket (e.g., "my-static-website").
- Select the AWS region for your bucket.
- Leave all other settings at their default values and click "Create bucket."

## Configuration on S3 bucket
- After creating the bucket, select it from the S3 Dashboard.
- Go to the "Properties" tab.
- Scroll down to the "Static website hosting" section and click "Edit."
- Select the "Use this bucket to host a website" option.
- In the "Index document" field, enter the name of your main HTML file (e.g., "index.html").
- Optionally, you can specify an error document if you have one.
- Click "Save changes."
## Uploading
- In your S3 bucket, navigate to the "Objects" tab.
- Click the "Upload" button.
- Upload all your website files, including HTML, CSS, JavaScript, images, and any other assets.
- Make sure to maintain the directory structure of your website files.
## setting permissions
- Select your S3 bucket.
- Go to the "Permissions" tab.
- Click "Bucket policy" and add a policy to allow public access to your website files. 
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::chandar1stbucket/*"
        }
    ]
}
```
- save changes
## Accessing the Website
- Your static website is now hosted on AWS S3. You can access it using either the S3 bucket's website endpoint or your custom domain if you configured one.

- To access the website via the S3 endpoint, find the URL under the "Static website hosting" section in your bucket's properties.