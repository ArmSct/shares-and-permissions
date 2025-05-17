
![image](https://github.com/user-attachments/assets/1cb2e6ca-2cd3-4771-8607-1514a5edf225)

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

![mstsc_DWcvUDjSUO](https://github.com/user-attachments/assets/1b95621e-5a77-4b1f-8b65-3dbb7f2864d4)

![mstsc_Yp6DLMw0a1](https://github.com/user-attachments/assets/83db58fe-3bf6-4e00-abec-ce15d2952736)

![mstsc_Q8gWCsiDm2](https://github.com/user-attachments/assets/df605a47-aac9-48b5-a5e0-c5b4d0b36386)

### Creating Group-Based Access

On the domain controller open the Active Directory Users and Computers panel. Create a new Group called ACCOUNTANTS. Then assign Read/Write permissions to the ACCOUNTANTS group.

![mstsc_DjmDPCajlu](https://github.com/user-attachments/assets/e6243e4e-2144-49a8-9860-ec91136c74f4)

Observe how the user cannot access the accounting folder because they are not part of the ACCOUNTANTS Security Group.

![mstsc_cMWXBdj2Ka](https://github.com/user-attachments/assets/911ef3e0-8d20-4f05-89ee-2d27c8d937cc)

On domain controller open the ACCOUNTANTS Properties on Active Directory Users and Computers. Add the user to the ACCOUNTANTS group. 

![mstsc_kUpuDPoUAA](https://github.com/user-attachments/assets/d761333f-e47c-4bbf-b447-7926dec9a4fd)

Then, as the client, open the accounting folder and observe how the user now has read and write permissions.

![mstsc_t77xA3pEMa](https://github.com/user-attachments/assets/1febc16b-135b-4b08-8ada-5f9cefcfd740)
