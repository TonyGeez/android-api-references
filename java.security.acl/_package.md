# java.security.acl

# java.security.acl

## Interfaces

| [Acl](Acl.md) | Interface representing an Access Control List (ACL). |
| --- | --- |
| [AclEntry](AclEntry.md) | This is the interface used for representing one entry in an Access Control List (ACL). |
| [Group](Group.md) | This interface is used to represent a group of principals. |
| [Owner](Owner.md) | Interface for managing owners of Access Control Lists (ACLs) or ACL configurations. |
| --- | --- |
| [Permission](Permission.md) | Legacy security code; do not use. |

## Exceptions

| [AclNotFoundException](AclNotFoundException.md) | This is an exception that is thrown whenever a reference is made to a non-existent ACL (Access Control List). |
| --- | --- |
| [LastOwnerException](LastOwnerException.md) | This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List. |
| [NotOwnerException](NotOwnerException.md) | This is an exception that is thrown whenever the modification of an object (such as an Access Control List) is only allowed to be done by an owner of the object, but the Principal attempting the modification is not an owner. |
