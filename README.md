# ☁️ AWS Serverless Website

> A fully serverless website built on AWS — no servers to manage, auto-scaling, and near-zero cost at low traffic.

![Architecture](docs/architecture.png)

## 🏗️ Architecture

| Service | Role |
|---|---|
| S3 | Hosts static files (HTML, CSS, JS) |
| CloudFront | CDN, HTTPS, edge caching |
| Route 53 | DNS routing |
| API Gateway | HTTP API endpoints |
| Lambda | Backend business logic |
| DynamoDB | Serverless NoSQL database |
| Cognito | User authentication (optional) |

## 🚀 Deploy

```bash
# Install AWS SAM CLI
brew install aws-sam-cli

# Deploy the stack
sam build && sam deploy --guided

# Upload frontend
aws s3 sync ./frontend s3://your-bucket-name
```

## 💸 Cost

Runs on AWS Free Tier — 1M Lambda requests, 5GB S3,
1TB CloudFront transfer, and 25GB DynamoDB free per month.

## 📄 License

MIT — [yourname] · [Year]
