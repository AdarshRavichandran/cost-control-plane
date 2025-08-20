
#Cost-Aware Control Plane (CACP)

A lightweight, cloud‑native control plane that provides real‑time cost visibility and policy enforcement (budgets/quotas) for Kubernetes workloads. Designed for MVP-first delivery and clear GitHub showcase value.

1) Vision & Scope

Goal: Prevent surprise cloud bills by:

Estimating cost before deploy (shift-left, PR checks + admission policy).

Measuring live cost using metrics.

Enforcing budgets/policies at deploy-time.

Initial scope (MVP):

Kubernetes on AWS EKS (region: ap-south-1 as default).

Compute cost from CPU/memory requests mapped to node types in the cluster.

Storage cost from PVCs (gp3 volumes).

Network: basic egress estimate (per-GB), ingress via LoadBalancer count.

Namespace budgets: block/deny deploys exceeding budget.

Out-of-scope (for MVP, future-ready):

Multi-cloud adapters (GCP/Azure) → planned.

Spot instances, Savings Plans nuances → planned.

Managed services (RDS, S3, MSK) → planned via external resource descriptors.e
