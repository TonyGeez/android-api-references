# java.security.acl

# java.security.acl

## Interfaces

| [Acl](https://developer.android.com/reference/kotlin/java/security/acl/Acl) | Interface representing an Access Control List (ACL). |
| [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry) | This is the interface used for representing one entry in an Access Control List (ACL). |
| [Group](https://developer.android.com/reference/kotlin/java/security/acl/Group) | This interface is used to represent a group of principals. |
| [Owner](https://developer.android.com/reference/kotlin/java/security/acl/Owner) | Interface for managing owners of Access Control Lists (ACLs) or ACL configurations. |
| [Permission](https://developer.android.com/reference/kotlin/java/security/acl/Permission) | Legacy security code; do not use. |

## Exceptions

| [AclNotFoundException](https://developer.android.com/reference/kotlin/java/security/acl/AclNotFoundException) | This is an exception that is thrown whenever a reference is made to a non-existent ACL (Access Control List). |
| [LastOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/LastOwnerException) | This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List. |
| [NotOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/NotOwnerException) | This is an exception that is thrown whenever the modification of an object (such as an Access Control List) is only allowed to be done by an owner of the object, but the Principal attempting the modification is not an owner. |
