# android.text

# android.text

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [Editable](Editable.md) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). |
| --- | --- |
| [GetChars](GetChars.md) | Please implement this interface if your CharSequence has a getChars() method like the one in String that is faster than calling charAt() multiple times. |
| [ImageGetter](../android/text/Html.ImageGetter.md) | Retrieves images for HTML \<img\> tags. |
| [TagHandler](../android/text/Html.TagHandler.md) | Is notified when HTML tags are encountered that the parser does not know how to interpret. |
| --- | --- |
| [InputFilter](InputFilter.md) | InputFilters can be attached to [Editable](Editable.md) s to constrain the changes that can be made to them. |
| [InputType](InputType.md) | Bit definitions for an integer defining the basic content type of text held in an [Editable](Editable.md) object. |
| [TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md) | Strategy for determining whether a text segment is inside a rectangle area. |
| --- | --- |
| [NoCopySpan](NoCopySpan.md) | This interface should be added to a span object that should not be copied into a new Spanned when performing a slice or copy operation on the original Spanned it was placed in. |
| [ParcelableSpan](ParcelableSpan.md) | A special kind of Parcelable for objects that will serve as text spans. |
| [Spannable](Spannable.md) | This is the interface for text to which markup objects can be attached and detached. |
| --- | --- |
| [Spanned](Spanned.md) | This is the interface for text that has markup objects attached to ranges of it. |
| [SpanWatcher](SpanWatcher.md) | When an object of this type is attached to a Spannable, its methods will be called to notify it that other markup objects have been added, changed, or removed. |
| [TextDirectionHeuristic](TextDirectionHeuristic.md) | Interface for objects that use a heuristic for guessing at the paragraph direction by examining text. |
| --- | --- |
| [GlyphsConsumer](../android/text/TextShaper.GlyphsConsumer.md) | A consumer interface for accepting text shape result. |
| [EllipsizeCallback](../android/text/TextUtils.EllipsizeCallback.md) | <br /> |
| [StringSplitter](../android/text/TextUtils.StringSplitter.md) | An interface for splitting strings according to rules that are opaque to the user of this interface. |
| --- | --- |
| [TextWatcher](TextWatcher.md) | When an object of this type is attached to an Editable, its methods will be called when the text is changed. |

## Classes

| [AlteredCharSequence](AlteredCharSequence.md) | An AlteredCharSequence is a CharSequence that is largely mirrored from another CharSequence, except that a specified range of characters are mirrored from a different char array instead. |
| --- | --- |
| [AndroidCharacter](AndroidCharacter.md) | AndroidCharacter exposes some character properties that used to be not easily accessed from java. |
| [Annotation](Annotation.md) | Annotations are simple key-value pairs that are preserved across TextView save/restore cycles and can be used to keep application-specific data that needs to be maintained for regions of text. |
| [AutoText](AutoText.md) | This class accesses a dictionary of corrections to frequent misspellings. |
| --- | --- |
| [BidiFormatter](BidiFormatter.md) | Utility class for formatting text for display in a potentially opposite-directionality context without garbling. |
| [BoringLayout](BoringLayout.md) | A BoringLayout is a very simple Layout implementation for text that fits on a single line and is all left-to-right characters. |
| [ClipboardManager](ClipboardManager.md) | <br /> |
| --- | --- |
| [DynamicLayout](DynamicLayout.md) | DynamicLayout is a text layout that updates itself as the text is edited. |
| [EmojiConsistency](EmojiConsistency.md) | The set of emoji that should be drawn by the system with the default font for device consistency. |
| [GraphemeClusterSegmentFinder](GraphemeClusterSegmentFinder.md) | Implementation of`SegmentFinder`using grapheme clusters as the text segment. |
| --- | --- |
| [Highlights](Highlights.md) | A class that represents of the highlight of the text. |
| [Html](Html.md) | This class processes HTML strings into displayable styled text. |
| [Layout](Layout.md) | A base class that manages text layout in visual elements on the screen. |
| --- | --- |
| [LoginFilter](LoginFilter.md) | Abstract class for filtering login-related text (user names and passwords) |
| [PrecomputedText](PrecomputedText.md) | A text which has the character metrics data. |
| [SegmentFinder](SegmentFinder.md) | Finds text segment boundaries within text. |
| --- | --- |
| [Selection](Selection.md) | Utility class for manipulating cursors and selections in CharSequences. |
| [SpannableString](SpannableString.md) | This is the class for text whose content is immutable but to which markup objects can be attached and detached. |
| [SpannableStringBuilder](SpannableStringBuilder.md) | This is the class for text whose content and markup can both be changed. |
| --- | --- |
| [SpannedString](SpannedString.md) | This is the class for text whose content and markup are immutable. |
| [StaticLayout](StaticLayout.md) | StaticLayout is a Layout for text that will not be edited after it is laid out. |
| [TextDirectionHeuristics](TextDirectionHeuristics.md) | Some objects that implement [TextDirectionHeuristic](TextDirectionHeuristic.md). |
| --- | --- |
| [TextPaint](TextPaint.md) | TextPaint is an extension of Paint that leaves room for some extra data used during text measuring and drawing. |
| [TextShaper](TextShaper.md) | Provides text shaping for multi-styled text. |
| [TextUtils](TextUtils.md) | <br /> |
| --- | --- |
| [WordSegmentFinder](WordSegmentFinder.md) | Implementation of [SegmentFinder](SegmentFinder.md) using words as the text segment. |
