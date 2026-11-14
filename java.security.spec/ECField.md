# ECField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ECField

```
interface ECField
```

| [java.security.spec.ECField](../java/security/spec/ECField.md) |

| Known Direct Subclasses [ECFieldF2m](../java/security/spec/ECFieldF2m.md), [ECFieldFp](../java/security/spec/ECFieldFp.md) |--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [ECFieldF2m](../java/security/spec/ECFieldF2m.md) | This immutable class defines an elliptic curve (EC) characteristic 2 finite field. | | [ECFieldFp](../java/security/spec/ECFieldFp.md) | This immutable class defines an elliptic curve (EC) prime finite field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This interface represents an elliptic curve (EC) finite field. All specialized EC fields must implements this interface.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFieldSize](../java/security/spec/ECField.md))`()` Returns the field size in bits. |

## Public methods

### getFieldSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFieldSize(): Int
```

Returns the field size in bits. Note: For prime finite field ECFieldFp, size of prime p in bits is returned. For characteristic 2 finite field ECFieldF2m, m is returned.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the field size in bits. |
