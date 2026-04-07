# Week 2 – Day 7: Domain User Login & Permission Validation (Active Directory)

## Objective
Validate Active Directory user authentication, profile creation, group membership, and file share permissions using a domain-joined client machine.

---

## Prerequisites
- DC01 is running and part of the domain environment  
- CLIENT01 is joined to `corp.geekytech.local`  
- DNS is pointing to DC01 (192.168.10.1)  
- Active Directory users and groups already created

---

## Steps Completed

### 1. Domain User Login
- Logged into CLIENT01 using domain account:
  CORP\jcarter  
- First login triggered user profile creation process

---

### 2. Profile Creation Verification
- Verified new user profile created in:
  C:\Users\jcarter  
- Confirmed successful domain-based profile provisioning

---

### 3. Group Membership Validation
- Ran `whoami /groups` to verify security groups  
- Confirmed user is part of:
  - Domain Users  
  - Additional assigned AD groups (if applicable)

---

### 4. File Share Access Test
- Accessed shared folder:
  \\DC01\ITDocs  
- Confirmed read access and visibility of shared directory

---

### 5. Permission Enforcement Testing
- Attempted to create a file in shared directory  
- Action failed with “You need permission to perform this action”  
- Confirmed NTFS and Share permissions are enforcing read-only access

---

## Issues Encountered & Resolutions

### Issue 1: Username confusion during login
- **Cause:** Display name was mistaken for login name  
- **Fix:** Used correct SAMAccountName format (CORP\\jcarter)

---

### Issue 2: Initial permission inconsistencies
- **Cause:** Share permissions were too permissive and NTFS inheritance caused conflicts  
- **Fix:** Adjusted Share permissions to Read-only and cleaned NTFS inheritance

---

## Key Concepts Learned
- Active Directory domain authentication  
- User profile creation on first login  
- Group-based access control  
- NTFS vs Share permission hierarchy  
- Real-world file server security enforcement  
- Permission troubleshooting and validation

---

## Outcome
Successfully validated a complete Active Directory authentication and file access control workflow using a domain-joined client system. The environment correctly enforces security policies and restricts unauthorized file modifications.