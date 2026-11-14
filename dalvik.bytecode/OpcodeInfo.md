# OpcodeInfo

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OpcodeInfo

```
class OpcodeInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [dalvik.bytecode.OpcodeInfo](OpcodeInfo.md) |

Information about Dalvik opcodes.

## Summary

| Properties ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAXIMUM_PACKED_VALUE](OpcodeInfo.md) The maximum possible "packed value" of a Dalvik opcode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAXIMUM_VALUE](OpcodeInfo.md) The maximum possible value of a Dalvik opcode. |

## Properties

### MAXIMUM_PACKED_VALUE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAXIMUM_PACKED_VALUE: Int
```

The maximum possible "packed value" of a Dalvik opcode. The packed value of an opcode is a denser representation that is only used when reporting usage statistics. The mapping between packed opcode values and regular opcode values is implementation-specific and may vary over time.

**Note:**: This is constant in any given VM incarnation, but it is subject to change over time, so it is not appropriate to represent as a compile-time constant value. 

### MAXIMUM_VALUE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAXIMUM_VALUE: Int
```

The maximum possible value of a Dalvik opcode.

**Note:**: This is constant in any given VM incarnation, but it is subject to change over time, so it is not appropriate to represent as a compile-time constant value.
