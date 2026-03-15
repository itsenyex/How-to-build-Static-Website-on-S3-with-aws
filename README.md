# How-to-build-Static-Website-on-S3-with-aws
I'll guide you through building a static website on Amazon S3. This is a cost-effective way to host websites with HTML, CSS, and JavaScript.
Step-by-Step Guide:

1. Create an S3 Bucket
   
Sign in to AWS Console and navigate to S3
Click "Create bucket"
Enter a bucket name (use your domain name if you plan to use a custom domain, like example.com)
Choose your AWS region
Uncheck "Block all public access" (you'll need public access for a website)
Acknowledge the warning about public access
Click "Create bucket"

2. Upload Your Website Files

Click on your newly created bucket
Click "Upload"
Add your files (index.html, CSS, JS, images, etc.)
Make sure you have an index.html file as your homepage
Optionally add an error.html for custom error pages
Click "Upload"

3. Enable Static Website Hosting

In your bucket, go to the "Properties" tab
Scroll down to "Static website hosting"
Click "Edit"
Select "Enable"
Set Index document to index.html
Set Error document to error.html (optional)
Click "Save changes"
Note the bucket website endpoint URL provided

4. Set Bucket Policy for Public Access

Go to the "Permissions" tab
Scroll to "Bucket policy"
Click "Edit" and paste this policy (replace your-bucket-name):
Click "Save changes"

5. Access Your Website
   Your website will be available at the endpoint URL, which looks like:

http://your-bucket-name.s3-website-region.amazonaws.com



Optional Enhancements
Add a Custom Domain with Route 53:

Register or transfer your domain to Route 53
Create a hosted zone
Add an A record alias pointing to your S3 bucket

Add HTTPS with CloudFront:

Create a CloudFront distribution
Set your S3 bucket as the origin
Add an SSL certificate from AWS Certificate Manager
Update DNS to point to CloudFront

Enable Versioning:

In bucket Properties, enable versioning to keep file history
