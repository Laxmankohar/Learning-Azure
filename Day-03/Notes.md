# Azure Core Architecture & Building Blocks

> These are the fundamental building blocks you’ll always use in Azure.  
> Knowing them well helps in both **real projects** and **interviews**.

---

## 🔹 Azure Subscription

- A **subscription** is like a billing container for all your Azure resources.  
- Every resource you create (VM, Storage, DB) is tied to a subscription.  

***👉 Industry Example:***  
> A company may use:  
> - One subscription for **Production**  
> - One for **Development/Testing**  
> - One for **Sandbox/POC**  

***👉 Key Point:***  
> Subscription = Billing + Resource boundary.  

***👉 Interview Answer:***  
> “A subscription is a logical container that holds resources in Azure. It defines billing, access, and resource limits.”  

---

## 🔹 Azure Resource

- The smallest manageable item in Azure.  
- Examples: Virtual Machine, Storage Account, App Service, Database.  

***👉 Industry Example:***  
> A request: “Create a Linux VM with 2vCPU, 8GB RAM in Central India region.”  
> → That VM is a **resource**.  

***👉 Key Point:***  
> Resource = Any service instance you create in Azure.  

***👉 Interview Answer:***  
> “In Azure, a resource is any service instance like VM, storage, or DB that you create and manage.”  

---

## 🔹 Azure Resource Group (RG)

- A **logical container** to group related resources.  
- Helps manage, monitor, and delete resources together.  

***👉 Industry Example:***  
> A project team creates a **Resource Group = `EcomApp-RG`**.  
> Inside it → VM, Storage, Database, App Service, Networking.  
> When project ends, deleting the RG removes everything inside.  

***👉 Key Point:***  
> RG = Logical container. Easy management, common lifecycle.  

***👉 Interview Answer:***  
> “A Resource Group is a container to hold related resources like VMs, DBs, and networking. It helps manage them together.”  

---

## 🔹 Azure Resource Manager (ARM)

- The **management layer** in Azure.  
- It handles all requests (Portal, CLI, PowerShell, SDK, REST API).  
- Uses **templates (ARM templates / Bicep)** for infrastructure-as-code.  

***👉 Industry Example:***  
> Infra team deploys a full environment (VM + DB + Storage) using an **ARM Template** instead of creating each manually.  

***👉 Key Point:***  
> ARM = Brain of Azure resource deployment & management.  

***👉 Interview Answer:***  
> “Azure Resource Manager is the control plane of Azure. It receives deployment requests via Portal, CLI, or API, and ensures resources are provisioned consistently.”  

---

## 🔹 Management Groups

- Used to organize **multiple subscriptions** under one hierarchy.  
- Apply governance (policies, RBAC) at a higher level.  

***👉 Industry Example:***  
> A multinational has:  
> - Subscriptions for **Finance**, **HR**, **IT**.  
> - All grouped under **Corporate Management Group** with global policies.  

***👉 Key Point:***  
> Management Groups = Governance across subscriptions.  

***👉 Interview Answer:***  
> “Management Groups allow you to apply policies and RBAC across multiple subscriptions in a hierarchy.”  

---

## 🔹 Tags

- Key-value pairs attached to resources for metadata.  
- Example: `Owner=DevTeam`, `Environment=Prod`.  

***👉 Industry Example:***  
> Billing team filters Azure bill by tags → knows exactly how much **Dev vs Prod** resources cost.  

***👉 Key Point:***  
> Tags = Metadata for cost mgmt, ownership, environment.  

***👉 Interview Answer:***  
> “Tags are key-value pairs used to organize resources by owner, cost, or environment. They help in billing and management.”  

---

## 🔹 Day 3 Interview Quick Questions

1. **What is the difference between a Subscription and a Resource Group?**  
   - Subscription = Billing container.  
   - RG = Logical container for resources.  

2. **How does Azure Resource Manager work?**  
   - It’s the management layer that handles all API calls and ensures consistent deployments.  

3. **If you want to delete all resources of a project at once, how would you do it?**  
   - Delete the Resource Group.  

4. **How do companies manage governance across multiple subscriptions?**  
   - By using Management Groups with Azure Policies and RBAC.  

5. **Why do we use tags in Azure?**  
   - For cost tracking, ownership, and organizing resources.  

---

## 🔹 Notes / Best Practices

- Always tag resources (Owner, Environment, CostCenter).  
- One RG per project or application lifecycle.  
- Don’t put Prod + Dev in the same RG.  
- Use Management Groups for enterprises with multiple subscriptions.  
- Use ARM/Bicep templates for consistent deployments.  

---
