[*description*][description]

# TextFormField class #

A FormField that contains a TextField.

This is a convenience widget that wraps a TextField widget in a FormField.

A Form ancestor is not required. The Form simply makes it easier to save, reset, or validate multiple fields at once. To use without a Form, pass a GlobalKey to the constructor and use GlobalKey.currentState to save or reset the form field.

When a controller is specified, its TextEditingController.text defines the initialValue. If this FormField is part of a scrolling container that lazily constructs its children, like a ListView or a CustomScrollView, then a controller should be specified. The controller's lifetime should be managed by a stateful widget ancestor of the scrolling container.

If a controller is not specified, initialValue can be used to give the automatically generated controller an initial value.

Remember to call TextEditingController.dispose of the TextEditingController when it is no longer needed. This will ensure we discard any resources used by the object.

By default, `decoration` will apply the ThemeData.inputDecorationTheme for the current context to the InputDecoration, see InputDecoration.applyDefaults.

For a documentation about the various parameters, see TextField.

 *link* 

Sample

Creates a TextFormField with an InputDecoration and validator function.

![If the user enters valid text, the TextField appears normally without any warnings to the user][If the user enters valid text_ the TextField appears normally without any warnings to the user]

![If the user enters invalid text, the error message returned from the validator function is displayed in dark red underneath the input][If the user enters invalid text_ the error message returned from the validator function is displayed in dark red underneath the input]

*assignment*

    TextFormField(
      decoration: const InputDecoration(
        icon: Icon(Icons.person),
        hintText: 'What do people call you?',
        labelText: 'Name *',
      ),
      onSaved: (String value) {
        // This optional block of code can be used to run
        // code when the user saves the form.
      },
      validator: (String value) {
        return value.contains('@') ? 'Do not use the @ char.' : null;
      },
    )

 *link* 

Interactive App Sample code

This example shows how to move the focus to the next field when the user presses the SPACE key.

To create a local project with this code sample, run:  
flutter create --sample=material.TextFormField.2 mysample

This example shows how to move the focus to the next field when the user presses the SPACE key.

*assignment*

    import 'package:flutter/services.dart';
    
    // ...
    
    Widget build(BuildContext context) {
      return Material(
        child: Center(
          child: Shortcuts(
            shortcuts: <LogicalKeySet, Intent>{
              // Pressing space in the field will now move to the next field.
              LogicalKeySet(LogicalKeyboardKey.space): const NextFocusIntent(),
            },
            child: FocusTraversalGroup(
              child: Form(
                autovalidateMode: AutovalidateMode.always,
                onChanged: () {
                  Form.of(primaryFocus.context).save();
                },
                child: Wrap(
                  children: List<Widget>.generate(5, (int index) {
                    return Padding(
                      padding: const EdgeInsets.all(8.0),
                      child: ConstrainedBox(
                        constraints: BoxConstraints.tight(const Size(200, 50)),
                        child: TextFormField(
                          onSaved: (String value) {
                            print('Value for field $index saved as "$value"');
                          },
                        ),
                      ),
                    );
                  }),
                ),
              ),
            ),
          ),
        ),
      );
    }

See also:

 *  [material.io/design/components/text-fields.html][material.io_design_components_text-fields.html]
 *  TextField, which is the underlying text field without the Form integration.
 *  InputDecorator, which shows the labels and other visual elements that surround the actual text editing widget.
 *  Learn how to use a TextEditingController in one of our [cookbook recipes][].

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  FormField<String>
 *  TextFormField

## Constructors ##

TextFormField(\{Key key, TextEditingController controller, String initialValue, FocusNode focusNode, InputDecoration decoration: const InputDecoration(), TextInputType keyboardType, TextCapitalization textCapitalization: TextCapitalization.none, TextInputAction textInputAction, TextStyle style, StrutStyle strutStyle, TextDirection textDirection, TextAlign textAlign: TextAlign.start, TextAlignVertical textAlignVertical, bool autofocus: false, bool readOnly: false, ToolbarOptions toolbarOptions, bool showCursor, String obscuringCharacter: '•', bool obscureText: false, bool autocorrect: true, SmartDashesType smartDashesType, SmartQuotesType smartQuotesType, bool enableSuggestions: true, @Deprecated('Use autoValidateMode parameter which provide more specific ' 'behaviour related to auto validation. ' 'This feature was deprecated after v1.19.0.') bool autovalidate: false, bool maxLengthEnforced: true, int maxLines: 1, int minLines, bool expands: false, int maxLength, ValueChanged<String> onChanged, GestureTapCallback onTap, VoidCallback onEditingComplete, ValueChanged<String> onFieldSubmitted, FormFieldSetter<String> onSaved, FormFieldValidator<String> validator, List<TextInputFormatter> inputFormatters, bool enabled, double cursorWidth: 2.0, double cursorHeight, Radius cursorRadius, Color cursorColor, Brightness keyboardAppearance, EdgeInsets scrollPadding: const EdgeInsets.all(20.0), bool enableInteractiveSelection: true, InputCounterWidgetBuilder buildCounter, ScrollPhysics scrollPhysics, Iterable<String> autofillHints, AutovalidateMode autovalidateMode\})

Creates a FormField that contains a TextField. \[...\]

## Properties ##

autovalidate → bool

Used to enable/disable auto validation and update their error text.

@Deprecated('Use autoValidateMode parameter which provides more specific ' 'behavior related to auto validation. ' 'This feature was deprecated after v1.19.0.'), final, inherited

autovalidateMode → AutovalidateMode

Used to enable/disable this form field auto validation and update its error text. \[...\]

final, inherited

builder → FormFieldBuilder<String>

Function that returns the widget representing this form field. It is passed the form field state as input, containing the current value and validation state of this field.

final, inherited

controller → TextEditingController

Controls the text being edited. \[...\]

final

enabled → bool

Whether the form is able to receive user input. \[...\]

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

initialValue → String

An optional value to initialize the form field to, or null otherwise.

final, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onSaved → FormFieldSetter<String>

An optional method to call with the final value when the form is saved via FormState.save.

final, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

validator → FormFieldValidator<String>

An optional method that validates an input. Returns an error string to display if the input is invalid, or null otherwise. \[...\]

final, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_TextFormFieldState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/text_form_field.dart#L127
[If the user enters valid text_ the TextField appears normally without any warnings to the user]: https://flutter.github.io/assets-for-api-docs/assets/material/text_form_field.png
[If the user enters invalid text_ the error message returned from the validator function is displayed in dark red underneath the input]: https://flutter.github.io/assets-for-api-docs/assets/material/text_form_field_error.png
[material.io_design_components_text-fields.html]: https://material.io/design/components/text-fields.html
[cookbook recipes]: https://flutter.dev/docs/cookbook/forms/text-field-changes#2-use-a-texteditingcontroller