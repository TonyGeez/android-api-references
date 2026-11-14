Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ButtonCustomizationTrigger

```
class ButtonCustomizationTrigger : CustomizationTrigger
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.hardware.input.CustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger) ||
| | ↳ | [android.hardware.input.ButtonCustomizationTrigger](https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#) |

Represents a trigger based on a physical button press on a peripheral (e.g., a mouse).

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_BACK:kotlin.Int` Customizable Button code: Back button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_EXTRA:kotlin.Int` Customizable Button code: Extra button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_FORWARD:kotlin.Int` Customizable Button code: Forward button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_SIDE:kotlin.Int` Customizable Button code: Side button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TASK:kotlin.Int` Customizable Button code: Task button. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TERTIARY:kotlin.Int` Customizable Button code: Tertiary/Middle button. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#ButtonCustomizationTrigger(kotlin.Int)(buttonCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a Trigger for a specific button code. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#getButtonCode()()` Returns the button code associated with this trigger. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#toString()()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. The `equals` method implements an equivalence relation on non-null object references: - It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`. - It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`. - It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`. - It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified. - For any non-null reference value `x`, `x.equals(null)` should return `false`. An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/hardware/input/CustomizationTrigger#hashCode()()` Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`. The general contract of `hashCode` is: - Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application. - If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result. - It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables. <br /> | ||

## Constants

### CUSTOMIZABLE_BUTTON_BACK

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_BACK: Int
```

Customizable Button code: Back button.

 Value: 8

### CUSTOMIZABLE_BUTTON_EXTRA

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_EXTRA: Int
```

Customizable Button code: Extra button.

 Value: 128

### CUSTOMIZABLE_BUTTON_FORWARD

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_FORWARD: Int
```

Customizable Button code: Forward button.

 Value: 16

### CUSTOMIZABLE_BUTTON_SIDE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_SIDE: Int
```

Customizable Button code: Side button.

 Value: 256

### CUSTOMIZABLE_BUTTON_TASK

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_TASK: Int
```

Customizable Button code: Task button.

 Value: 512

### CUSTOMIZABLE_BUTTON_TERTIARY

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUSTOMIZABLE_BUTTON_TERTIARY: Int
```

Customizable Button code: Tertiary/Middle button.

 Value: 4

## Public constructors

### ButtonCustomizationTrigger

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ButtonCustomizationTrigger(buttonCode: Int)
```

Creates a Trigger for a specific button code.

| Parameters ||
|---|---|
| `buttonCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The button code for the trigger. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TERTIARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_EXTRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_SIDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TASK:kotlin.Int` |

## Public methods

### getButtonCode

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getButtonCode(): Int
```

Returns the button code associated with this trigger.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TERTIARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_BACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_FORWARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_EXTRA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_SIDE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/input/ButtonCustomizationTrigger#CUSTOMIZABLE_BUTTON_TASK:kotlin.Int` |

### toString

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
