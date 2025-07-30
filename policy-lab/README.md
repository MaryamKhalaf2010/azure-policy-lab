# Cloud Governance Gone Rogue – Azure Policy Lab

## name: Maryam Khalaf

## 📌 Summary
This lab enforces governance in Azure using custom policies.  
We created 3 custom policies and grouped them into an initiative:

✅ Restrict resources to **Canada Central**  
✅ Require **ProjectName tag**  
✅ Deny creation of **Public IP addresses**  

---

## 📂 Folder Structure
policy-lab/
 ├─ policy-definitions/   # JSON files for 3 policies
 ├─ screenshots/          # Test result screenshots
 └─ README.md

---

## 📊 Test Results
| Test | Resource | Result |
|------|-----------|---------|
| Deploy in East US | Storage Account | ❌ Denied |
| Missing ProjectName tag | Storage Account | ❌ Denied |
| Create Public IP | Public IP Resource | ❌ Denied |
| Canada Central with tag | Storage Account | ✅ Allowed |

---

## 🎥 Video Demo
[👉 Video Link](PUT-YOUR-VIDEO-LINK-HERE)

---

## 📝 Lessons Learned
- Azure Policy **enforces compliance before resource creation**.
- Policy initiatives simplify governance by grouping multiple rules.
- College tenant restrictions prevented VM creation, so **Storage Accounts were used for testing**.
