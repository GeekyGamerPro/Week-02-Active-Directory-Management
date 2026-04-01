# Week 2 – Day 4: Domain Join (CLIENT01)

## Objective
Join CLIENT01 to the Active Directory domain (corp.geekytech.local) and verify successful authentication.

## Prerequisites
- DC01 is running and configured as Domain Controller  
- Domain: corp.geekytech.local exists  
- CLIENT01 is installed and on same internal network as DC01  
- DNS on CLIENT01 points to DC01 (192.168.10.1)

## Steps Completed

### 1. Network Setup
- CLIENT01 placed on same internal network as DC01  
- Verified connectivity using ping to DC01 (192.168.10.1)

### 2. DNS Configuration
- Set DNS server to: 192.168.10.1  
- Verified name resolution using nslookup

### 3. Domain Join
- Opened System Properties → Computer Name → Change  
- Selected “Domain” option  
- Entered: corp.geekytech.local  
- Authenticated using:
  - Username: CORP\Administrator  
  - Password: DC01 Administrator password  

### 4. Restart
- CLIENT01 restarted to apply domain changes

### 5. Login Verification
- Logged in using: CORP\Administrator  
- Confirmed successful domain authentication

## Screenshots Required
- Domain entry screen  
- Credentials prompt  
- Domain join success confirmation  
- Login screen showing CORP domain  
- Successful desktop login

## Key Concepts Learned
- Domain joining process in Windows  
- DNS requirement for Active Directory  
- Difference between local vs domain accounts  
- First-time domain login behavior (“Hi” screen)

## Outcome
CLIENT01 successfully joined to corp.geekytech.local domain and authenticated using domain credentials.