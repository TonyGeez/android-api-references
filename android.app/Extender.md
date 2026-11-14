# Notification.Extender

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Extender

Kotlin| [Java](../android/app/Notification.Extender.md) 
| --- | --- |

```
interface Extender
```

| [android.app.Notification.Extender](../android/app/Notification.Extender.md) |

| Known Direct Subclasses [Notification.CarExtender](../android/app/Notification.CarExtender.md), [Notification.TvExtender](../android/app/Notification.TvExtender.md), [Notification.WearableExtender](../android/app/Notification.WearableExtender.md) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------| | [Notification.CarExtender](../android/app/Notification.CarExtender.md) | Helper class to add Android Auto extensions to notifications. | | [Notification.TvExtender](../android/app/Notification.TvExtender.md) | Helper class to add Android TV extensions to notifications. | | [Notification.WearableExtender](../android/app/Notification.WearableExtender.md) | Helper class to add wearable extensions to notifications. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Extender interface for use with [Builder.extend](../android/app/Notification.Builder.md)). Extenders may be used to add metadata or change options on a notification builder.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Notification.Builder](../android/app/Notification.Builder.md)! | [extend](../android/app/Notification.Extender.md))`(`builder:` ` [Notification.Builder](../android/app/Notification.Builder.md)!`)` Apply this extender to a notification builder. |

## Public methods

### extend

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun extend(builder: Notification.Builder!): Notification.Builder!
```

Apply this extender to a notification builder.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `builder` | [Notification.Builder](../android/app/Notification.Builder.md)!:the builder to be modified |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------|
| [Notification.Builder](../android/app/Notification.Builder.md)! | the build object for chaining |
