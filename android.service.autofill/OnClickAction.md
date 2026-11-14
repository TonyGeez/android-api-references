# OnClickAction

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClickAction

Kotlin| [Java](OnClickAction.md) 
| --- | --- |

```
interface OnClickAction
```

| [android.service.autofill.OnClickAction](OnClickAction.md) |

| Known Direct Subclasses [VisibilitySetterAction](VisibilitySetterAction.md) |--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [VisibilitySetterAction](VisibilitySetterAction.md) | Action used to change the visibility of other child view in a [CustomDescription](CustomDescription.md) [presentation template](../android.widget/RemoteViews.md). | |
| --- | --- | --- | --- | --- | --- | --- |

Class used to define an action to be performed when a child view in a [presentation](../android.widget/RemoteViews.md) is clicked.

Typically used to switch the visibility of other views in a [custom save UI](CustomDescription.md).

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary
