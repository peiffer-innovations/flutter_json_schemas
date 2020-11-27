[*description*][description]

# TextInputType class Null safety #

The type of information for which to optimize the text input control.

On Android, behavior may vary across device and keyboard provider.

This class stays as close to `Enum` interface as possible, and allows for additional flags for some input types. For example, numeric input can specify whether it supports decimal numbers and/or signed numbers.

Annotations

 *  @immutable

## Constructors ##

TextInputType.numberWithOptions(\{bool? signed: false, bool? decimal: false\})

Optimize for numerical information. \[...\]

const

## Properties ##

decimal → bool?

The number is decimal, allowing a decimal point to provide fractional. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

index → int

Enum value index, corresponds to one of the values.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

signed → bool?

The number is signed, allowing a positive or negative sign at the start. \[...\]

final

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toJson() → Map<String, dynamic>

Returns a representation of this object as a JSON object.

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override

## Constants ##

datetime → const TextInputType

Optimize for date and time information. \[...\]

`TextInputType._(4)`

emailAddress → const TextInputType

Optimize for email addresses. \[...\]

`TextInputType._(5)`

multiline → const TextInputType

Optimize for multiline textual information. \[...\]

`TextInputType._(1)`

name → const TextInputType

Optimized for a person's name. \[...\]

`TextInputType._(8)`

number → const TextInputType

Optimize for unsigned numerical information without a decimal point. \[...\]

`TextInputType.numberWithOptions()`

phone → const TextInputType

Optimize for telephone numbers. \[...\]

`TextInputType._(3)`

streetAddress → const TextInputType

Optimized for postal mailing addresses. \[...\]

`TextInputType._(9)`

text → const TextInputType

Optimize for textual information. \[...\]

`TextInputType._(0)`

url → const TextInputType

Optimize for URLs. \[...\]

`TextInputType._(6)`

values → const List<TextInputType>

All possible enum values.

`<TextInputType>[text, multiline, number, phone, datetime, emailAddress, url, visiblePassword, name, streetAddress]`

visiblePassword → const TextInputType

Optimize for passwords that are visible to the user. \[...\]

`TextInputType._(7)`


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/services/text_input.dart#L82