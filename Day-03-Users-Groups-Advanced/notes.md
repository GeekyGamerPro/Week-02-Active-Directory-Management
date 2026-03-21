# Day 3 — Users and Groups (Advanced)

## Objective
- Practice creating users and groups with more realistic details.
- Understand how group membership is used to manage access.

## Steps Completed

### Step 1 — Review Existing Users and Groups
- Opened Active Directory Users and Computers (ADUC).
- Reviewed users and groups in:
  - IT
  - HR
  - Sales
- Verified previous setup from Week 1.
- **Screenshot:** `day3-01-review-users-groups.png`

### Step 2 — Create Detailed User
- Created new user in IT OU:
  - Name: David Williams
  - Username: dwilliams
- Added description:
  - "IT Support Technician"
- **Screenshot:** `day3-02-create-detailed-user.png`

### Step 3 — Create Security Group
- Created new group in IT OU:
  - Name: IT_Support
  - Scope: Global
  - Type: Security
- Added description:
  - "IT support team with standard privileges"
- **Screenshot:** `day3-03-create-it-support-group.png`

### Step 4 — Add User to Group
- Added David Williams to:
  - IT_Support group
- Verified using **Member Of** tab.
- **Screenshot:** `day3-04-add-dwilliams-to-it-support.png`

### Step 5 — Final Verification
- Confirmed IT OU contains:
  - Users:
    - John Carter
    - David Williams
  - Groups:
    - IT_Admins
    - IT_Support
- Verified group membership via **Members tab**
- **Screenshot:** `day3-05-final-review.png`

## Notes / Takeaways
- Users should include descriptions to reflect real job roles.
- Groups are used to manage permissions instead of assigning access directly to users.
- Adding users to groups simplifies administration and scales better in enterprise environments.
- Proper organization of users and groups improves management and security.