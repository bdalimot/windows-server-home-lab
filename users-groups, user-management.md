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


## Group Policy

A Group Policy Object (GPO) named `IT Security Policy` was created
and linked to the `IT` Organizational Unit.

The GPO was configured with the following user policy:

- Remove and prevent access to the Shut Down, Restart, Sleep, and
  Hibernate commands

The policy was tested on the Windows 11 client using the
`egatchalian` domain account.

After running `gpupdate /force`, the Power options were restricted
and only the Lock option remained available.

This confirmed that the GPO was successfully applied to the user.
