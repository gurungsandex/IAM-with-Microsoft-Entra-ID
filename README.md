
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

<img width="876" height="761" alt="Screenshot 2026-02-28 at 4 41 07 PM" src="https://github.com/user-attachments/assets/dcd3f5cb-7ffc-446b-90ac-e4a72d261eb6" />

---

You can assign:

* Users
* Groups
* Scope

<img width="880" height="374" alt="Screenshot 2026-02-28 at 4 41 45 PM" src="https://github.com/user-attachments/assets/9ef7a6d7-1c4b-4e0d-9d93-90da33fbc4b4" />

---

# Enable Authentication Methods (MFA)

MFA is critical in Zero Trust.

It ensures that even if a password is stolen:

> The attacker still cannot log in.

---

### Steps to Enable MFA:

1. Go to **Authentication Methods**
2. Select policy
3. Enable method (e.g., Microsoft Authenticator)

---

<img width="1692" height="901" alt="auth1" src="https://github.com/user-attachments/assets/85a8ae61-ea92-4362-b7fe-c8279d6f18cb" />



---

When a user logs in first time:

* They are forced to register MFA
* Install Authenticator App
* Scan QR Code
* Enter verification code

User cannot access system until registration is complete.

---

<img width="932" height="624" alt="Screenshot 2026-02-28 at 4 47 38 PM" src="https://github.com/user-attachments/assets/8bf70e99-9efa-440a-b024-d018af1cdba1" />

<img width="753" height="731" alt="Screenshot 2026-02-28 at 4 48 29 PM" src="https://github.com/user-attachments/assets/20599964-7245-4092-aaef-85aa4e5f6d70" />

<img width="829" height="724" alt="Screenshot 2026-02-28 at 4 48 52 PM" src="https://github.com/user-attachments/assets/471b72ec-e219-4f19-acb0-f63d5f4135d3" />

<img width="919" height="626" alt="Screenshot 2026-02-28 at 4 49 16 PM" src="https://github.com/user-attachments/assets/4ee42e37-d20b-4ed8-8c4a-05c06e0ccf22" />

<img width="779" height="642" alt="Screenshot 2026-02-28 at 4 49 56 PM" src="https://github.com/user-attachments/assets/237d6357-aa15-475e-941f-e000ca2eb636" />

---

# License Assignment

Licenses unlock advanced security features.

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
5. Add Users
6. Assign Lincenses 

---

<img width="1224" height="480" alt="sc10" src="https://github.com/user-attachments/assets/5e44a3e3-ab47-4162-993d-0e43f36ab956" />

---

## Assign License to Group (Recommended for Large Organizations)

Benefits:

* Automatic assignment
* Scalable
* Easier management

If user leaves group → license automatically removed.

---

<img width="1641" height="563" alt="sc11" src="https://github.com/user-attachments/assets/e6f34961-c6d6-4eab-9889-1c934457d905" />

---

# Self-Service Password Reset (SSPR)

SSPR allows users to reset passwords without IT help.

Admins must use two authentication methods.

<img width="675" height="391" alt="Screenshot 2026-02-28 at 4 57 14 PM" src="https://github.com/user-attachments/assets/4d7c9f0e-f47d-48d9-a49c-a8e6244a7e80" />

---

### Enable SSPR

1. Go to **Password Reset**
2. Select **Selected**
3. Choose group
4. Save

---

<img width="675" height="391" alt="Screenshot 2026-02-28 at 4 57 14 PM" src="https://github.com/user-attachments/assets/48d470db-8176-49e5-ad9c-e561dca453c7" />

---

### User Side Reset Process

1. Click **Forgot my password**
2. Complete verification
3. Create new password

---

<img width="692" height="493" alt="Screenshot 2026-02-28 at 4 59 19 PM" src="https://github.com/user-attachments/assets/a013f69e-8a80-4bfe-9cad-db62652156e4" />

<img width="967" height="697" alt="Screenshot 2026-02-28 at 4 59 43 PM" src="https://github.com/user-attachments/assets/9c79e43a-3350-4a4b-9a0d-b251e2720176" />

<img width="955" height="551" alt="Screenshot 2026-02-28 at 5 00 06 PM" src="https://github.com/user-attachments/assets/0ecba729-cdae-4180-93f3-cdaee65bfe7f" />

<img width="933" height="552" alt="Screenshot 2026-02-28 at 5 00 27 PM" src="https://github.com/user-attachments/assets/66bdb13b-1363-4ed3-883f-d872f42bb170" />

<img width="588" height="318" alt="Screenshot 2026-02-28 at 5 00 52 PM" src="https://github.com/user-attachments/assets/cd43c38b-470e-4d74-aa98-24e6ac8328ac" />

---

# Smart Lockout

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

<img width="1279" height="724" alt="Screenshot 2026-02-28 at 5 01 52 PM" src="https://github.com/user-attachments/assets/cf4d2925-3f0f-4193-a3db-dcf69c695960" />

---

# Creating Security Groups

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

<img width="1282" height="612" alt="Screenshot 2026-02-28 at 5 02 53 PM" src="https://github.com/user-attachments/assets/d7a6ad3d-61b3-42cf-a1ea-fa61b2bd3311" />


---

# Managing External Collaboration (Guest Users)

External Users (Guest Users):

* Partners
* Vendors
* Consultants

They use their own identity (Google, company email, etc.)

This ensures:

* Identity sovereignty
* Secure collaboration
* Zero Trust enforcement

External collaboration settings

<img width="1275" height="809" alt="Screenshot 2026-02-28 at 5 04 20 PM" src="https://github.com/user-attachments/assets/81cc102a-c7e6-4f0b-ba7b-1a6a9d3a30ec" />

---

## Invite External User

1. Go to Users
2. Click **+ New user**
3. Select **Invite external user**
4. Enter external email
5. Review and invite

---

<img width="1283" height="537" alt="Screenshot 2026-02-28 at 5 03 46 PM" src="https://github.com/user-attachments/assets/1a04b8ba-6001-4d45-9a15-3d46ba580e63" />

<img width="1277" height="804" alt="Screenshot 2026-02-28 at 5 05 41 PM" src="https://github.com/user-attachments/assets/540bb6bb-7621-4af5-9e8b-84541b804abb" />

<img width="1278" height="771" alt="Screenshot 2026-02-28 at 5 06 20 PM" src="https://github.com/user-attachments/assets/ef7a309b-2de1-467d-a4de-0eb0a7904a25" />

---

Guest user must accept invitation. They have no access until assigned.

<img width="972" height="723" alt="Screenshot 2026-02-28 at 5 06 57 PM" src="https://github.com/user-attachments/assets/02248517-1c1b-4168-82a5-04ee9ce313f1" />

<img width="730" height="834" alt="Screenshot 2026-02-28 at 5 07 27 PM" src="https://github.com/user-attachments/assets/32dfeeab-7c16-4704-b8d1-68305671be02" />

<img width="1282" height="508" alt="Screenshot 2026-02-28 at 5 07 49 PM" src="https://github.com/user-attachments/assets/11fb6aca-217e-4605-a9a7-0b0645af424c" />

---

# Add Enterprise Applications

### Steps:

1. Go to **Enterprise Applications**
2. Click **+ New Application**
3. Select app
4. Create

---

<img width="1273" height="617" alt="Screenshot 2026-02-28 at 5 08 31 PM" src="https://github.com/user-attachments/assets/d5186a0a-d262-4bdd-abb8-0a3e82c7150b" />

---

## Assign App to Guest User

1. Go to Enterprise apps
2. Select App
3. Assign users & groups
4. Assign

---

<img width="879" height="438" alt="Screenshot 2026-02-28 at 5 11 12 PM" src="https://github.com/user-attachments/assets/02f5727f-7554-45d6-a66f-b1f62cf666b8" />

<img width="1318" height="505" alt="Screenshot 2026-02-28 at 5 11 44 PM" src="https://github.com/user-attachments/assets/78c940fe-5278-4180-9f40-7dc38c5bd147" />

---

# Conditional Access Policies

Conditional Access is the "if-then" engine.

Example:

* IF login from unknown country
* THEN require MFA

---

### Steps to Create Policy

1. Go to Conditional Access
2. Create New Policy
3. Add:

   * Policy name 
   * Users
   * Resources
   * Conditions
4. Grant controls:

   * Require MFA
   * Block
5. Enable policy
6. Create

---

<img width="1321" height="599" alt="Screenshot 2026-02-28 at 5 13 55 PM" src="https://github.com/user-attachments/assets/86a56604-a2a2-461d-a9e5-b5489508a092" />

---

⚠ If replacing security defaults, disable them first.

---

# Sign-in Risk & User Risk Policies

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

<img width="1362" height="732" alt="Screenshot 2026-02-28 at 5 16 39 PM" src="https://github.com/user-attachments/assets/38919668-28b8-4216-a80e-709c43bad95c" />

<img width="1347" height="723" alt="Screenshot 2026-02-28 at 5 20 18 PM" src="https://github.com/user-attachments/assets/91af0f40-254e-4886-9fe2-3ed31ed89370" />

---


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

I will continue expanding this lab with more advanced features to make this IAM learning journey even more interesting and practical.

Coming next:

- Privileged Identity Management (PIM)
- Identity Protection advanced configurations
- Dynamic groups
- Passwordless authentication (FIDO2, Windows Hello)
- Log Analytics and monitoring
- Hybrid identity (On-prem AD + Entra ID)
- Access governance best practices

This repository will evolve as I continue learning and testing advanced IAM features in Microsoft Entra ID.

Stay tuned — more hands-on labs coming soon!
.
.






