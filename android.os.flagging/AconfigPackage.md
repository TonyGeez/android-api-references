Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AconfigPackage

Kotlin | [Java](AconfigPackage.md)
| --- | --- |

```
open class AconfigPackage
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.flagging.AconfigPackage](AconfigPackage.md) |

An `aconfig` package containing the enabled state of its flags.

**Note: this is intended only to be used by generated code. To determine if a given flag is enabled in app code, the generated android flags should be used.**

This class is used to read the flag from Aconfig Package.Each instance of this class will cache information related to one package. To read flags from a different package, a new instance of this class should be load.

## Summary

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getBooleanFlagValue Retrieves the value of a boolean flag. |
| open static [AconfigPackage](AconfigPackage.md) | load Loads an Aconfig Package from Aconfig Storage. |

## Public methods

### getBooleanFlagValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBooleanFlagValue(
    flagName: String, 
    defaultValue: Boolean
): Boolean
```

Retrieves the value of a boolean flag.

This method retrieves the value of the specified flag. If the flag exists within the loaded Aconfig Package, its value is returned. Otherwise, the provided \`defaultValue\` is returned.

| Parameters ||
|---|---|
| `flagName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the flag (excluding any package name prefix). This value cannot be `null`. |
| `defaultValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The value to return if the flag is not found. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The boolean value of the flag, or \`defaultValue\` if the flag is not found. |

### load

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun load(packageName: String): AconfigPackage
```

Loads an Aconfig Package from Aconfig Storage.

This method attempts to load the specified Aconfig package.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the Aconfig package to load. This value cannot be `null`. |

| Return ||
|---|---|
| AconfigPackage | An instance of AconfigPackage, which may be empty if the package is not found in the container. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.flagging.AconfigStorageReadException` | if there is an error reading from Aconfig Storage, such as if the storage system is not found, the package is not found, or there is an error reading the storage file. The specific error code can be obtained using getErrorCode. |
