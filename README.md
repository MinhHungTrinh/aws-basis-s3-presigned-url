# aws-s3-presigned-url

Get Amazon web services(AWS) S3 bucket presigned URL. By providing the Access Key, Secret Key, Bucket name, Key, Expiry time and region name. It also uses HTML5 localstorage to save your recent data on browser.

## Getting Started

Just download it and start your node server. Currently it will run on port 10 you can change it in index.js file.

### Prerequisites

Node version >= 6.10.1 should be installed.

Create a S3 Bucket and configure CORS permission:
https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html
```$xslt
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "PUT",
            "POST",
            "DELETE",
            "GET"
        ],
        "AllowedOrigins": [
            "*"
        ],
        "ExposeHeaders": [],
        "MaxAgeSeconds": 3000
    }
]
```

Create IAM User or IAM Role (if you use EC2) have policy action (or S3FullAccessPolicy):
* PutObject
* GetObject

```
You can check Nodejs version by node -v
```

### Installing

Download or clone the project

start your server by `node index.js`

# Deployment
Update content in env file
```
REGION=
ACCESS_KEY=
SECRET_KEY=
BUCKET=
```
