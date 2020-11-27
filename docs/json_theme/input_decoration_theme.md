[*description*][description]

# InputDecorationTheme class #

Defines the default appearance of InputDecorators.

This class is used to define the value of ThemeData.inputDecorationTheme. The InputDecorator, TextField, and TextFormField widgets use the current input decoration theme to initialize null InputDecoration properties.

The InputDecoration.applyDefaults method is used to combine a input decoration theme with an InputDecoration object.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

InputDecorationTheme(\{TextStyle labelStyle, TextStyle helperStyle, int helperMaxLines, TextStyle hintStyle, TextStyle errorStyle, int errorMaxLines, @Deprecated('Use floatingLabelBehavior instead. ' 'This feature was deprecated after v1.13.2.') bool hasFloatingPlaceholder: true, FloatingLabelBehavior floatingLabelBehavior: FloatingLabelBehavior.auto, bool isDense: false, EdgeInsetsGeometry contentPadding, bool isCollapsed: false, TextStyle prefixStyle, TextStyle suffixStyle, TextStyle counterStyle, bool filled: false, Color fillColor, Color focusColor, Color hoverColor, InputBorder errorBorder, InputBorder focusedBorder, InputBorder focusedErrorBorder, InputBorder disabledBorder, InputBorder enabledBorder, InputBorder border, bool alignLabelWithHint: false\})

Creates a value for ThemeData.inputDecorationTheme that defines default values for InputDecorator. \[...\]

const

## Properties ##

alignLabelWithHint → bool

Typically set to true when the InputDecorator contains a multiline TextField (TextField.maxLines is null or > 1) to override the default behavior of aligning the label with the center of the TextField.

final

border → InputBorder

The shape of the border to draw around the decoration's container. \[...\]

final

contentPadding → EdgeInsetsGeometry

The padding for the input decoration's container. \[...\]

final

counterStyle → TextStyle

The style to use for the InputDecoration.counterText. \[...\]

final

disabledBorder → InputBorder

The border to display when the InputDecorator is disabled and is not showing an error. \[...\]

final

enabledBorder → InputBorder

The border to display when the InputDecorator is enabled and is not showing an error. \[...\]

final

errorBorder → InputBorder

The border to display when the InputDecorator does not have the focus and is showing an error. \[...\]

final

errorMaxLines → int

The maximum number of lines the InputDecoration.errorText can occupy. \[...\]

final

errorStyle → TextStyle

The style to use for the InputDecoration.errorText. \[...\]

final

fillColor → Color

The color to fill the decoration's container with, if filled is true. \[...\]

final

filled → bool

If true the decoration's container is filled with fillColor. \[...\]

final

floatingLabelBehavior → FloatingLabelBehavior

Defines how the floating label should be displayed. \[...\]

final

focusColor → Color

The color to blend with the decoration's fillColor with, if filled is true and the container has the input focus. \[...\]

final

focusedBorder → InputBorder

The border to display when the InputDecorator has the focus and is not showing an error. \[...\]

final

focusedErrorBorder → InputBorder

The border to display when the InputDecorator has the focus and is showing an error. \[...\]

final

hasFloatingPlaceholder → bool

Whether the placeholder text floats to become a label on focus. \[...\]

@Deprecated('Use floatingLabelBehavior instead. ' 'This feature was deprecated after v1.13.2.'), final

hashCode → int

The hash code for this object. \[...\]

read-only, override

helperMaxLines → int

The maximum number of lines the InputDecoration.helperText can occupy. \[...\]

final

helperStyle → TextStyle

The style to use for InputDecoration.helperText.

final

hintStyle → TextStyle

The style to use for the InputDecoration.hintText. \[...\]

final

hoverColor → Color

The color to blend with the decoration's fillColor with, if the decoration is being hovered over by a mouse pointer. \[...\]

final

isCollapsed → bool

Whether the decoration is the same size as the input field. \[...\]

final

isDense → bool

Whether the input decorator's child is part of a dense form (i.e., uses less vertical space). \[...\]

final

labelStyle → TextStyle

The style to use for InputDecoration.labelText when the label is above (i.e., vertically adjacent to) the input field. \[...\]

final

prefixStyle → TextStyle

The style to use for the InputDecoration.prefixText. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

suffixStyle → TextStyle

The style to use for the InputDecoration.suffixText. \[...\]

final

## Methods ##

copyWith(\{TextStyle labelStyle, TextStyle helperStyle, int helperMaxLines, TextStyle hintStyle, TextStyle errorStyle, int errorMaxLines, bool hasFloatingPlaceholder, FloatingLabelBehavior floatingLabelBehavior, bool isDense, EdgeInsetsGeometry contentPadding, bool isCollapsed, TextStyle prefixStyle, TextStyle suffixStyle, TextStyle counterStyle, bool filled, Color fillColor, Color focusColor, Color hoverColor, InputBorder errorBorder, InputBorder focusedBorder, InputBorder focusedErrorBorder, InputBorder disabledBorder, InputBorder enabledBorder, InputBorder border, bool alignLabelWithHint\}) → InputDecorationTheme

Creates a copy of this object but with the given fields replaced with the new values.

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

toDiagnosticsNode(\{String name, DiagnosticsTreeStyle style\}) → DiagnosticsNode

Returns a debug representation of the object that is used by debugging tools and by DiagnosticsNode.toStringDeep. \[...\]

inherited

toString(\{DiagnosticLevel minLevel: DiagnosticLevel.info\}) → String

Returns a string representation of this object.

inherited

toStringShort() → String

A brief description of this object, usually just the runtimeType and the hashCode. \[...\]

inherited

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

override


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/input_decorator.dart#L3578