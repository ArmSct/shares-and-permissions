# Network File Sharing and Permissions

This lab demonstrates how to create network file shares on a domain controller and manage access through group-based permissions in Active Directory. You will test file access from a standard user account and observe how group membership affects share access. A domain controller (DC-1) and client (Client-1) virtual machine are pre-configured for this lab.

## Technologies Utilized
- Microsoft Azure
- Active Directory Domain Services (AD DS)
- File and Storage Services
- Shared Folder Permissions
- Security Groups

## Actions and Observations

### File Share Setup

Log into DC-1 as the domain administrator and into Client-1 as a standard domain user. On DC-1, create the following four appropriately named folders on the C:\ drive.

![mstsc_DyWmML3cbx](https://github.com/user-attachments/assets/520660d4-9834-45e8-897f-2a3ccea449ec)

Domain Users have read-only access to the read-access folder and read/write permissions on the write-access folder, while Domain Admins have read/write access to the no-access folder.

![mstsc_zxGLDQ4tff](https://github.com/user-attachments/assets/3d1921e1-90b3-44de-9c9f-7bf75338a50d)

![mstsc_zxGLDQ4tff](https://github.com/user-attachments/assets/d29d95a5-c0b4-488c-aa36-2f2429790583)

### Testing Share Access as a Regular User

Confirm that permissions for folders are tied to their respective Security Group. Navigate to the shared folders and test each folder to see which ones can or cannot be opened or modified.

