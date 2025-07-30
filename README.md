# Cloud Governance Gone Rogue – Azure Policy Lab

## name: Maryam Khalaf

##  Overview
This lab demonstrates how to enforce governance, security, and compliance in Azure using **Azure Policy**.  

Scenario: MapleTech Solutions developers were deploying resources globally, skipping tags, and exposing public IPs.  
As the Cloud Security Engineer, I created and assigned **custom Azure Policies** to enforce organizational guardrails.

---

##  Objectives
✔ Create **3 custom policies**:
1. Restrict resources to **Canada Central**  
2. Require **ProjectName** tag  
3. Deny creation of **Public IP addresses**  

✔ Group policies into a **Policy Initiative**  
✔ Assign the initiative to a **resource group**  
✔ Test enforcement with sample deployments

##  Folder Structure
policy-lab/
 ├─ policy-definitions/   # JSON files for 3 policies
 ├─ screenshots/          # Test result screenshots
 └─ README.md

---

##  Test Results
| Test | Resource | Result |
|------|-----------|---------|
| Deploy in East US | Storage Account | ❌ Denied |
| Missing ProjectName tag | Storage Account | ❌ Denied |
| Create Public IP | Public IP Resource | ❌ Denied |
| Canada Central with tag | Storage Account | ✅ Allowed |

---
## Screenshots

All screenshots of success and failure cases are inside the `screenshots/` folder.

---

##  Video Demo

---

##  Lessons Learned
- Azure Policy **enforces compliance before resource creation**.
- Policy initiatives simplify governance by grouping multiple rules.
- College tenant restrictions prevented VM creation, so **Storage Accounts were used for testing**.
