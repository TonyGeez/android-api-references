# RecognizerResultsIntent

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognizerResultsIntent

Kotlin | [Java](https://developer.android.com/reference/android/speech/RecognizerResultsIntent "View this page in Java") 

```
open class RecognizerResultsIntent
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.speech.RecognizerResultsIntent](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#) |

Constants for intents related to showing speech recognition results. These constants should not be needed for normal utilization of speech recognition. They would only be called if you wanted to trigger a view of voice search results in your application, or implemented if you wanted to offer a different view for voice search results with your application. The standard behavior here for someone receiving an [ACTION_VOICE_SEARCH_RESULTS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#ACTION_VOICE_SEARCH_RESULTS:kotlin.String) is to first retrieve the list of [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String), and use any provided HTML for that result in [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String), if available, to display the search results. If that is not available, then the corresponding url for that result in [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String) should be used. And if even that is not available, then a search url should be constructed from the actual recognition result string.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_VOICE_SEARCH_RESULTS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#ACTION_VOICE_SEARCH_RESULTS:kotlin.String) Intent that can be sent by implementations of voice search to display the results of a search in, for example, a web browser. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String) The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the html content to use, if available, for the recognition alternates provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS:kotlin.String) The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the base url to assume when interpreting html provided in [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOICE_SEARCH_RESULT_HTTP_HEADERS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTTP_HEADERS:kotlin.String) The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) s that contains key/value pairs. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the list of recognition alternates from voice search, in order from highest to lowest confidence. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String) The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the search urls to use, if available, for the recognition alternates provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [URI_SCHEME_INLINE](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#URI_SCHEME_INLINE:kotlin.String) The scheme used currently for html content in [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String). |

## Constants

### ACTION_VOICE_SEARCH_RESULTS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_VOICE_SEARCH_RESULTS: String
```

Intent that can be sent by implementations of voice search to display the results of a search in, for example, a web browser. This intent should always be accompanied by at least [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String), and optionally but recommended, [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String), and sometimes [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String) and [EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS:kotlin.String). These are parallel arrays, where a recognition result string at index N of [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) should be accompanied by a url to use for searching based on that string at index N of [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String), and, possibly, the full html to display for that result at index N of [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String). If full html is provided, a base url (or list of base urls) should be provided with [EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS:kotlin.String). 

 Value: "android.speech.action.VOICE_SEARCH_RESULTS"

### EXTRA_VOICE_SEARCH_RESULT_HTML

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOICE_SEARCH_RESULT_HTML: String
```

The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the html content to use, if available, for the recognition alternates provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String). This list should always be the same size as the one provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) - if a result cannot provide html, that entry in this list should be `null`, and the implementor of [ACTION_VOICE_SEARCH_RESULTS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#ACTION_VOICE_SEARCH_RESULTS:kotlin.String) should back off to the corresponding url provided in [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String), if available, or else should execute a search of its own choosing, based on the recognition result string. Currently this html content should be expected in the form of a uri with scheme [URI_SCHEME_INLINE](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#URI_SCHEME_INLINE:kotlin.String) for the Browser. In the future this may change to a "content://" uri or some other identifier. Anyone who reads this extra should confirm that a result is in fact an "inline:" uri and back off to the urls or strings gracefully if it is not, thus maintaining future backwards compatibility if this changes. 

 Value: "android.speech.extras.VOICE_SEARCH_RESULT_HTML"

### EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOICE_SEARCH_RESULT_HTML_BASE_URLS: String
```

The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the base url to assume when interpreting html provided in [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String). A list of size 1 may be provided to apply the same base url to all html results. A list of the same size as [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) may be provided to apply different base urls to each different html result in the [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String) list. 

 Value: "android.speech.extras.VOICE_SEARCH_RESULT_HTML_BASE_URLS"

### EXTRA_VOICE_SEARCH_RESULT_HTTP_HEADERS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOICE_SEARCH_RESULT_HTTP_HEADERS: String
```

The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) s that contains key/value pairs. All the values and the keys are [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s. Each key/value pair represents an extra HTTP header. The keys can't be the standard HTTP headers as they are set by the WebView. A list of size 1 may be provided to apply the same HTTP headers to all web results. A list of the same size as [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) may be provided to apply different HTTP headers to each different web result in the list. These headers will only be used in the case that the url for a particular web result (from [EXTRA_VOICE_SEARCH_RESULT_URLS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_URLS:kotlin.String)) is loaded. 

 Value: "android.speech.extras.EXTRA_VOICE_SEARCH_RESULT_HTTP_HEADERS"

### EXTRA_VOICE_SEARCH_RESULT_STRINGS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOICE_SEARCH_RESULT_STRINGS: String
```

The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the list of recognition alternates from voice search, in order from highest to lowest confidence. 

 Value: "android.speech.extras.VOICE_SEARCH_RESULT_STRINGS"

### EXTRA_VOICE_SEARCH_RESULT_URLS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_VOICE_SEARCH_RESULT_URLS: String
```

The key to an extra [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#) of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) s that contains the search urls to use, if available, for the recognition alternates provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String). This list should always be the same size as the one provided in [EXTRA_VOICE_SEARCH_RESULT_STRINGS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_STRINGS:kotlin.String) - if a result cannot provide a search url, that entry in this ArrayList should be `null`, and the implementor of [ACTION_VOICE_SEARCH_RESULTS](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#ACTION_VOICE_SEARCH_RESULTS:kotlin.String) should execute a search of its own choosing, based on the recognition result string. 

 Value: "android.speech.extras.VOICE_SEARCH_RESULT_URLS"

### URI_SCHEME_INLINE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val URI_SCHEME_INLINE: String
```

The scheme used currently for html content in [EXTRA_VOICE_SEARCH_RESULT_HTML](https://developer.android.com/reference/kotlin/android/speech/RecognizerResultsIntent#EXTRA_VOICE_SEARCH_RESULT_HTML:kotlin.String). Note that this should only be used in tandem with this particular extra; it should NOT be used for generic URIs such as those found in the data field of an Intent. 

 Value: "inline"
