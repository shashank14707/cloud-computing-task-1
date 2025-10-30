# ☁ Task 7: Configure Load Balancing and Auto Scaling for a Web Application

## 🎯 Objective

To understand **scalability** and **fault tolerance** in cloud computing by setting up a **Load Balancer** and **Auto Scaling group** for a simple web application running on multiple virtual machines.

This task demonstrates how cloud systems ensure **high availability**, **traffic management**, and **cost-efficient scaling** automatically.

---

## 🛠 Tools (Free & Beginner-Friendly)

Choose **any one** platform:

- **AWS (Free Tier)** – EC2 + Elastic Load Balancer + Auto Scaling  
- **Google Cloud Platform (GCP)** – Compute Engine + Load Balancer + Instance Group  
- **Microsoft Azure** – Virtual Machine Scale Sets + Load Balancer  

### Local Tools:
- Web browser  
- VS Code or any code editor  
- Terminal / Cloud Shell  

---

## 📦 Deliverables

Submit the following screenshots:
1. Load Balancer dashboard showing backend instances  
2. Auto Scaling configuration page  
3. Public load balancer URL (showing your running web app)  

### Short Note (4–5 lines)
Explain how your setup works and what happens during auto scaling.

---

## 🧭 Mini Guide (Step-by-Step)

### **1️⃣ Create a Basic Web App Template**

Create a simple HTML file named `index.html`:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Cloud Auto Scaling Demo</title>
</head>
<body>
  <h2>Hello from my Cloud Instance!</h2>
  <p>This page is served from a cloud VM behind a load balancer.</p>
</body>
</html>
```

You can upload this file to multiple VMs or use a startup script to deploy it automatically using **nginx** or **apache**.

---

### **2️⃣ Launch Multiple VM Instances**

1. Go to your cloud console (e.g., AWS EC2 → Launch Instances).  
2. Create **2 or more small VMs (t2.micro / e2-micro)**.  
3. Install a web server:

```bash
sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2
```

4. Copy your HTML file to the web directory:

```bash
sudo cp index.html /var/www/html/
```

---

### **3️⃣ Set Up a Load Balancer**

1. Create a **Load Balancer** (HTTP type).  
2. Add your VM instances as **backend servers**.  
3. Configure **health checks** (HTTP on port 80).  
4. Obtain the **public URL/IP** of the load balancer.

✅ **Test:** Visit the load balancer URL — your webpage should load successfully.

---

### **4️⃣ Configure Auto Scaling**

1. Create an **Auto Scaling Group**:  
   - Choose your VM template (AMI or instance group)  
   - Define:
     - Minimum: `1`
     - Desired: `2`
     - Maximum: `4`  
   - Set scaling trigger: **CPU Utilization > 60%**

When traffic increases → new VMs are created.  
When traffic decreases → extra VMs are terminated (cost-efficient).

---

### **5️⃣ Test the Scaling**

Run a simple load test:

```bash
ab -n 500 -c 50 http://your-load-balancer-url/
```

Observe in your console — new instances should launch automatically.

---

### **6️⃣ Monitor and Clean Up**

- Monitor **metrics dashboard** (CPU, network, scaling history).  
- After testing, **delete all resources** to avoid charges.

---

## 🧠 Outcome

After completing this task, you will:

- Understand **load balancing** and **auto scaling** concepts  
- Learn how cloud maintains **availability** and **performance**  
- Get hands-on experience with **instance groups** and **health checks**  
- Gain knowledge of **scalable architecture design**

---

## 💬 Interview Questions

1️⃣ What is load balancing and why is it important in cloud systems?  
2️⃣ What is auto scaling and how does it improve cost efficiency?  
3️⃣ How does a load balancer decide which instance to send traffic to?  
4️⃣ What is a health check in load balancing, and how is it used?  
5️⃣ What are the main differences between horizontal and vertical scaling?  
6️⃣ What happens when one of your backend instances fails?  
7️⃣ Can auto scaling work with serverless functions or containers? How?  
8️⃣ How would you monitor and troubleshoot a scaling issue in production?
