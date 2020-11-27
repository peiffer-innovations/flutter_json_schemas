[*description*][description]

# SmartQuotesType enum Null safety #

Indicates how to handle the intelligent replacement of quotes in text input.

See also:

 *  TextField.smartQuotesType
 *  CupertinoTextField.smartQuotesType
 *  EditableText.smartQuotesType
 *  [developer.apple.com/documentation/uikit/uitextinputtraits][developer.apple.com_documentation_uikit_uitextinputtraits]

## Constants ##

disabled → const SmartQuotesType

Smart quotes is disabled.

This corresponds to the ["no" value of UITextSmartQuotesType][no_ value of UITextSmartQuotesType].

`const SmartQuotesType(0)`

enabled → const SmartQuotesType

Smart quotes is enabled.

This corresponds to the ["yes" value of UITextSmartQuotesType][yes_ value of UITextSmartQuotesType].

`const SmartQuotesType(1)`

values → const List<SmartQuotesType>

A constant List of the values in this enum, in order of their declaration.

`const List<SmartQuotesType>`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/services/text_input.dart#L60
[developer.apple.com_documentation_uikit_uitextinputtraits]: https://developer.apple.com/documentation/uikit/uitextinputtraits
[no_ value of UITextSmartQuotesType]: https://developer.apple.com/documentation/uikit/uitextsmartquotestype/no
[yes_ value of UITextSmartQuotesType]: https://developer.apple.com/documentation/uikit/uitextsmartquotestype/yes