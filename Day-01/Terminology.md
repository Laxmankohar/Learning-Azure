# 📍 Azure Terminology

## 🔹 Region

- Physical location (like East US, West Europe).

- Contains multiple datacenters.

***👉 Industry Example:***
> If your customers are in India, you pick “Central India” region to reduce latency.

***👉 Key Point:***
> Choose closest region to users for performance.

***👉 Interview Q:“What is a region in Azure?”***
> 👉 Answer: “A region is a geographical area with multiple datacenters. Example: East US or Central India.”

---

## 🔹 Availability Zone (AZ)

- Each region has 2–3 zones (separate datacenters).

- If one zone fails, others keep service running.

***👉 Industry Example:***
> E-commerce app backend spread across Zone 1, Zone 2, Zone 3 → one zone outage doesn’t kill the site.

***👉 Key Point:***
> Used for high availability.

***👉 Interview Answer:***
> “Availability Zones are physically separate datacenters within a region. They ensure redundancy. Example: deploying VMs across Zone 1 and Zone 2 in East US.”
---

## 🔹 High Availability (HA)

- Designing systems to stay online even if part fails.

- Achieved via load balancing + zones.

***👉 Industry Example:***
> Banking app must be up 24/7. Deploy 2 VMs in different AZs behind a load balancer.

***👉 Key Point:***
> HA = minimize downtime.

***👉 Interview Answer:***
> “High Availability means designing infra so if one component fails, another takes over. Example: Web servers across AZs behind Azure Load Balancer.”

---

## 🔹 Fault Tolerance

- Ability to continue without service interruption even if failures happen.

- More advanced than HA.

***👉 Industry Example:***
> Critical healthcare system: if one datacenter burns down, system automatically runs from another.

***👉 Key Point:***
> HA = less downtime; Fault Tolerance = zero downtime.

***👉 Interview Answer:***
> “Fault tolerance is the ability of a system to operate fully even after component failures. Example: geo-replication across regions.”
---

## 🔹 Scalability

- System can grow as demand grows.

- Vertical (bigger VM) or Horizontal (more VMs).

***👉 Industry Example:***
> Ticket booking site during IPL finals → scale out more VMs automatically.

***👉 Key Point:***
> Pay only when load increases.

***👉 Interview Answer:***
> Scalability is the ability to increase capacity on demand. Example: Azure Scale Sets automatically adding VMs during peak load.”

---

## 🔹 Elasticity

- Auto-adjust resources up or down based on demand.

***👉 Industry Example:***
> Food delivery app: spikes at lunch/dinner → extra VMs added, removed later.

***👉 Key Point:***
> Elasticity = Scalability + Auto.

***👉 Interview Answer:***
> “Elasticity means automatically adjusting resources based on workload. Example: Azure App Service Plan scaling web apps during high traffic.”


---

## 🔹 Virtualization

- Technology to create virtual versions of hardware so multiple OS instances can run on one physical server.

***👉 Industry Example:***  
> One physical server at a company hosts 10 VMs for dev, QA, and prod teams.

***👉 Key Point:***  
> Virtualization = Abstraction of hardware. VM = virtual computer.

***👉 Interview Answer:***  
> “Virtualization allows multiple virtual machines to run on a single physical server. Each VM acts like an independent computer with its own OS and resources.”

---

## 🔹 Disaster Recovery (DR)

- Plan + setup to recover apps/data after a major failure.

***👉 Industry Example:***  
> A hospital replicates its patient database to a secondary Azure region. In case the primary region fails, they failover within minutes.

***👉 Key Point:***  
> DR = Backup + Replication + Failover (planned & tested).  
> Measured with RTO (time to recover) and RPO (data loss tolerance).

***👉 Interview Answer:***  
> “Disaster Recovery ensures business continuity by recovering apps and data after outages. Example: Azure Site Recovery replicates workloads to a secondary region and enables failover.”