**Drawbacks of Traditional Push**

**kubectl scale deployment my-app --replicas=0**

- git push -> CI/CD -> Cluster: This causes config drift, poor auditability , difficult rollbacks, inconsistent deployments

---

**GitOps**

![Gitops Workflow](images/gitops1.png)


**Principles**


![Gitops Workflow](images/gitops2.png)

---


**ArgoCD Architecture**


- Understanding the role of API Server, Repository Server and Application Controller


![Gitops Workflow](images/architecture.png)



---






---

**argocd auto sync**

- **selfHeal:true** - This ensures whenever someone makes changes to live cluster like scaling the deployment to 6 replicas where as the kubernetes manifests still has 2. This option brings back the pods to 2.

```yaml
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
```
---

**PROJECTS**

- Manage and segregate multiple ArgoCD applications at scale.



---

**Propogration Policies**




---

**Sync Waves**


![Gitops Workflow](images/gitops3.png)



---


