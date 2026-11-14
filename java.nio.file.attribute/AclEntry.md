# AclEntry

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntry

```
class AclEntry
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.AclEntry](../java/nio/file/attribute/AclEntry.md) |

An entry in an access control list (ACL).

The ACL entry represented by this class is based on the ACL model specified in [*RFC 3530: Network File System (NFS) version 4 Protocol*](http://www.ietf.org/rfc/rfc3530.txt). Each entry has four components as follows:

1. The [type](../java/nio/file/attribute/AclEntry.md))component determines if the entry grants or denies access.
2. The [principal](../java/nio/file/attribute/AclEntry.md))component, sometimes called the "who" component, is a [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) corresponding to the identity that the entry grants or denies access
3. The [permissions](../java/nio/file/attribute/AclEntry.md))component is a set of [permissions](../java/nio/file/attribute/AclEntryPermission.md)
4. The [flags](../java/nio/file/attribute/AclEntry.md))component is a set of [flags](../java/nio/file/attribute/AclEntryFlag.md) to indicate how entries are inherited and propagated

ACL entries are created using an associated [Builder](../java/nio/file/attribute/AclEntry.Builder.md) object by invoking its [build](../java/nio/file/attribute/AclEntry.Builder.md))method.

ACL entries are immutable and are safe for use by multiple concurrent threads.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../java/nio/file/attribute/AclEntry.Builder.md) A builder of [AclEntry](../java/nio/file/attribute/AclEntry.md) objects. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/nio/file/attribute/AclEntry.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this ACL entry for equality. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AclEntryFlag](../java/nio/file/attribute/AclEntryFlag.md)!\>! | [flags](../java/nio/file/attribute/AclEntry.md))`()` Returns a copy of the flags component. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/nio/file/attribute/AclEntry.md))`()` Returns the hash-code value for this ACL entry. |
| --- | --- |
| static [AclEntry.Builder](../java/nio/file/attribute/AclEntry.Builder.md)! | [newBuilder](../java/nio/file/attribute/AclEntry.md))`()` Constructs a new builder. |
| static [AclEntry.Builder](../java/nio/file/attribute/AclEntry.Builder.md)! | [newBuilder](../java/nio/file/attribute/AclEntry.md))`(`entry:` ` [AclEntry](../java/nio/file/attribute/AclEntry.md)!`)` Constructs a new builder with the components of an existing ACL entry. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AclEntryPermission](../java/nio/file/attribute/AclEntryPermission.md)!\>! | [permissions](../java/nio/file/attribute/AclEntry.md))`()` Returns a copy of the permissions component. |
| --- | --- |
| [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)! | [principal](../java/nio/file/attribute/AclEntry.md))`()` Returns the principal component. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/nio/file/attribute/AclEntry.md))`()` Returns the string representation of this ACL entry. |
| [AclEntryType](../java/nio/file/attribute/AclEntryType.md)! | [type](../java/nio/file/attribute/AclEntry.md))`()` Returns the ACL entry type. |
| --- | --- |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares the specified object with this ACL entry for equality.

If the given object is not an`AclEntry`then this method immediately returns`false`.

For two ACL entries to be considered equals requires that they are both the same type, their who components are equal, their permissions components are equal, and their flags components are equal.

This method satisfies the general contract of the [Object.equals](../java/lang/Object.md))method.

| Parameters ||
|-------|---------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `ob` | the object to which this object is to be compared |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the given object is an AclEntry that is identical to this AclEntry |

### flags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flags(): MutableSet<AclEntryFlag!>!
```

Returns a copy of the flags component.

The returned set is a modifiable copy of the flags.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AclEntryFlag](../java/nio/file/attribute/AclEntryFlag.md)!>! | the flags component |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash-code value for this ACL entry.

This method satisfies the general contract of the [java.lang.Object#hashCode](../java/lang/Object.md))method.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### newBuilder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBuilder(): AclEntry.Builder!
```

Constructs a new builder. The initial value of the type and who components is`null`. The initial value of the permissions and flags components is the empty set.

| Return ||
|--------------------------------------------------------------------------------------------------------------|---------------|
| [AclEntry.Builder](../java/nio/file/attribute/AclEntry.Builder.md)! | a new builder |

### newBuilder

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newBuilder(entry: AclEntry!): AclEntry.Builder!
```

Constructs a new builder with the components of an existing ACL entry.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `entry` | [AclEntry](../java/nio/file/attribute/AclEntry.md)!:an ACL entry |

| Return ||
|--------------------------------------------------------------------------------------------------------------|---------------|
| [AclEntry.Builder](../java/nio/file/attribute/AclEntry.Builder.md)! | a new builder |

### permissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun permissions(): MutableSet<AclEntryPermission!>!
```

Returns a copy of the permissions component.

The returned set is a modifiable copy of the permissions.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AclEntryPermission](../java/nio/file/attribute/AclEntryPermission.md)!>! | the permissions component |

### principal

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun principal(): UserPrincipal!
```

Returns the principal component.

| Return ||
|--------------------------------------------------------------------------------------------------------|-------------------------|
| [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md)! | the principal component |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the string representation of this ACL entry.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this entry |

### type

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun type(): AclEntryType!
```

Returns the ACL entry type.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------|
| [AclEntryType](../java/nio/file/attribute/AclEntryType.md)! | the ACL entry type |
