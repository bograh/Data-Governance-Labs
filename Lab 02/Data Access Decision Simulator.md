# **Data Access Decision Simulator**

**Role:** DevOps Engineer
**Organization:** EduConnect Ghana
**Regulatory Framework:** Ghana Data Protection Act

---

## **Data Access Decision Form – Request 1**

### **Request 1: Marketing Campaign**

**Requester:** Sarah Owusu, Marketing Manager

### **Decision**

**DENY (with alternative recommendation)**

### **Lifecycle Stage**

**Use / Share**

### **Justification**

* The request includes **CONFIDENTIAL data** (student email addresses).
* Sarah has **INTERNAL access only**, which does not permit handling CONFIDENTIAL data.
* Request violates the **principle of least privilege**—marketing does not require full student PII to run campaigns.
* Bulk access to PII increases risk of data leakage and non-compliance.

### **Action Steps**

1. Deny access to the full student database.
2. Propose an **alternative solution**:

   * Use an **opt-in mailing list** or
   * Provide **anonymized or consent-based contact data** extracted by Engineering.
3. Require confirmation that students have explicitly consented to marketing communications.
4. Log the decision for audit purposes.

---

## **Data Access Decision Form – Request 2**

### **Request 2: Analytics Partnership**

**Requester:** David Mensah, Head of Product
**Third Party:** DataInsights Inc.

### **Decision**

**CONDITIONALLY APPROVE**

### **Lifecycle Stage**

**Share**

### **Justification**

* Request involves **cross-border data transfer** and **CONFIDENTIAL data** (student profiles).
* Sharing raw database access and credentials is a **major security and compliance violation**.
* Ghana DPA requires safeguards for international data transfers and third-party processing.
* Least privilege is violated by granting full AWS database access.

### **Action Steps**

1. **Do NOT share database credentials.**
2. Limit shared data to **anonymized or pseudonymized datasets** only.
3. Ensure the following are in place before approval:

   * Data Processing Agreement (DPA)
   * Cross-border data transfer safeguards
   * Purpose limitation and retention terms
4. Grant access via:

   * Read-only API or
   * Secure data export bucket with logging enabled
5. Obtain sign-off from:

   * Legal
   * Security
   * Data Protection Officer (if designated)

---

## **Data Access Decision Form – Request 3**

### **Request 3: Archive & Deletion**

**Requester:** Comfort Asante, Customer Support Lead
**Student:** James Boateng

### **Decision**

**APPROVE**

### **Lifecycle Stage**

**Destroy (with limited Archive)**

### **Justification**

* Student has exercised the **“right to be forgotten”** under Ghana DPA.
* Account is inactive, and there are **no legal or financial obligations** preventing deletion.
* Organization is required to delete personal data when it is no longer necessary for its original purpose.

### **Action Steps**

1. Verify the requester’s identity and confirm deletion request.
2. Trigger account deletion workflow:

   * Remove PII (name, email, phone, profiles)
   * Delete learning activity linked to identity
3. Retain **minimal non-identifiable records** only if required:

   * Financial transaction summaries (for statutory audit)
   * Fully anonymized analytics data
4. Document the deletion request and completion.
5. Notify the student once deletion is finalized.

---

## **Final Summary**

All three data access requests were evaluated using **data classification policy**, **data lifecycle principles**, **least privilege**, and **regulatory compliance**. The decisions protect student data, reduce organizational risk, and align EduConnect Ghana with best practices in DevOps and data governance.