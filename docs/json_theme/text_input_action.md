[*description*][description]

# TextInputAction enum Null safety #

An action the user has requested the text input control to perform.

Each action represents a logical meaning, and also configures the soft keyboard to display a certain kind of action button. The visual appearance of the action button might differ between versions of the same OS.

Despite the logical meaning of each action, choosing a particular TextInputAction does not necessarily cause any specific behavior to happen. It is up to the developer to ensure that the behavior that occurs when an action button is pressed is appropriate for the action button chosen.

For example: If the user presses the keyboard action button on iOS when it reads "Emergency Call", the result should not be a focus change to the next TextField. This behavior is not logically appropriate for a button that says "Emergency Call".

See EditableText for more information about customizing action button behavior.

Most TextInputActions are supported equally by both Android and iOS. However, there is not a complete, direct mapping between Android's IME input types and iOS's keyboard return types. Therefore, some TextInputActions are inappropriate for one of the platforms. If a developer chooses an inappropriate TextInputAction when running in debug mode, an error will be thrown. If the same thing is done in release mode, then instead of sending the inappropriate value, Android will use "unspecified" on the platform side and iOS will use "default" on the platform side.

See also:

 *  TextInput, which configures the platform's keyboard setup.
 *  EditableText, which invokes callbacks when the action button is pressed.

## Constants ##

continueAction → const TextInputAction

Logical meaning: In iOS apps, it is common for a "Back" button and "Continue" button to appear at the top of the screen. However, when the keyboard is open, these buttons are often hidden off-screen. Therefore, the purpose of the "Continue" return key on iOS is to make the "Continue" button available when the user is entering text.

Historical context aside, TextInputAction.continueAction can be used any time that the term "Continue" seems most appropriate for the given action.

Android: Android does not have an IME input type of "continue." It is inappropriate to choose this TextInputAction when running on Android.

iOS: Corresponds to iOS's "UIReturnKeyContinue". The title displayed in the action button is "Continue". This action is only available on iOS 9.0+.

The reason that this value has "Action" post-fixed to it is because "continue" is a reserved word in Dart, as well as many other languages.

`const TextInputAction(8)`

done → const TextInputAction

Logical meaning: The user is done providing input to a group of inputs (like a form). Some kind of finalization behavior should now take place.

Android: Corresponds to Android's "IME\_ACTION\_DONE". The OS displays a button that represents completion, e.g., a checkmark button.

iOS: Corresponds to iOS's "UIReturnKeyDone". The title displayed in the action button is "Done".

`const TextInputAction(2)`

emergencyCall → const TextInputAction

Logical meaning: Initiate a call to emergency services.

Android: Android does not have an IME input type of "emergencyCall." It is inappropriate to choose this TextInputAction when running on Android.

iOS: Corresponds to iOS's "UIReturnKeyEmergencyCall". The title displayed in the action button is "Emergency Call".

`const TextInputAction(11)`

go → const TextInputAction

Logical meaning: The user has entered some text that represents a destination, e.g., a restaurant name. The "go" button is intended to take the user to a part of the app that corresponds to this destination.

Android: Corresponds to Android's "IME\_ACTION\_GO". The OS displays a button that represents taking "the user to the target of the text they typed", e.g., a right-facing arrow button.

iOS: Corresponds to iOS's "UIReturnKeyGo". The title displayed in the action button is "Go".

`const TextInputAction(3)`

join → const TextInputAction

Logical meaning: The user wants to join something, e.g., a wireless network.

Android: Android does not have an IME input type of "join." It is inappropriate to choose this TextInputAction when running on Android.

iOS: Corresponds to iOS's "UIReturnKeyJoin". The title displayed in the action button is "Join".

`const TextInputAction(9)`

newline → const TextInputAction

Logical meaning: Insert a newline character in the focused text input, e.g., TextField.

Android: Corresponds to Android's "IME\_ACTION\_NONE". The OS displays a button that represents a new line, e.g., a carriage return button.

iOS: Corresponds to iOS's "UIReturnKeyDefault". The title displayed in the action button is "return".

The term TextInputAction.newline exists in Flutter but not in Android or iOS. The reason for introducing this term is so that developers can achieve the common result of inserting new lines without needing to understand the various IME actions on Android and return keys on iOS. Thus, TextInputAction.newline is a convenience term that alleviates the need to understand the underlying platforms to achieve this common behavior.

`const TextInputAction(12)`

next → const TextInputAction

Logical meaning: The user is done with the current input source and wants to move to the next one.

Android: Corresponds to Android's "IME\_ACTION\_NEXT". The OS displays a button that represents moving forward, e.g., a right-facing arrow button.

iOS: Corresponds to iOS's "UIReturnKeyNext". The title displayed in the action button is "Next".

`const TextInputAction(6)`

none → const TextInputAction

Logical meaning: There is no relevant input action for the current input source, e.g., TextField.

Android: Corresponds to Android's "IME\_ACTION\_NONE". The keyboard setup is decided by the OS. The keyboard will likely show a return key.

iOS: iOS does not have a keyboard return type of "none." It is inappropriate to choose this TextInputAction when running on iOS.

`const TextInputAction(0)`

previous → const TextInputAction

Logical meaning: The user wishes to return to the previous input source in the group, e.g., a form with multiple TextFields.

Android: Corresponds to Android's "IME\_ACTION\_PREVIOUS". The OS displays a button that represents moving backward, e.g., a left-facing arrow button.

iOS: iOS does not have a keyboard return type of "previous." It is inappropriate to choose this TextInputAction when running on iOS.

`const TextInputAction(7)`

route → const TextInputAction

Logical meaning: The user wants routing options, e.g., driving directions.

Android: Android does not have an IME input type of "route." It is inappropriate to choose this TextInputAction when running on Android.

iOS: Corresponds to iOS's "UIReturnKeyRoute". The title displayed in the action button is "Route".

`const TextInputAction(10)`

search → const TextInputAction

Logical meaning: Execute a search query.

Android: Corresponds to Android's "IME\_ACTION\_SEARCH". The OS displays a button that represents a search, e.g., a magnifying glass button.

iOS: Corresponds to iOS's "UIReturnKeySearch". The title displayed in the action button is "Search".

`const TextInputAction(4)`

send → const TextInputAction

Logical meaning: Sends something that the user has composed, e.g., an email or a text message.

Android: Corresponds to Android's "IME\_ACTION\_SEND". The OS displays a button that represents sending something, e.g., a paper plane button.

iOS: Corresponds to iOS's "UIReturnKeySend". The title displayed in the action button is "Send".

`const TextInputAction(5)`

unspecified → const TextInputAction

Logical meaning: Let the OS decide which action is most appropriate.

Android: Corresponds to Android's "IME\_ACTION\_UNSPECIFIED". The OS chooses which keyboard action to display. The decision will likely be a done button or a return key.

iOS: Corresponds to iOS's "UIReturnKeyDefault". The title displayed in the action button is "return".

`const TextInputAction(1)`

values → const List<TextInputAction>

A constant List of the values in this enum, in order of their declaration.

`const List<TextInputAction>`

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

index → int

The integer index of this enum.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/services/text_input.dart#L251