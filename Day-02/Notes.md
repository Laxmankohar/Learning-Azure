# Cloud Service Models (IaaS vs PaaS vs SaaS)

## 🔹 What are Service Models?
Cloud services are mainly divided into 3 models in Azure:  
- **IaaS (Infrastructure as a Service)**  
- **PaaS (Platform as a Service)**  
- **SaaS (Software as a Service)**  

They differ in how much responsibility is on **you (the customer)** vs **Azure (the provider)**.

---

## 🔹 IaaS (Infrastructure as a Service)

- You rent **infrastructure** (servers, storage, networking) from Azure.  
- You manage OS, applications, and configurations.  
- Azure manages hardware and datacenters.

***👉 Characteristics:***  
- Full control over VMs.  
- Flexible but more responsibility.  
- Good for lift-and-shift migrations.  

***👉 Industry Example:***  
> A company migrates its on-premise app to Azure VMs (IaaS) without rewriting code.  

***👉 Key Point:***  
> IaaS = “You control most things, Azure gives hardware.”  

---

## 🔹 PaaS (Platform as a Service)

- Azure provides **platform** (runtime, OS, middleware).  
- You only focus on **apps and data**.  
- No need to worry about patching OS or scaling infrastructure.

***👉 Characteristics:***  
- Developer-focused.  
- Auto-scaling, built-in availability.  
- Faster development lifecycle.  

***👉 Industry Example:***  
> A startup builds a web app using **Azure App Service** and SQL Database (no need to manage VMs).  

***👉 Key Point:***  
> PaaS = “You focus on code, Azure manages platform.”  

---

## 🔹 SaaS (Software as a Service)

- Complete **software/application** delivered over the internet.  
- You just **use** it; everything is managed by Azure/provider.  
- No management of infrastructure or app.  

***👉 Characteristics:***  
- Ready-to-use applications.  
- Subscription-based (pay monthly/yearly).  
- Accessible via browser/app.  

***👉 Industry Example:***  
> Office 365, Outlook.com, Dynamics 365.  

***👉 Key Point:***  
> SaaS = “End product, ready to use.”  

---

## 🔹 Visual Responsibility Model

| Layer              | IaaS (You Manage) | PaaS (You Manage) | SaaS (You Manage) |
|--------------------|------------------|------------------|------------------|
| Application        | ✅               | ✅               | ❌               |
| Data               | ✅               | ✅               | ❌               |
| Runtime            | ✅               | ❌               | ❌               |
| Middleware         | ✅               | ❌               | ❌               |
| OS                 | ✅               | ❌               | ❌               |
| Virtualization     | ❌               | ❌               | ❌               |
| Servers/Storage/Network | ❌         | ❌               | ❌               |

✅ = You manage  
❌ = Azure manages  

---

## 🔹 How to Decide?

- Choose **IaaS** if → You want control, need VMs, or migrating legacy apps.  
- Choose **PaaS** if → You want to build/deploy apps quickly without managing infra.  
- Choose **SaaS** if → You just need to use the software, not build it.  

---
