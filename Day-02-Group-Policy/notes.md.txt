# Day 2 — Group Policy Basics

## Objective
- Learn how to create and edit a Group Policy Object (GPO).
- Understand linking GPOs to OUs and testing policy effects.

## Steps Completed

### Step 1 — Open Group Policy Management Console (GPMC)
- Press **Windows + S → type Group Policy Management → Enter**.
- Observed domain: `corp.geekytech.local` and OUs (Corporate → IT, HR, Sales, Workstations).
- **Screenshot:** `day2-01-gpmc-console.png`

### Step 2 — Create First GPO
- Right-click **IT OU → Create a GPO in this domain, and Link it here…**
- Name: `IT_Workstation_Policy`
- **Screenshot:** `day2-02-create-gpo.png`

### Step 3 — Edit GPO
- Right-click GPO → **Edit**
- Example Policy: Set Desktop Wallpaper
  - Path: `C:\Windows\Web\Wallpaper\Windows\img0.jpg`
  - Style: Fill
  - Enabled
- **Screenshot:** `day2-03-gpo-edit-wallpaper.png`

### Step 4 — Test GPO
- DC01 used as test environment (client VM not yet created).
- Run in Command Prompt: `gpupdate /force`
- Wallpaper policy applied to logged-in user on DC.
- **Screenshot:** `day2-04-gpo-tested.png`

## Notes / Takeaways
- GPOs control user and computer configurations across the domain.
- Policies are linked to OUs; only objects in that OU are affected.
- Advanced testing with a client VM will show effects for domain users.
- The process of creating, editing, and linking GPOs is the critical learning outcome.