# 📅 Day 5: Create GP3 Volume

---

## 🧠 Task

Create an AWS EBS volume with the following specifications:

* Name: `devops-volume`
* Volume Type: `gp3`
* Size: `2 GiB`
* Region: `us-east-1`

---

## 🎯 Objective

* Understand EBS volume creation
* Work with **gp3 (General Purpose SSD)** volumes
* Practice AWS resource provisioning

---

## ☁️ AWS Details

* Service: Amazon EC2 (EBS)
* Region: us-east-1
* Volume Name: `devops-volume`
* Volume Type: gp3
* Size: 2 GiB

---

## 🚀 Steps to Execute (AWS Console)

### 1. Login to AWS Console

* Use provided credentials
* Select region: **us-east-1**

---

### 2. Navigate to EC2

* Search for **EC2**
* Open EC2 Dashboard

---

### 3. Create Volume

* Go to **Elastic Block Store → Volumes**
* Click **Create Volume**

---

### 4. Configure Volume

* Volume Type → `gp3`
* Size → `2 GiB`
* Availability Zone → Select any AZ in us-east-1 (e.g., us-east-1a)

---

### 5. Add Name Tag

* Key → `Name`
* Value → `devops-volume`

---

### 6. Create Volume

* Click **Create Volume**

---

## 💻 AWS CLI Method (Corrected)

### ✅ Single-line command (recommended)

```bash id="k3d9xp"
aws ec2 create-volume --availability-zone us-east-1a --size 2 --volume-type gp3 --tag-specifications 'ResourceType=volume,Tags=[{Key=Name,Value=devops-volume}]'
```

### ✅ Multi-line command (proper format)

```bash id="p9g2ml"
aws ec2 create-volume \
  --availability-zone us-east-1a \
  --size 2 \
  --volume-type gp3 \
  --tag-specifications 'ResourceType=volume,Tags=[{Key=Name,Value=devops-volume}]'
```

> Note: When using `\`, it must be at the end of the line and the next argument should be on a new line.

---

## 🔍 Verification

```bash id="c8q2yb"
aws ec2 describe-volumes --filters "Name=tag:Name,Values=devops-volume"
```

---

## 💡 Key Learning

* gp3 volumes provide better performance and flexibility than gp2
* EBS volumes act as block storage for EC2 instances
* Proper CLI formatting is crucial to avoid errors

---

## ⚠️ Challenges Faced

* Incorrect CLI formatting using `\`
* Understanding how AWS CLI parses arguments

---

## 🧩 Summary

Created a gp3 EBS volume with correct CLI formatting, ensuring proper resource provisioning and avoiding command errors.

---
