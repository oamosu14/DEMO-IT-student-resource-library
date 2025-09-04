# Lab: Deploy an EC2 Instance on AWS Free Tier

## Objective
Learn how to create a virtual server (EC2) and connect to it via SSH.

## Steps
1. Log in to AWS Management Console.
2. Navigate to EC2 → Instances → Launch Instance.
3. Choose **Amazon Linux 2 AMI (Free Tier)**.
4. Select **t2.micro** instance type (free tier eligible).
5. Configure instance details (leave default settings for this lab).
6. Create a new key pair (download `.pem` file).
7. Launch the instance.
8. Connect via terminal:
   ```bash
   ssh -i "your-key.pem" ec2-user@<Public-IP-address>

Run basic Linux commands (ls, pwd, whoami) to verify connectivity.


---

### **Example AWS lab: labs/s3-storage-demo.md**
```markdown
# Lab: Create and Use an S3 Storage Bucket

## Objective
Learn how to create an S3 bucket and upload/download files.

## Steps
1. Log in to AWS Management Console → S3.
2. Click "Create bucket" → name it uniquely.
3. Choose region, leave default settings, click "Create bucket".
4. Click bucket → "Upload" → select a test file.
5. After upload, download to verify file integrity.

## Notes
- S3 free-tier provides 5GB of storage.
- Practice organizing files and setting permissions.


Next Steps
Repeat similar structure for Azure labs (deploy-vm.md, blob-storage-demo.md).
Add screenshots or command snippets to make it beginner-friendly.
Optional: create cloud-platforms/images/ for visual aids.
