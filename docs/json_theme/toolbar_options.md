[*description*][description]

# ToolbarOptions class #

Toolbar configuration for EditableText.

Toolbar is a context menu that will show up when user right click or long press the EditableText. It includes several options: cut, copy, paste, and select all.

EditableText and its derived widgets have their own default ToolbarOptions. Create a custom ToolbarOptions if you want explicit control over the toolbar option.

## Constructors ##

ToolbarOptions(\{bool copy: false, bool cut: false, bool paste: false, bool selectAll: false\})

Create a toolbar configuration with given options. \[...\]

const

## Properties ##

copy → bool

Whether to show copy option in toolbar. \[...\]

final

cut → bool

Whether to show cut option in toolbar. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

paste → bool

Whether to show paste option in toolbar. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

selectAll → bool

Whether to show select all option in toolbar. \[...\]

final

## Methods ##

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toString() → String

Returns a string representation of this object.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/editable_text.dart#L267