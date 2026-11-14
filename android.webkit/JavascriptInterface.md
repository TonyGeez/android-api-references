# JavascriptInterface

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JavascriptInterface

Kotlin| [Java](https://developer.android.com/reference/android/webkit/JavascriptInterface "View this page in Java") 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class JavascriptInterface
```

| [android.webkit.JavascriptInterface](https://developer.android.com/reference/kotlin/android/webkit/JavascriptInterface#) |

Annotation that allows exposing methods to JavaScript. Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int) and above, only methods explicitly marked with this annotation are available to the Javascript code. See [android.webkit.WebView#addJavascriptInterface](https://developer.android.com/reference/kotlin/android/webkit/WebView#addJavascriptInterface(kotlin.Any,%20kotlin.String))for more information about it.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JavascriptInterface](https://developer.android.com/reference/kotlin/android/webkit/JavascriptInterface#JavascriptInterface())`()` Annotation that allows exposing methods to JavaScript. |

## Public constructors

### JavascriptInterface

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JavascriptInterface()
```

Annotation that allows exposing methods to JavaScript. Starting from API level [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int) and above, only methods explicitly marked with this annotation are available to the Javascript code. See [android.webkit.WebView#addJavascriptInterface](https://developer.android.com/reference/kotlin/android/webkit/WebView#addJavascriptInterface(kotlin.Any,%20kotlin.String))for more information about it.
