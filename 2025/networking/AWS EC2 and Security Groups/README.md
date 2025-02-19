# AWS EC2 Instance & Security Groups Guide

## 🚀 Launch an AWS EC2 Instance (Free Tier)

Follow these steps to launch an EC2 instance on AWS:

### 1️⃣ Log in to AWS
- Go to the [AWS Management Console](https://aws.amazon.com/console/).
- Navigate to **EC2 Dashboard** and click **Launch Instance**.

### 2️⃣ Choose an Amazon Machine Image (AMI)
- Select an OS, e.g., **Ubuntu 22.04 LTS** or **Amazon Linux**.

### 3️⃣ Select an Instance Type
- Choose **t2.micro** (Free Tier Eligible).

### 4️⃣ Configure Instance Details
- Keep default settings or adjust as needed.

### 5️⃣ Add Storage
- Default is **8GB (gp2)**; modify if required.

### 6️⃣ Configure Security Group (Important 🔐)
- Click **Create a new security group**.
- Name it: `MyWebServerSG`
- Add **Inbound Rules**:
  | Protocol | Port | Source |
  |----------|------|--------|
  | SSH | 22 | My IP (recommended) |
  | HTTP | 80 | Anywhere (for web access) |
  | HTTPS | 443 | Anywhere (for secure web access) |
- **Outbound Rules**: Keep **Allow All** (default).

### 7️⃣ Launch and Connect to Your Instance
- Click **Launch** and select a key pair.
- Use SSH to connect:
  ```
  ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
  ```

---

## 🔧 Modifying Security Group Rules (Post Launch)
1. Go to **EC2 Dashboard > Security Groups**.
2. Select your security group (`MyWebServerSG`).
3. Click **Edit Inbound Rules**.
4. Modify rules (e.g., restrict SSH access to a specific IP).
5. Click **Save Rules**.

---

## 📌 Testing Security Group Rules
- **Check allowed services**: Try accessing your EC2 instance via SSH, HTTP, or HTTPS.
- **Verify restrictions**: Attempt access from a blocked IP to ensure security.

---
