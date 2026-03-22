# 📅 Day 1: Create Key Pair (AWS)

## 🎯 Task

Create an AWS key pair with:

* **Name:** `datacenter-kp`
* **Type:** `RSA`
* **Region:** `us-east-1`

---

## 🧠 What is a Key Pair?

A key pair is used to securely connect to EC2 instances.

* Public key → Stored in AWS
* Private key → Downloaded (`.pem` file)

---

## 🚀 Steps

1. Login to AWS Console
2. Select region → **us-east-1**
3. Go to **EC2 Dashboard**
4. Click **Key Pairs → Create Key Pair**
5. Enter:

   * Name: `datacenter-kp`
   * Type: `RSA`
6. Click **Create** and download the `.pem` file

---

## ⚠️ Important

* Use **us-east-1 region only**
* Name must be exactly **datacenter-kp**
* Select **RSA**, not ED25519

---

## ❌ Common Mistakes

* Wrong region
* Incorrect key name
* Wrong key type

---

## 🧩 Summary

```bash
Create an RSA key pair named datacenter-kp in us-east-1 using EC2
```

---

## ✅ Outcome

Key pair successfully created and ready for EC2 usage 🚀

---
