# Notification.Extender

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Extender

Kotlin| [Java](https://developer.android.com/reference/android/app/Notification.Extender "View this page in Java") 
| --- | --- |

```
interface Extender
```

| [android.app.Notification.Extender](https://developer.android.com/reference/kotlin/android/app/Notification.Extender#) |

| Known Direct Subclasses [Notification.CarExtender](https://developer.android.com/reference/kotlin/android/app/Notification.CarExtender), [Notification.TvExtender](https://developer.android.com/reference/kotlin/android/app/Notification.TvExtender), [Notification.WearableExtender](https://developer.android.com/reference/kotlin/android/app/Notification.WearableExtender) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [Notification.CarExtender](https://developer.android.com/reference/kotlin/android/app/Notification.CarExtender) | Helper class to add Android Auto extensions to notifications. | | [Notification.TvExtender](https://developer.android.com/reference/kotlin/android/app/Notification.TvExtender) | Helper class to add Android TV extensions to notifications. | | [Notification.WearableExtender](https://developer.android.com/reference/kotlin/android/app/Notification.WearableExtender) | Helper class to add wearable extensions to notifications. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Extender interface for use with [Builder.extend](https://developer.android.com/reference/kotlin/android/app/Notification.Builder#extend(android.app.Notification.Extender)). Extenders may be used to add metadata or change options on a notification builder.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Notification.Builder](https://developer.android.com/reference/kotlin/android/app/Notification.Builder)! | [extend](https://developer.android.com/reference/kotlin/android/app/Notification.Extender#extend(android.app.Notification.Builder))`(`builder:` ` [Notification.Builder](https://developer.android.com/reference/kotlin/android/app/Notification.Builder)!`)` Apply this extender to a notification builder. |

## Public methods

### extend

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun extend(builder: Notification.Builder!): Notification.Builder!
```

Apply this extender to a notification builder.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `builder` | [Notification.Builder](https://developer.android.com/reference/kotlin/android/app/Notification.Builder)!:the builder to be modified |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------|
| [Notification.Builder](https://developer.android.com/reference/kotlin/android/app/Notification.Builder)! | the build object for chaining |
