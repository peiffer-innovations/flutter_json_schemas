[*description*][description]

# DropdownButtonFormField<T> class #

A convenience widget that makes a DropdownButton into a FormField.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  FormField<T>
 *  DropdownButtonFormField

## Constructors ##

DropdownButtonFormField(\{Key key, @required List<DropdownMenuItem<T>> items, DropdownButtonBuilder selectedItemBuilder, T value, Widget hint, Widget disabledHint, @required ValueChanged<T> onChanged, VoidCallback onTap, int elevation: 8, TextStyle style, Widget icon, Color iconDisabledColor, Color iconEnabledColor, double iconSize: 24.0, bool isDense: true, bool isExpanded: false, double itemHeight, Color focusColor, FocusNode focusNode, bool autofocus: false, Color dropdownColor, InputDecoration decoration, FormFieldSetter<T> onSaved, FormFieldValidator<T> validator, @Deprecated('Use autoValidateMode parameter which provide more specific ' 'behaviour related to auto validation. ' 'This feature was deprecated after v1.19.0.') bool autovalidate: false, AutovalidateMode autovalidateMode\})

Creates a DropdownButton widget that is a FormField, wrapped in an InputDecorator. \[...\]

## Properties ##

autovalidate → bool

Used to enable/disable auto validation and update their error text.

@Deprecated('Use autoValidateMode parameter which provides more specific ' 'behavior related to auto validation. ' 'This feature was deprecated after v1.19.0.'), final, inherited

autovalidateMode → AutovalidateMode

Used to enable/disable this form field auto validation and update its error text. \[...\]

final, inherited

builder → FormFieldBuilder<T>

Function that returns the widget representing this form field. It is passed the form field state as input, containing the current value and validation state of this field.

final, inherited

decoration → InputDecoration

The decoration to show around the dropdown button form field. \[...\]

final

enabled → bool

Whether the form is able to receive user input. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

initialValue → T

An optional value to initialize the form field to, or null otherwise.

final, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onChanged → ValueChanged<T>

Called when the user selects an item. \[...\]

final

onSaved → FormFieldSetter<T>

An optional method to call with the final value when the form is saved via FormState.save.

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

validator → FormFieldValidator<T>

An optional method that validates an input. Returns an error string to display if the input is invalid, or null otherwise. \[...\]

final, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → FormFieldState<T>

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

inherited

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringDeep(\{String prefixLineOne: '', String prefixOtherLines, DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a string representation of this node and its descendants. \[...\]

inherited

toStringShallow(\{String joiner: ', ', DiagnosticLevel minLevel: DiagnosticLevel.debug\}) → String

Returns a one-line detailed description of the object. \[...\]

inherited

toStringShort() → String

A short, textual description of this widget.

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/dropdown.dart#L1436