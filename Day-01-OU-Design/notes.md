# Day 1 — OU Design

## Objective
- Learn to create and organize Organizational Units (OUs) in Active Directory.
- Understand how OUs are structured for enterprise environments.

## Steps Completed

### Step 1 — Review Current OU Structure
- Open **Active Directory Users and Computers (ADUC)**.
- Observed existing OUs:
  - IT
  - HR
  - Sales
- **Screenshot:** `day1-01-current-ou-structure.png`

### Step 2 — Create Workstations OU
- Right-click domain → **New → Organizational Unit**.
- Name: `Workstations`
- **Protect from accidental deletion**: Checked
- **Screenshot:** `day1-02-add-workstations-ou.png`

### Step 3 — Create Corporate Parent OU
- Right-click domain → **New → Organizational Unit**.
- Name: `Corporate`
- **Protect from accidental deletion**: Checked
- **Screenshot:** `day1-03-create-corporate-ou.png`

### Step 4 — Move Child OUs under Corporate
- Drag and drop:
  - IT, HR, Sales, Workstations → Corporate OU
- **Screenshot:** `day1-04-ou-structure-organized.png`

### Step 5 — Enable Advanced Features
- **View → Advanced Features** in ADUC.
- Extra tabs now visible in OU properties:
  - Object (protect/unprotect deletion)
  - Security (permissions)
  - Attribute Editor (view/edit AD attributes)
- **Screenshot:** `day1-05-advanced-features-tabs.png`

### Step 6 — Review OU Design
- Corporate OU contains all child OUs.
- Naming conventions are clear and consistent.
- All critical OUs protected from accidental deletion.
- **Screenshot:** `day1-06-final-ou-review.png`

## Notes / Takeaways
- OU structure provides organization and simplifies delegation.
- Always plan parent and child OUs logically.
- Advanced Features reveal extra management options without giving superuser access.