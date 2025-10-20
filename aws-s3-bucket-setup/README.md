My Amazon S3 Bucket Setup

This project shows how I created and configured an Amazon S3 bucket for public access.

The Steps I Followed

1. Logged into AWS Console and opened S3.
2. Clicked “Create bucket” and named it `anyasi-chineme-bucket`.
3. Turned off “Block all public access.”
4. Uploaded my file (`101415-video-720.mp4`).
5. Added the following policy to make items public:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::anyasi-chineme-bucket/*"
        }
    ]
}