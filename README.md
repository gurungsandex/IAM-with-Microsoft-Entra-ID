
# Identity and Access Management (IAM) with Microsoft Entra ID – Hands-On Lab Guide

> A practical, beginner-friendly guide to learning Identity and Access Management (IAM) using Microsoft Entra ID (Azure AD)

---

# Table of Contents

1. What is Identity and Access Management (IAM)?
2. Why IAM Is Important
3. Understanding Zero Trust (Microsoft Entra ID)
4. Core IAM Pillars
5. Get a Free Trial Subscription 
6. Identity Lifecycle Management
7. Creating Users in Microsoft Entra ID
8. Role-Based Access Control (RBAC)
9. Creating Custom Roles
10. Enabling Authentication Methods (MFA)
11. License Assignment (User & Group)
12. Self-Service Password Reset (SSPR)
13. Smart Lockout Protection
14. Creating and Managing Security Groups
15. Managing External Collaboration (Guest Users)
16. Adding Enterprise Applications
17. Conditional Access Policies
18. Managing Sign-in Risk & User Risk Policies

---

# What is Identity and Access Management (IAM)?

**Identity and Access Management (IAM)** is the process of controlling:

* Who can access a system
* What they can access
* When they can access it
* Why are they allowed access

In simple words:

> IAM makes sure the **right person** gets access to the **right resource**, at the **right time**, for the **right reason**.

### Definitions

* **Identity** → A digital representation of a user, device, or application.
* **Authentication** → Proving who you are.
* **Authorization** → What you are allowed to do.
* **Least Privilege** → Give users only the permissions they need — nothing more.

---

# Why IAM Is Important

Today, most cyberattacks target **identities**, not systems.

If an attacker steals credentials and there are no strong access controls:

* They can move inside the system freely.
* They can escalate privileges.
* They can access sensitive data.

IAM helps organizations:

- Prevent unauthorized access
- Reduce over-permissioned accounts
- Enforce Multi-Factor Authentication (MFA)
- Track user activity using logs
- Meet compliance requirements

Without IAM, security becomes **reactive** instead of **proactive**.

---

# Zero Trust in Microsoft Entra ID

**Zero Trust** is a security model based on one rule:

> “Never trust. Always verify.”

There is no automatic trust — even if the user is inside the organization.

Every access request is verified based on:

* User identity
* Device health
* Location
* Risk signals
* Application sensitivity

### How Microsoft Entra ID Implements Zero Trust

* Conditional Access Policies
* Multi-Factor Authentication (MFA)
* Privileged Identity Management (PIM)
* Risk-based policies

---

# Core IAM Pillars

| Pillar         | What It Does       | Key Tools                     |
| -------------- | ------------------ | ----------------------------- |
| Authentication | Verifies identity  | MFA, Passwordless, FIDO2      |
| Authorization  | Grants permissions | RBAC, Conditional Access, PIM |
| Auditing       | Tracks activity    | Sign-in Logs, Audit Logs      |

---

# Getting a Free Trial Subscription

The best way to learn IAM is not just reading — it's practicing.

I subscribed to:

> **Microsoft Entra ID P2 – 30 Day Trial**

With this trial, you also get access to:

* Microsoft Entra ID
* Azure
* Microsoft 365
* Intune
* Microsoft Defender

<img width="1699" height="934" alt="sc1" src="https://github.com/user-attachments/assets/5c258cba-9741-401e-994a-d9e13a7449f2" />

---

# Identity Lifecycle Management

Identity management means managing users from:

* Joiner (New employee)
* Mover (Role change)
* Leaver (Employee exit)


Deleted users remain recoverable for **30 days**.

After 30 days → permanently deleted.

⚠ You cannot restore permanently deleted users.

---

# Creating a User in Microsoft Entra ID

Let’s do this step-by-step.

### Step 1: Login

Go to:

```
https://entra.microsoft.com
```

### Step 2: Navigate to Users

* Click **Users**
* Click **+ New user**
* Select **Create new user**

---

<img width="1696" height="743" alt="sc2" src="https://github.com/user-attachments/assets/237dda2e-7778-45b0-9d36-b9995ef4cdfd" />


---

### Step 3: Enter User Details

Fill in:

* Name
* Username
* Password

Password requirements:

* Minimum 8 characters
* Uppercase
* Lowercase
* Number
* Symbol

This ensures strong password security.

---

<img width="1026" height="728" alt="sc3" src="https://github.com/user-attachments/assets/b6df1406-484f-4e21-9bc3-005ea11d3d8c" />


---

### Step 4: Assign Directory Roles

Go to **Assignments tab**

Assign only necessary roles.

This enforces:

> Principle of Least Privilege

Example:

* Global Reader
* Compliance Administrator
* User Administrator

---

<img width="1689" height="683" alt="sc4" src="https://github.com/user-attachments/assets/4e3f65d5-d6b5-450d-b07b-d9e82ecd06eb" />


---

### Step 5: Review and Create

Click **Review + Create**

User is now created 🎉

<img width="1411" height="457" alt="sc6" src="https://github.com/user-attachments/assets/74df85af-42fe-494b-a562-cae76e6564ab" />

---

# Role-Based Access Control (RBAC)

**RBAC (Role-Based Access Control)** means:

1. Define roles
2. Assign permissions to roles
3. Assign roles to users

Important:

> ❌ Do NOT create roles based only on job titles
> ✅ Create roles based on required permissions

---

## Example: Compliance Administrator

### Steps:

1. Go to **Roles & Admins**
2. Select **Compliance Administrator**
3. Click **Add Assignments**
4. Add user
5. Choose:
   * Active
   * Eligible (via PIM)
6. Assign

---

<img width="812" height="683" alt="Screenshot 2026-02-28 at 2 29 13 PM" src="https://github.com/user-attachments/assets/bf5b6498-1fc0-4184-a0be-e8edfd056c86" />

<img width="677" height="521" alt="Screenshot 2026-02-28 at 2 30 13 PM" src="https://github.com/user-attachments/assets/92737b57-2ec7-4c8a-a310-8801020094e6" />

---

# Creating a Custom Role

If built-in roles don’t meet your needs:

Create a custom role.

### What is a Custom Role?

A custom role is a tailored set of permissions such as:

* microsoft.directory/users/create
* microsoft.directory/applications/update

---

### Steps:

1. Go to **Roles & Admins**
2. Click **+ New Custom Role**
3. Enter:

   * Name
   * Description
4. Add required permissions
5. Review and Create

---

<img width="1226" height="514" alt="Screenshot 2026-02-28 at 2 32 07 PM" src="https://github.com/user-attachments/assets/4a7c69e5-d688-4709-b83d-b5cc93ac786c" />


---

You can assign:

* Users
* Groups
* Scope

---

# 🔟 Enable Authentication Methods (MFA)

MFA is critical in Zero Trust.

It ensures that even if a password is stolen:

> The attacker still cannot log in.

---

### Steps to Enable MFA:

1. Go to **Authentication Methods**
2. Select policy
3. Enable method (e.g., Microsoft Authenticator)

---

📸 **[Screenshot Placeholder – Authentication Methods Policy]**

---

When a user logs in first time:

* They are forced to register MFA
* Install Authenticator App
* Scan QR Code
* Enter verification code

User cannot access system until registration is complete.

---

📸 **[Screenshot Placeholder – MFA Registration Screen]**

---

# 1️⃣1️⃣ License Assignment

Licenses unlock features.

Without a license:

* No advanced security features
* No P2 features like Risk Policies

---

## Assign License to a User

Go to:

```
https://admin.cloud.microsoft/
```

1. Go to Billing
2. Select Licenses
3. Choose license
4. Assign License
5. Add user
6. Save

---

📸 **[Screenshot Placeholder – License Assignment]**

---

## Assign License to Group (Recommended for Large Organizations)

Benefits:

* Automatic assignment
* Scalable
* Easier management

If user leaves group → license automatically removed.

---

📸 **[Screenshot Placeholder – Group License Assignment]**

---

# 1️⃣2️⃣ Self-Service Password Reset (SSPR)

SSPR allows users to reset passwords without IT help.

Admins must use two authentication methods.

---

### Enable SSPR

1. Go to **Password Reset**
2. Select **Selected**
3. Choose group
4. Save

---

📸 **[Screenshot Placeholder – SSPR Settings]**

---

### User Side Reset Process

1. Click **Forgot my password**
2. Complete verification
3. Create new password

---

📸 **[Screenshot Placeholder – Password Reset Page]**

---

# 1️⃣3️⃣ Smart Lockout

Smart Lockout protects against brute-force attacks.

It uses:

* Lockout Threshold (default: 10 attempts)
* Lockout Duration (default: 60 seconds)

It distinguishes between:

* Real user mistakes
* Attack attempts

---

### Configure Smart Lockout

1. Go to Authentication Methods
2. Password Protection
3. Set threshold & duration

---

📸 **[Screenshot Placeholder – Smart Lockout Settings]**

---

# 1️⃣4️⃣ Creating Security Groups

Security groups manage access to:

* Applications
* Licenses
* Resources

---

## Group Types

| Type           | Description                     |
| -------------- | ------------------------------- |
| Assigned       | Manually add members            |
| Dynamic User   | Auto-add users based on rules   |
| Dynamic Device | Auto-add devices based on rules |

---

### Steps:

1. Go to **Groups**
2. Click **New Group**
3. Select type
4. Add owners
5. Add members
6. Create

---

📸 **[Screenshot Placeholder – Create Security Group]**

---

# 1️⃣5️⃣ Managing External Collaboration (Guest Users)

External Users (Guest Users):

* Partners
* Vendors
* Consultants

They use their own identity (Google, company email, etc.)

This ensures:

* Identity sovereignty
* Secure collaboration
* Zero Trust enforcement

---

## Invite External User

1. Go to Users
2. Click **+ New user**
3. Select **Invite external user**
4. Enter external email
5. Review and invite

---

📸 **[Screenshot Placeholder – Invite Guest User]**

---

Guest user must accept invitation.

They have no access until assigned.

---

# 1️⃣6️⃣ Add Enterprise Applications

### Steps:

1. Go to **Enterprise Applications**
2. Click **+ New Application**
3. Select app
4. Create

---

📸 **[Screenshot Placeholder – Add Enterprise App]**

---

## Assign App to Guest User

1. Select App
2. Assign users & groups
3. Add user
4. Save

---

📸 **[Screenshot Placeholder – Assign App to User]**

---

# 1️⃣7️⃣ Conditional Access Policies

Conditional Access is the "if-then" engine.

Example:

* IF login from unknown country
* THEN require MFA

---

### Steps to Create Policy

1. Go to Conditional Access
2. Click New Policy
3. Add:

   * Users
   * Resources
   * Conditions
4. Grant controls:

   * Require MFA
   * Block
5. Enable policy
6. Create

---

📸 **[Screenshot Placeholder – Conditional Access Policy Creation]**

---

⚠ If replacing security defaults, disable them first.

---

# 1️⃣8️⃣ Sign-in Risk & User Risk Policies

## Sign-in Risk Policy

Focus: One login attempt
Response: Require MFA

## User Risk Policy

Focus: Account compromised
Response: Force password reset

---

### Configure:

1. Go to Conditional Access
2. New Policy
3. Conditions → User risk or Sign-in risk
4. Configure level
5. Grant control
6. Enable

---

📸 **[Screenshot Placeholder – Risk Policy Settings]**

---

# 🎯 Final Thoughts

This lab demonstrates core IAM concepts using Microsoft Entra ID:

✔ Identity lifecycle
✔ RBAC
✔ MFA
✔ Conditional Access
✔ Risk-based policies
✔ External collaboration
✔ Licensing

IAM is not just configuration — it is strategy.

Security is strongest when:

* Access is minimal
* Verification is constant
* Monitoring is continuous

---

If you'd like, I can now:

* ✅ Convert this into a **professional GitHub portfolio README**
* ✅ Create a **LinkedIn-ready IAM project post**
* ✅ Add architecture diagrams (text-based)
* ✅ Create a SOC / Security Engineer resume project description**
* ✅ Improve it to senior-level documentation standard**

Tell me what you want next 👇


