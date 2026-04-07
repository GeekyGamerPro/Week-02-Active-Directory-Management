# Week 2 – Day 6: File Sharing & NTFS Permissions (Active Directory)

## Objective
Configure and test shared folder access in an Active Directory environment using Share and NTFS permissions, while validating correct security enforcement between DC01 and CLIENT01.

---

## Prerequisites
- DC01 is running and part of the domain environment  
- CLIENT01 is joined to `corp.geekytech.local`  
- DNS is pointing to DC01 (192.168.10.1)

---

## Steps Completed

### 1. Folder Creation
- Created directory:
  C:\Shares\ITDocs

---

### 2. SMB Share Configuration
- Enabled sharing on ITDocs folder  
- Share name: ITDocs  
- Removed Everyone group  
- Added Domain Users  
- Initially Share permissions were too permissive (allowed write access)  
- Corrected Share permissions to **Read only**  
- Applied and confirmed settings

---

### 3. NTFS Permissions Configuration
- Opened Security tab on ITDocs folder  
- Added Domain Users  
- Applied Read & Execute, List Folder Contents, Read permissions only  
- Initially inheritance and previous permissions caused unexpected write access  
- Disabled inheritance and removed incorrect permissions  
- Corrected NTFS to enforce read-only access  
- Applied and confirmed settings

---

### 4. Client Access Test
- Accessed shared folder from CLIENT01 using:
  \\DC01\ITDocs  
- Verified folder access from domain client  

---

### 5. Permission Validation Test
- Initially able to create files due to overly permissive Share permissions  
- After corrections, attempted file creation from CLIENT01  
- Action was denied with message:
  “You need permission to perform this action”  
- Confirmed NTFS and Share permissions are properly enforced

---

## Issues Encountered & Resolutions

### Issue 1: Users were able to create files
- **Cause:** Share permissions initially allowed "Change" or overly broad access  
- **Fix:** Removed Everyone group and restricted Share permissions to Read only for Domain Users  

---

### Issue 2: NTFS inheritance and legacy permissions affected behavior
- **Cause:** Existing inherited permissions allowed unintended write access  
- **Fix:** Disabled inheritance and explicitly defined Domain Users permissions  

---

### Issue 3: Confusion between Share vs NTFS permissions
- **Cause:** Both permission layers were not initially aligned  
- **Fix:** Applied correct security model understanding:
  - Share = network access layer  
  - NTFS = file system security layer  
  - Most restrictive permission applies  

---

## Key Concepts Learned
- SMB file sharing in Windows Server environments  
- Difference between Share and NTFS permissions  
- Permission layering and most restrictive rule behavior  
- Active Directory group-based access control  
- Real-world troubleshooting of file server access issues  

---

## Outcome
A secure shared folder was successfully configured with read-only access for Domain Users. Permission issues were identified, analyzed, and resolved, demonstrating real-world troubleshooting and Active Directory administration skills.