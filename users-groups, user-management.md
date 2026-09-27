Security Group

A security group was created to organize users who require IT support
permissions.

| Setting | Value |
|---|---|
| Group Name | IT Support |
| Group Type | Security |
| Group Scope | Global |
| Member | bdalimot |

The `bdalimot` user account was added as a member of the `IT Support`
security group.

Using security groups allows permissions to be assigned to a group
instead of configuring permissions individually for each user.


## Organizational Unit

An Organizational Unit (OU) was created to organize IT-related
accounts within the Active Directory domain.

The `bdalimot` user account was moved into the `IT` OU.

The current structure is:

homelab.local
└── IT
    └── bdalimot

Organizational Units can also be used as a target for Group Policy
and delegated administration.
