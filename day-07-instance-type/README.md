---

# 🚀 Day 7 – Change EC2 Instance Type

## 📌 Task Overview

During the migration process, the Nautilus DevOps team identified an **underutilized EC2 instance**. To optimize resource usage and reduce cost, the instance type needs to be downgraded.

---

## 🎯 Objectives

1. Change the instance type from **t2.micro → t2.nano** for `xfusion-ec2`
2. Ensure the instance is in **Running state** after modification
3. Perform all actions in **us-east-1 region**
4. Ensure **Status Checks are completed** before making changes

---

## ⚙️ Prerequisites

* AWS Account access
* IAM permissions for EC2
* Instance `xfusion-ec2` already exists
* Region set to: **us-east-1**

---

## 🧭 Step-by-Step Implementation

### 1️⃣ Login to AWS Console

* Go to AWS Management Console
* Navigate to **EC2 Dashboard**
* Select region: **us-east-1**

---

### 2️⃣ Verify Instance Status

* Go to **Instances**
* Select `xfusion-ec2`
* Check:

  * Instance State → `Running`
  * Status Checks → `2/2 checks passed`

⚠️ If status is **Initializing**, wait until checks are complete.

---

### 3️⃣ Stop the Instance

> Instance type cannot be changed while running

* Select instance `xfusion-ec2`
* Click: **Instance State → Stop Instance**
* Wait until state becomes **Stopped**

---

### 4️⃣ Change Instance Type

* With instance selected:

  * Click **Actions → Instance Settings → Change Instance Type**
  * Select: `t2.nano`
  * Click **Apply**

---

### 5️⃣ Start the Instance

* Click: **Instance State → Start Instance**
* Wait until:

  * State = `Running`
  * Status Checks = `2/2 passed`

---

## ✅ Verification

* Instance Name: `xfusion-ec2`
* Instance Type: `t2.nano`
* Instance State: `Running`
* Status Checks: Passed

---

## 💡 Key Notes

* Always **stop the instance** before changing type
* Ensure **status checks are complete** before modification
* Smaller instance type = **cost optimization**
* Perform all operations in **correct region (us-east-1)**

---

## 🧠 Learning Outcome

* Understanding EC2 instance resizing
* Cost optimization using right-sized instances
* Importance of instance state & health checks

---

## 🏁 Conclusion

Successfully optimized the EC2 instance by:

* Downgrading from `t2.micro` to `t2.nano`
* Ensuring system stability post-change
* Maintaining proper AWS operational practices

---
