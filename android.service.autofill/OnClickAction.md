# OnClickAction

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClickAction

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/OnClickAction "View this page in Java") 
| --- | --- |

```
interface OnClickAction
```

| [android.service.autofill.OnClickAction](https://developer.android.com/reference/kotlin/android/service/autofill/OnClickAction#) |

| Known Direct Subclasses [VisibilitySetterAction](https://developer.android.com/reference/kotlin/android/service/autofill/VisibilitySetterAction) |--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [VisibilitySetterAction](https://developer.android.com/reference/kotlin/android/service/autofill/VisibilitySetterAction) | Action used to change the visibility of other child view in a [CustomDescription](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription) [presentation template](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#). | |
| --- | --- | --- | --- | --- | --- | --- |

Class used to define an action to be performed when a child view in a [presentation](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) is clicked.

Typically used to switch the visibility of other views in a [custom save UI](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription).

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary
