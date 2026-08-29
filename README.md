# osTicket: Post-Installation Configuration

## Project Overview

In this lab, I performed the post-installation configuration of **osTicket**, an open-source help desk ticketing system. I configured roles, departments, teams, agents, users, Service Level Agreements (SLAs), and help topics to simulate a functional enterprise help desk environment.

## Environments and Technologies Used

- Microsoft Azure Virtual Machines
- Windows 10/11
- Internet Information Services (IIS)
- osTicket
- PHP
- MySQL
- HeidiSQL

## osTicket Access URLs

### Admin/Analyst Login Page

```text
http://localhost/osTicket/scp/login.php
```

The Staff Control Panel is used by administrators and help desk agents to configure osTicket, manage users, and work support tickets.

### End-User Portal

```text
http://localhost/osTicket
```

The end-user portal allows customers to register, sign in, create tickets, and check the status of existing tickets.

## Post-Installation Configuration

### 1. Agent Panel vs. Admin Panel

After signing in to the Staff Control Panel, I reviewed the two primary interfaces:

- **Agent Panel:** Used by help desk agents to view, assign, manage, and resolve tickets.
- **Admin Panel:** Used by administrators to configure permissions, agents, departments, teams, SLAs, and help topics.

---

### 2. Configure Roles

Roles group permissions together and determine what agents are allowed to access and manage within osTicket.

**Navigation:**

```text
Admin Panel → Agents → Roles
```

I created the following role:

- **Supreme Admin**
- Granted full administrative permissions

![Supreme Admin Role](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 3. Configure Departments

Departments organize agents by support function and control ticket visibility.

**Navigation:**

```text
Admin Panel → Agents → Departments
```

I created the following department:

- **SysAdmins**

![SysAdmins Department](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 4. Configure Teams

Teams allow agents from different departments to work together on specific issues or projects.

**Navigation:**

```text
Admin Panel → Agents → Teams
```

I created the following team:

- **Online Banking**

![Online Banking Team](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 5. Configure User Registration

I configured osTicket to require users to register and sign in before submitting tickets.

**Navigation:**

```text
Admin Panel → Settings → Users
```

Configuration changes:

- Unchecked **Allow unregistered users to create tickets**
- Selected **Registration Required**
- Required users to register and sign in before creating tickets

This setting ensures that every ticket is connected to an authenticated user account.

![User Registration Settings](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 6. Configure Agents

Agents are help desk workers responsible for receiving, managing, and resolving support tickets.

**Navigation:**

```text
Admin Panel → Agents → Add New
```

I created the following agents:

| Agent | Department |
|---|---|
| Jane | SysAdmins |
| John | Support |

![Configured Agents](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 7. Configure Users

Users represent customers or employees who submit support requests through the end-user portal.

**Navigation:**

```text
Agent Panel → Users → Add New
```

I created the following users:

- Karen
- Ken

![Configured Users](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

### 8. Configure Service Level Agreements

Service Level Agreements establish the expected response and resolution timeframes for tickets based on severity.

**Navigation:**

```text
Admin Panel → Manage → SLA
```

I configured the following SLA plans:

| SLA Plan | Grace Period | Schedule |
|---|---:|---|
| Sev-A | 1 hour | 24/7 |
| Sev-B | 4 hours | 24/7 |
| Sev-C | 8 hours | Business Hours |

![Configured SLA Plans] <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/4b26b941-1a78-45ca-b166-25c5a79425b3" />


---

### 9. Configure Help Topics

Help topics allow users to categorize their requests when creating tickets. This helps route tickets to the appropriate department or support team.

**Navigation:**

```text
Admin Panel → Manage → Help Topics
```

I created the following help topics:

- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
- Other

![Configured Help Topics](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

## Configuration Summary

| Component | Configuration |
|---|---|
| Role | Supreme Admin |
| Department | SysAdmins |
| Team | Online Banking |
| Agents | Jane and John |
| Users | Karen and Ken |
| SLA Plans | Sev-A, Sev-B, and Sev-C |
| Help Topics | Business outage, computer issues, equipment requests, password resets, and other |
| User Access | Registration and login required |

## Skills Demonstrated

- Help desk system administration
- Role-based access control
- Permission management
- Department and team configuration
- Agent and user account administration
- Service Level Agreement configuration
- Ticket categorization and workflow organization
- Enterprise help desk ticketing experience

## Conclusion

This lab provided hands-on experience configuring osTicket after installation. I created roles, departments, teams, agents, users, SLAs, and help topics to build a structured help desk environment.

These configurations created the foundation needed to simulate real-world ticket intake, assignment, escalation, troubleshooting, and resolution.
