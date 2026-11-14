# android.text

# android.text

Kotlin| [Java](https://developer.android.com/reference/android/text/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). |
| --- | --- |
| [GetChars](https://developer.android.com/reference/kotlin/android/text/GetChars) | Please implement this interface if your CharSequence has a getChars() method like the one in String that is faster than calling charAt() multiple times. |
| [ImageGetter](https://developer.android.com/reference/kotlin/android/text/Html.ImageGetter) | Retrieves images for HTML \<img\> tags. |
| [TagHandler](https://developer.android.com/reference/kotlin/android/text/Html.TagHandler) | Is notified when HTML tags are encountered that the parser does not know how to interpret. |
| --- | --- |
| [InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter) | InputFilters can be attached to [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) s to constrain the changes that can be made to them. |
| [InputType](https://developer.android.com/reference/kotlin/android/text/InputType) | Bit definitions for an integer defining the basic content type of text held in an [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) object. |
| [TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy) | Strategy for determining whether a text segment is inside a rectangle area. |
| --- | --- |
| [NoCopySpan](https://developer.android.com/reference/kotlin/android/text/NoCopySpan) | This interface should be added to a span object that should not be copied into a new Spanned when performing a slice or copy operation on the original Spanned it was placed in. |
| [ParcelableSpan](https://developer.android.com/reference/kotlin/android/text/ParcelableSpan) | A special kind of Parcelable for objects that will serve as text spans. |
| [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable) | This is the interface for text to which markup objects can be attached and detached. |
| --- | --- |
| [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) | This is the interface for text that has markup objects attached to ranges of it. |
| [SpanWatcher](https://developer.android.com/reference/kotlin/android/text/SpanWatcher) | When an object of this type is attached to a Spannable, its methods will be called to notify it that other markup objects have been added, changed, or removed. |
| [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic) | Interface for objects that use a heuristic for guessing at the paragraph direction by examining text. |
| --- | --- |
| [GlyphsConsumer](https://developer.android.com/reference/kotlin/android/text/TextShaper.GlyphsConsumer) | A consumer interface for accepting text shape result. |
| [EllipsizeCallback](https://developer.android.com/reference/kotlin/android/text/TextUtils.EllipsizeCallback) | <br /> |
| [StringSplitter](https://developer.android.com/reference/kotlin/android/text/TextUtils.StringSplitter) | An interface for splitting strings according to rules that are opaque to the user of this interface. |
| --- | --- |
| [TextWatcher](https://developer.android.com/reference/kotlin/android/text/TextWatcher) | When an object of this type is attached to an Editable, its methods will be called when the text is changed. |

## Classes

| [AlteredCharSequence](https://developer.android.com/reference/kotlin/android/text/AlteredCharSequence) | An AlteredCharSequence is a CharSequence that is largely mirrored from another CharSequence, except that a specified range of characters are mirrored from a different char array instead. |
| --- | --- |
| [AndroidCharacter](https://developer.android.com/reference/kotlin/android/text/AndroidCharacter) | AndroidCharacter exposes some character properties that used to be not easily accessed from java. |
| [Annotation](https://developer.android.com/reference/kotlin/android/text/Annotation) | Annotations are simple key-value pairs that are preserved across TextView save/restore cycles and can be used to keep application-specific data that needs to be maintained for regions of text. |
| [AutoText](https://developer.android.com/reference/kotlin/android/text/AutoText) | This class accesses a dictionary of corrections to frequent misspellings. |
| --- | --- |
| [BidiFormatter](https://developer.android.com/reference/kotlin/android/text/BidiFormatter) | Utility class for formatting text for display in a potentially opposite-directionality context without garbling. |
| [BoringLayout](https://developer.android.com/reference/kotlin/android/text/BoringLayout) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. |
| [ClipboardManager](https://developer.android.com/reference/kotlin/android/text/ClipboardManager) | <br /> |
| --- | --- |
| [DynamicLayout](https://developer.android.com/reference/kotlin/android/text/DynamicLayout) | DynamicLayout is a text layout that updates itself as the text is edited. |
| [EmojiConsistency](https://developer.android.com/reference/kotlin/android/text/EmojiConsistency) | The set of emoji that should be drawn by the system with the default font for device consistency. |
| [GraphemeClusterSegmentFinder](https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder) | Implementation of`SegmentFinder`using grapheme clusters as the text segment. |
| --- | --- |
| [Highlights](https://developer.android.com/reference/kotlin/android/text/Highlights) | A class that represents of the highlight of the text. |
| [Html](https://developer.android.com/reference/kotlin/android/text/Html) | This class processes HTML strings into displayable styled text. |
| [Layout](https://developer.android.com/reference/kotlin/android/text/Layout) | A base class that manages text layout in visual elements on the screen. |
| --- | --- |
| [LoginFilter](https://developer.android.com/reference/kotlin/android/text/LoginFilter) | Abstract class for filtering login-related text (user names and passwords) |
| [PrecomputedText](https://developer.android.com/reference/kotlin/android/text/PrecomputedText) | A text which has the character metrics data. |
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) | Finds text segment boundaries within text. |
| --- | --- |
| [Selection](https://developer.android.com/reference/kotlin/android/text/Selection) | Utility class for manipulating cursors and selections in CharSequences. |
| [SpannableString](https://developer.android.com/reference/kotlin/android/text/SpannableString) | This is the class for text whose content is immutable but to which markup objects can be attached and detached. |
| [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. |
| --- | --- |
| [SpannedString](https://developer.android.com/reference/kotlin/android/text/SpannedString) | This is the class for text whose content and markup are immutable. |
| [StaticLayout](https://developer.android.com/reference/kotlin/android/text/StaticLayout) | StaticLayout is a Layout for text that will not be edited after it is laid out. |
| [TextDirectionHeuristics](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristics) | Some objects that implement [TextDirectionHeuristic](https://developer.android.com/reference/kotlin/android/text/TextDirectionHeuristic). |
| --- | --- |
| [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint) | TextPaint is an extension of Paint that leaves room for some extra data used during text measuring and drawing. |
| [TextShaper](https://developer.android.com/reference/kotlin/android/text/TextShaper) | Provides text shaping for multi-styled text. |
| [TextUtils](https://developer.android.com/reference/kotlin/android/text/TextUtils) | <br /> |
| --- | --- |
| [WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder) | Implementation of [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) using words as the text segment. |
