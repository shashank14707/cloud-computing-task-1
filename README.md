# 🪣 Task 1: Create a Cloud Storage Bucket and Upload Files

## 🎯 Objective
Understand the concept of **cloud object storage**, including bucket creation, file uploading, and file accessibility through cloud URLs.

---

## 🧰 Tools
- **Google Cloud Storage (Free Tier)**  
  or  
- **AWS S3 (Free Tier)**

---

## 📘 Step-by-Step Guide (Google Cloud Storage)

### 1. Create a Google Cloud Account
- Visit [https://cloud.google.com/](https://cloud.google.com/)
- Sign in with your Google account.
- Activate the **Free Tier** (you get $300 in free credits).

### 2. Open Cloud Storage
- Go to [Google Cloud Console → Storage](https://console.cloud.google.com/storage)

### 3. Create a Bucket
- Click **"Create bucket"**
- Enter a **unique bucket name**, e.g., `my-sample-bucket-shashankv`
- Select a **region** (e.g., `us-east1`)
- Leave all default settings
- Click **"Create"**

### 4. Upload a File
- Open your new bucket.
- Click **"Upload files"**.
- Choose a small file like `hello.txt` or `sample-image.jpg`.

### 5. (Optional) Make the File Public
- Click on your uploaded file.
- Go to the **Permissions** tab.
- Click **"Grant Access" → Add "allUsers"**.
- Under **Role**, choose **Storage Object Viewer**.
- Save changes.

### 6. Copy and Test File URL
- Copy the **Public URL**, e.g.  
  `https://storage.googleapis.com/my-sample-bucket-shashankv/hello.txt`
- Open it in your browser to verify access.

### 7. Take a Screenshot
- Capture the screen showing:
  - Bucket name
  - Uploaded file
  - Upload success message or file list view

---

## ☁️ Alternative: AWS S3

### 1. Sign Up for AWS
- Visit [https://aws.amazon.com/free/](https://aws.amazon.com/free/)
- Log in to the **AWS Management Console**

### 2. Create an S3 Bucket
- Navigate to **S3 → Create bucket**
- Enter a unique name (e.g., `my-s3-bucket-shashankv`)
- Select a region (e.g., `us-east-1`)
- Leave defaults and click **"Create bucket"**

### 3. Upload a File
- Open your bucket.
- Click **"Upload" → Add files → Upload**.

### 4. (Optional) Make the File Public
- In **Permissions**, enable **Public Read Access**.

### 5. Get and Test File URL
- Copy the **Object URL** and open it in your browser.

### 6. Screenshot
- Take a screenshot showing the file successfully uploaded.

---

## ✅ Deliverables
- **Screenshot** of successful file upload (GCS or AWS S3)
- **Public file URL** (if applicable)

---

## 🧠 Outcome
By completing this task, you will:
- Understand the **concept of cloud object storage**.
- Learn how to **create and configure storage buckets**.
- Be able to **upload and access files** in the cloud.
- Know how **permissions** affect public/private access.

---
