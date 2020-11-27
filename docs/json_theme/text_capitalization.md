[*description*][description]

# TextCapitalization enum Null safety #

Configures how the platform keyboard will select an uppercase or lowercase keyboard.

Only supports text keyboards, other keyboard types will ignore this configuration. Capitalization is locale-aware.

## Constants ##

characters → const TextCapitalization

Defaults to an uppercase keyboard for each character.

Corresponds to `InputType.TYPE_TEXT_FLAG_CAP_CHARACTERS` on Android, and `UITextAutocapitalizationTypeAllCharacters` on iOS.

`const TextCapitalization(2)`

none → const TextCapitalization

Defaults to a lowercase keyboard.

`const TextCapitalization(3)`

sentences → const TextCapitalization

Defaults to an uppercase keyboard for the first letter of each sentence.

Corresponds to `InputType.TYPE_TEXT_FLAG_CAP_SENTENCES` on Android, and `UITextAutocapitalizationTypeSentences` on iOS.

`const TextCapitalization(1)`

values → const List<TextCapitalization>

A constant List of the values in this enum, in order of their declaration.

`const List<TextCapitalization>`

words → const TextCapitalization

Defaults to an uppercase keyboard for the first letter of each word.

Corresponds to `InputType.TYPE_TEXT_FLAG_CAP_WORDS` on Android, and `UITextAutocapitalizationTypeWords` on iOS.

`const TextCapitalization(0)`

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/services/text_input.dart#L403