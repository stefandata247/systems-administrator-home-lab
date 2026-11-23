# Project 02 — Linux User and Permission Management

## 1. Project Overview

**Objective:** Simulate employee account administration within a business environment using RHEL 10.

This project demonstrates how to create users, organize department groups, configure directory ownership, and enforce file permissions.

## 2. Business Scenario

A company requires Linux accounts for employees in two departments:

- IT Department
- Human Resources Department

The administrator must create employee accounts and restrict access to departmental directories.

## 3. Skills Demonstrated

- Linux user management
- Group management
- Password administration
- File ownership
- File permissions
- Access control

## 4. Implementation Steps

### Step 1 — Create Department Groups

```bash
sudo groupadd IT
sudo groupadd HR
```

### Step 2 — Create Employee Accounts

```bash
sudo useradd -m -s /bin/bash jsmith
sudo useradd -m -s /bin/bash mjones
sudo useradd -m -s /bin/bash bwilliams
```

### Step 3 — Set User Passwords

```bash
sudo passwd jsmith
sudo passwd mjones
sudo passwd bwilliams
```

### Step 4 — Assign Department Groups

```bash
sudo usermod -aG IT jsmith
sudo usermod -aG IT mjones
sudo usermod -aG HR bwilliams
```

### Step 5 — Create Department Directories

```bash
sudo mkdir -p /company/IT
sudo mkdir -p /company/HR
```

### Step 6 — Configure Directory Ownership

```bash
sudo chown root:IT /company/IT
sudo chown root:HR /company/HR
```

### Step 7 — Configure Permissions

```bash
sudo chmod 2770 /company/IT
sudo chmod 2770 /company/HR
```

### Step 8 — Verify Accounts and Permissions

```bash
id jsmith
id mjones
id bwilliams

ls -ld /company/IT
ls -ld /company/HR
```

### Step 9 — Test Access

```bash
sudo -u jsmith touch /company/IT/test.txt

sudo -u bwilliams touch /company/IT/denied.txt
```

The IT user should be able to create the file. The HR user should receive a permission-denied error when accessing the IT directory.

## 5. Verification

Confirm user accounts, group membership, ownership, and directory permissions.

## 6. Screenshots

Recommended screenshots:

1. User account creation
2. Department group creation
3. User group membership
4. Directory ownership
5. Successful and denied access tests

## 7. Troubleshooting

Document any account creation errors, group membership issues, or permission problems.

## 8. Lessons Learned

Developed practical experience managing Linux accounts, departmental groups, directory ownership, and access control.

## 9. Project Status

Update after successful implementation and testing.


