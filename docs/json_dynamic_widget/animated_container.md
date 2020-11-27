[*description*][description]

# AnimatedContainer class #

Animated version of Container that gradually changes its values over a period of time.

The AnimatedContainer will automatically animate between the old and new values of properties when they change using the provided curve and duration. Properties that are null are not animated. Its child and descendants are not animated.

This class is useful for generating simple implicit transitions between different parameters to Container with its internal AnimationController. For more complex animations, you'll likely want to use a subclass of AnimatedWidget such as the DecoratedBoxTransition or use your own AnimationController.

 *link* 

Interactive App Sample code

The following example (depicted above) transitions an AnimatedContainer between two states. It adjusts the `height`, `width`, `color`, and alignment properties when tapped.

To create a local project with this code sample, run:  
flutter create --sample=widgets.AnimatedContainer.1 mysample

The following example (depicted above) transitions an AnimatedContainer between two states. It adjusts the `height`, `width`, `color`, and alignment properties when tapped.

*assignment*

    bool selected = false;
    
    @override
    Widget build(BuildContext context) {
      return GestureDetector(
        onTap: () {
          setState(() {
            selected = !selected;
          });
        },
        child: Center(
          child: AnimatedContainer(
            width: selected ? 200.0 : 100.0,
            height: selected ? 100.0 : 200.0,
            color: selected ? Colors.red : Colors.blue,
            alignment: selected ? Alignment.center : AlignmentDirectional.topCenter,
            duration: Duration(seconds: 2),
            curve: Curves.fastOutSlowIn,
            child: FlutterLogo(size: 75),
          ),
        ),
      );
    }

See also:

 *  AnimatedPadding, which is a subset of this widget that only supports animating the padding.
 *  The [catalog of layout widgets][].
 *  AnimatedPositioned, which, as a child of a Stack, automatically transitions its child's position over a given duration whenever the given position changes.
 *  AnimatedAlign, which automatically transitions its child's position over a given duration whenever the given alignment changes.
 *  AnimatedSwitcher, which switches out a child for a new one with a customizable transition.
 *  AnimatedCrossFade, which fades between two children and interpolates their sizes.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedContainer

## Constructors ##

AnimatedContainer(\{Key key, AlignmentGeometry alignment, EdgeInsetsGeometry padding, Color color, Decoration decoration, Decoration foregroundDecoration, double width, double height, BoxConstraints constraints, EdgeInsetsGeometry margin, Matrix4 transform, Widget child, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd\})

Creates a container that animates its parameters implicitly. \[...\]

## Properties ##

alignment → AlignmentGeometry

Align the child within the container. \[...\]

final

child → Widget

The child contained by the container. \[...\]

final

constraints → BoxConstraints

Additional constraints to apply to the child. \[...\]

final

curve → Curve

The curve to apply when animating the parameters of this container.

final, inherited

decoration → Decoration

The decoration to paint behind the child. \[...\]

final

duration → Duration

The duration over which to animate the parameters of this container.

final, inherited

foregroundDecoration → Decoration

The decoration to paint in front of the child.

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

margin → EdgeInsetsGeometry

Empty space to surround the decoration and child.

final

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

padding → EdgeInsetsGeometry

Empty space to inscribe inside the decoration. The child, if any, is placed inside this padding.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

transform → Matrix4

The transformation matrix to apply before painting the container.

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedContainerState

Creates the mutable state for this widget at a given location in the tree. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L627
[catalog of layout widgets]: https://flutter.dev/widgets/layout/