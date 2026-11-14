# ProtocolFamily

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProtocolFamily

```
interface ProtocolFamily
```

| [java.net.ProtocolFamily](../java/net/ProtocolFamily.md) |

| Known Direct Subclasses [StandardProtocolFamily](../java/net/StandardProtocolFamily.md) |----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [StandardProtocolFamily](../java/net/StandardProtocolFamily.md) | Defines the standard families of communication protocols. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [StandardProtocolFamily.INET](../java/net/StandardProtocolFamily.md), [StandardProtocolFamily.INET6](../java/net/StandardProtocolFamily.md), [StandardProtocolFamily.UNIX](../java/net/StandardProtocolFamily.md) |---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------| | [StandardProtocolFamily.INET](../java/net/StandardProtocolFamily.md) | Internet Protocol Version 4 (IPv4) | | [StandardProtocolFamily.INET6](../java/net/StandardProtocolFamily.md) | Internet Protocol Version 6 (IPv6) | | [StandardProtocolFamily.UNIX](../java/net/StandardProtocolFamily.md) | Unix domain (Local) interprocess communication. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents a family of communication protocols.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](../java/net/ProtocolFamily.md))`()` Returns the name of the protocol family. |

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
