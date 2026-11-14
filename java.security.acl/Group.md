# Group

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Group

```
interface Group : Principal
```

| [java.security.acl.Group](../java/security/acl/Group.md) |

| **This interface was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

This interface is used to represent a group of principals. (A principal represents an entity such as an individual user or a company).

Note that Group extends Principal. Thus, either a Principal or a Group can be passed as an argument to methods containing a Principal parameter. For example, you can add either a Principal or a Group to a Group object by calling the object's`addMember`method, passing it the Principal or Group.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addMember](../java/security/acl/Group.md))`(`user:` ` [Principal](../java/security/Principal.md)!`)` Adds the specified member to the group. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMember](../java/security/acl/Group.md))`(`member:` ` [Principal](../java/security/Principal.md)!`)` Returns true if the passed principal is a member of the group. |
| abstract [Enumeration](../java/util/Enumeration.md)\<out [Principal](../java/security/Principal.md)!\>! | [members](../java/security/acl/Group.md))`()` Returns an enumeration of the members in the group. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeMember](../java/security/acl/Group.md))`(`user:` ` [Principal](../java/security/Principal.md)!`)` Removes the specified member from the group. |

| Inherited functions ||
|---|---|
| From class [Principal](../java/security/Principal.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/Principal.md))`()` <br /> Returns the name of this principal. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Principal.md))`(`subject:` ` [Subject](../javax/security/auth/Subject.md)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

## Public methods

### addMember

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addMember(user: Principal!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds the specified member to the group.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `user` | [Principal](../java/security/Principal.md)!:the principal to add to this group. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the member was successfully added, false if the principal was already a member. |

### isMember

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isMember(member: Principal!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the passed principal is a member of the group. This method does a recursive search, so if a principal belongs to a group which is a member of this group, true is returned.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `member` | [Principal](../java/security/Principal.md)!:the principal whose membership is to be checked. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the principal is a member of this group, false otherwise. |

### members

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun members(): Enumeration<out Principal!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration of the members in the group. The returned objects can be instances of either Principal or Group (which is a subclass of Principal).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Enumeration](../java/util/Enumeration.md)<out` ` [Principal](../java/security/Principal.md)!>! | an enumeration of the group members. |

### removeMember

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeMember(user: Principal!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes the specified member from the group.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `user` | [Principal](../java/security/Principal.md)!:the principal to remove from this group. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the principal was removed, or false if the principal was not a member. |
