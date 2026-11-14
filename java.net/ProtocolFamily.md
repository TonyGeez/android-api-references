# ProtocolFamily

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtocolFamily

```
interface ProtocolFamily
```

| [java.net.ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily#) |

| Known Direct Subclasses [StandardProtocolFamily](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily) |----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [StandardProtocolFamily](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily) | Defines the standard families of communication protocols. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [StandardProtocolFamily.INET](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:INET), [StandardProtocolFamily.INET6](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:INET6), [StandardProtocolFamily.UNIX](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:UNIX) |---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------| | [StandardProtocolFamily.INET](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:INET) | Internet Protocol Version 4 (IPv4) | | [StandardProtocolFamily.INET6](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:INET6) | Internet Protocol Version 6 (IPv6) | | [StandardProtocolFamily.UNIX](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily#ENUM_VALUE:UNIX) | Unix domain (Local) interprocess communication. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents a family of communication protocols.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily#name())`()` Returns the name of the protocol family. |

## Public methods

### name

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun name(): String!
```

Returns the name of the protocol family.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the protocol family |
