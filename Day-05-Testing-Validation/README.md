# Week 2 – Day 5: Domain Validation & Testing

## Objective
Validate Active Directory functionality by testing domain authentication, hostname configuration, and DNS resolution between CLIENT01 and DC01.

---

## Prerequisites
- DC01 is running as Domain Controller  
- CLIENT01 is joined to `corp.geekytech.local`  
- DNS on CLIENT01 points to DC01 (192.168.10.1)  
- Domain login is working (`CORP\Administrator` or domain user)

---

## Steps Completed

### 1. Domain Verification (whoami)
- Ran `whoami` on CLIENT01  
- Confirmed system is logged into the CORP domain  

---

### 2. Hostname Verification
- Ran `hostname`  
- Verified computer name (updated to CLIENT01 if renamed)

---

### 3. Computer Rename (if needed)
- Renamed system to CLIENT01 via System Properties  
- Restarted system to apply changes  
- Logged back in successfully

---

### 4. Domain Context Verification
- Ran `echo %USERDOMAIN%`  
- Confirmed output shows: CORP  

---

### 5. Network Connectivity Test
- Ran `ping dc01`  
- Verified successful communication with Domain Controller  

---

### 6. DNS Validation
- Ran `nslookup dc01`  
- Confirmed DNS resolution to DC01 IP (192.168.10.1)  
- Note: “Server: Unknown” may appear, this is normal without reverse lookup configuration

---

## Key Concepts Learned
- Domain authentication validation
- Hostname verification after rename
- DNS role in Active Directory environments
- Basic network connectivity between domain client and DC
- Understanding nslookup output behavior

---

## Outcome
CLIENT01 is fully validated within the Active Directory environment.  
Domain authentication, DNS resolution, and network communication are all functioning correctly.# Week 2 – Day 5: Domain Validation & Testing

## Objective
Validate Active Directory functionality by testing domain authentication, hostname configuration, and DNS resolution between CLIENT01 and DC01.

---

## Prerequisites
- DC01 is running as Domain Controller  
- CLIENT01 is joined to `corp.geekytech.local`  
- DNS on CLIENT01 points to DC01 (192.168.10.1)  
- Domain login is working (`CORP\Administrator` or domain user)

---

## Steps Completed

### 1. Domain Verification (whoami)
- Ran `whoami` on CLIENT01  
- Confirmed system is logged into the CORP domain  

---

### 2. Hostname Verification
- Ran `hostname`  
- Verified computer name (updated to CLIENT01 if renamed)

---

### 3. Computer Rename (if needed)
- Renamed system to CLIENT01 via System Properties  
- Restarted system to apply changes  
- Logged back in successfully

---

### 4. Domain Context Verification
- Ran `echo %USERDOMAIN%`  
- Confirmed output shows: CORP  

---

### 5. Network Connectivity Test
- Ran `ping dc01`  
- Verified successful communication with Domain Controller  

---

### 6. DNS Validation
- Ran `nslookup dc01`  
- Confirmed DNS resolution to DC01 IP (192.168.10.1)  
- Note: “Server: Unknown” may appear, this is normal without reverse lookup configuration

---

## Key Concepts Learned
- Domain authentication validation
- Hostname verification after rename
- DNS role in Active Directory environments
- Basic network connectivity between domain client and DC
- Understanding nslookup output behavior

---

## Outcome
CLIENT01 is fully validated within the Active Directory environment.  
Domain authentication, DNS resolution, and network communication are all functioning correctly.