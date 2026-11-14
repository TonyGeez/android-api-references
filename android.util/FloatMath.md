# FloatMath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FloatMath

Kotlin| [Java](../android/util/FloatMath.md) 
| --- | --- |

```
open class FloatMath
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.FloatMath](../android/util/FloatMath.md) |

| **This class was deprecated in API level 22.**
|
| Use [java.lang.Math](../java/lang/Math.md) instead.

Math routines similar to those found in [java.lang.Math](../java/lang/Math.md).

Historically these methods were faster than the equivalent double-based [java.lang.Math](../java/lang/Math.md) methods. On versions of Android with a JIT they became slower and have since been re-implemented to wrap calls to [java.lang.Math](../java/lang/Math.md). [java.lang.Math](../java/lang/Math.md) should be used in preference.

All methods were removed from the public API in version 23.

## Summary
