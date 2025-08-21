# Cost-Aware Control Plane (CACP)

A lightweight, cloud-native control plane that provides real-time cost visibility and policy enforcement (budgets/quotas) for Kubernetes workloads. Designed for MVP-first delivery and clear GitHub showcase value.

---

## Vision & Scope

**Goal:** Prevent surprise cloud bills by:

- **Estimating cost before deploy** (shift-left: PR checks + admission policy).  
- **Measuring live cost** using metrics.  
- **Enforcing budgets/policies** at deploy time.  

---

### Initial Scope (MVP)

- **Platform:** Kubernetes on AWS EKS (`ap-south-1` default region).  
- **Compute:** Cost from CPU/memory requests mapped to node types in the cluster.  
- **Storage:** PVCs (gp3 volumes).  
- **Network:** Basic egress estimate (per-GB), ingress via LoadBalancer count.  
- **Budgets:** Namespace-level budgets; block/deny deploys exceeding limits.  

---

### Out of Scope (for MVP, future-ready)

- Multi-cloud adapters (**GCP/Azure**) → *planned*.  
- Spot instances, Savings Plans nuances → *planned*.  
- Managed services (RDS, S3, MSK) → *planned via external resource descriptors*.  
---

## High-Level Architecture

![CACP Architecture](docs/architecture.png)
