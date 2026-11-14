# android.service.autofill

Kotlin | [Java](https://developer.android.com/reference/android/service/autofill/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [OnClickAction](https://developer.android.com/reference/kotlin/android/service/autofill/OnClickAction) | Class used to define an action to be performed when a child view in a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` is clicked. |
| --- | --- |
| [Sanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/Sanitizer) | Helper class used to sanitize user input before using it in a save request. |
| [SavedDatasetsInfoCallback](https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback) | Handles the response to `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSavedDatasetsInfoRequest(android.service.autofill.SavedDatasetsInfoCallback)`. |
| [Transformation](https://developer.android.com/reference/kotlin/android/service/autofill/Transformation) | Helper class used to change a child view of a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` at runtime, using the values of fields contained in the screen. |
| --- | --- |
| [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | Class used to define whether a condition is satisfied. |

## Classes

| [AutofillService](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) | An `AutofillService` is a service used to automatically fill the contents of the screen on behalf of a given user - for more information about autofill, read [Autofill Framework](https://developer.android.com/preview/features/autofill.html). |
| --- | --- |
| [BatchUpdates](https://developer.android.com/reference/kotlin/android/service/autofill/BatchUpdates) | Defines actions to be applied to a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`. |
| [CharSequenceTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/CharSequenceTransformation) | Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` with the contents of one or more regular expressions (regexs). |
| [CustomDescription](https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription) | Defines a custom description for the autofill save UI. |
| --- | --- |
| [Dataset](https://developer.android.com/reference/kotlin/android/service/autofill/Dataset) | A `Dataset` object represents a group of fields (key / value pairs) used to autofill parts of a screen. |
| [DateTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/DateTransformation) | Replaces a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` child of a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` with the contents of a field that is expected to have a `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#forDate(kotlin.Long)`. |
| [DateValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/DateValueSanitizer) | Sanitizes a date `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#`. |
| --- | --- |
| [Field](https://developer.android.com/reference/kotlin/android/service/autofill/Field) | This class is used to set all information of a field. |
| [FieldClassification](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification) | Represents the [field classification](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#FieldClassification) results for a given field. |
| [FillCallback](https://developer.android.com/reference/kotlin/android/service/autofill/FillCallback) | `FillCallback` handles autofill requests from the `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` into the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` being autofilled. |
| --- | --- |
| [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext) | This class represents a context for each fill request made via `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)`. |
| [FillEventHistory](https://developer.android.com/reference/kotlin/android/service/autofill/FillEventHistory) | Describes what happened after the last `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)` call. |
| [FillRequest](https://developer.android.com/reference/kotlin/android/service/autofill/FillRequest) | This class represents a request to an autofill service to interpret the screen and provide information to the system which views are interesting for saving and what are the possible ways to fill the inputs on the screen if applicable. |
| --- | --- |
| [FillResponse](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse) | Response for an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onFillRequest(android.service.autofill.FillRequest,%20android.os.CancellationSignal,%20android.service.autofill.FillCallback)`. |
| [ImageTransformation](https://developer.android.com/reference/kotlin/android/service/autofill/ImageTransformation) | Replaces the content of a child `https://developer.android.com/reference/kotlin/android/widget/ImageView.html#` of a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` with the first image that matches a regular expression (regex). |
| [InlinePresentation](https://developer.android.com/reference/kotlin/android/service/autofill/InlinePresentation) | Wrapper class holding a `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#` and an `https://developer.android.com/reference/kotlin/android/widget/inline/InlinePresentationSpec.html#` for rendering UI for an Inline Suggestion. |
| --- | --- |
| [LuhnChecksumValidator](https://developer.android.com/reference/kotlin/android/service/autofill/LuhnChecksumValidator) | Validator that returns `true` if the number created by concatenating all given fields pass a Luhn algorithm checksum. |
| [Presentations](https://developer.android.com/reference/kotlin/android/service/autofill/Presentations) | Holds presentations used to visualize autofill suggestions for each available UI type. |
| [RegexValidator](https://developer.android.com/reference/kotlin/android/service/autofill/RegexValidator) | Defines if a field is valid based on a regular expression (regex). |
| --- | --- |
| [SaveCallback](https://developer.android.com/reference/kotlin/android/service/autofill/SaveCallback) | Handles save requests from the `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` into the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` being autofilled. |
| [SavedDatasetsInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfo) | A result returned from `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSavedDatasetsInfoRequest(android.service.autofill.SavedDatasetsInfoCallback)`. |
| [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo) | Information used to indicate that an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` is interested on saving the user-inputed data for future use, through a `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#onSaveRequest(android.service.autofill.SaveRequest,%20android.service.autofill.SaveCallback)` call. |
| --- | --- |
| [SaveRequest](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest) | This class represents a request to an `https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService` to save applicable data entered by the user. |
| [TextValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/TextValueSanitizer) | Sanitizes a text `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#` using a regular expression (regex) substitution. |
| [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData) | Defines the user data used for [field classification](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#FieldClassification). |
| --- | --- |
| [Validators](https://developer.android.com/reference/kotlin/android/service/autofill/Validators) | Factory for `https://developer.android.com/reference/kotlin/android/service/autofill/Validator` operations. |
| [VisibilitySetterAction](https://developer.android.com/reference/kotlin/android/service/autofill/VisibilitySetterAction) | Action used to change the visibility of other child view in a `https://developer.android.com/reference/kotlin/android/service/autofill/CustomDescription` `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#`. |
