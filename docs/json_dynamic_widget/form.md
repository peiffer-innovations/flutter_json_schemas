[*description*][description]

# Form class #

An optional container for grouping together multiple form field widgets (e.g. TextField widgets).

Each individual form field should be wrapped in a FormField widget, with the Form widget as a common ancestor of all of those. Call methods on FormState to save, reset, or validate each FormField that is a descendant of this Form. To obtain the FormState, you may use Form.of with a context whose ancestor is the Form, or pass a GlobalKey to the Form constructor and call GlobalKey.currentState.

 *link* 

Interactive App Sample code

This example shows a Form with one TextFormField to enter an email address and an ElevatedButton to submit the form. A GlobalKey is used here to identify the Form and validate input.

![form.png][]

To create a local project with this code sample, run:  
flutter create --sample=widgets.Form.1 mysample

This example shows a Form with one TextFormField to enter an email address and an ElevatedButton to submit the form. A GlobalKey is used here to identify the Form and validate input.

![form.png][]

*assignment*

    final _formKey = GlobalKey<FormState>();
    
    @override
    Widget build(BuildContext context) {
      return Form(
        key: _formKey,
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: <Widget>[
            TextFormField(
              decoration: const InputDecoration(
                hintText: 'Enter your email',
              ),
              validator: (value) {
                if (value.isEmpty) {
                  return 'Please enter some text';
                }
                return null;
              },
            ),
            Padding(
              padding: const EdgeInsets.symmetric(vertical: 16.0),
              child: ElevatedButton(
                onPressed: () {
                  // Validate will return true if the form is valid, or false if
                  // the form is invalid.
                  if (_formKey.currentState.validate()) {
                    // Process data.
                  }
                },
                child: Text('Submit'),
              ),
            ),
          ],
        ),
      );
    }

See also:

 *  GlobalKey, a key that is unique across the entire app.
 *  FormField, a single form field widget that maintains the current state.
 *  TextFormField, a convenience widget that wraps a TextField widget in a FormField.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  Form

## Constructors ##

Form(\{Key key, @required Widget child, @Deprecated('Use autoValidateMode parameter which provides more specific ' 'behavior related to auto validation. ' 'This feature was deprecated after v1.19.0.') bool autovalidate: false, WillPopCallback onWillPop, VoidCallback onChanged, AutovalidateMode autovalidateMode\})

Creates a container for form fields. \[...\]

const

## Properties ##

autovalidate → bool

Used to enable/disable form fields auto validation and update their error text.

@Deprecated('Use autoValidateMode parameter which provides more specific ' 'behavior related to auto validation. ' 'This feature was deprecated after v1.19.0.'), final

autovalidateMode → AutovalidateMode

Used to enable/disable form fields auto validation and update their error text. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onChanged → VoidCallback

Called when one of the form fields changes. \[...\]

final

onWillPop → WillPopCallback

Enables the form to veto attempts by the user to dismiss the ModalRoute that contains the form. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → FormState

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

## Static Methods ##

of(BuildContext context) → FormState

Returns the closest FormState which encloses the given context. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/form.dart#L74
[form.png]: https://flutter.github.io/assets-for-api-docs/assets/widgets/form.png