[*description*][description]

# AnimatedSwitcher class #

A widget that by default does a cross-fade between a new widget and the widget previously set on the AnimatedSwitcher as a child.

If they are swapped fast enough (i.e. before duration elapses), more than one previous child can exist and be transitioning out while the newest one is transitioning in.

If the "new" child is the same widget type and key as the "old" child, but with different parameters, then AnimatedSwitcher will *not* do a transition between them, since as far as the framework is concerned, they are the same widget and the existing widget can be updated with the new parameters. To force the transition to occur, set a Key on each child widget that you wish to be considered unique (typically a ValueKey on the widget data that distinguishes this child from the others).

The same key can be used for a new child as was used for an already-outgoing child; the two will not be considered related. (For example, if a progress indicator with key A is first shown, then an image with key B, then another progress indicator with key A again, all in rapid succession, then the old progress indicator and the image will be fading out while a new progress indicator is fading in.)

The type of transition can be changed from a cross-fade to a custom transition by setting the transitionBuilder.

 *link* 

Interactive App Sample code

This sample shows a counter that animates the scale of a text widget whenever the value changes.

To create a local project with this code sample, run:  
flutter create --sample=widgets.AnimatedSwitcher.1 mysample

This sample shows a counter that animates the scale of a text widget whenever the value changes.

*assignment*

    int _count = 0;
    
    @override
    Widget build(BuildContext context) {
      return Container(
        color: Colors.white,
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            AnimatedSwitcher(
              duration: const Duration(milliseconds: 500),
              transitionBuilder: (Widget child, Animation<double> animation) {
                return ScaleTransition(child: child, scale: animation);
              },
              child: Text(
                '$_count',
                // This key causes the AnimatedSwitcher to interpret this as a "new"
                // child each time the count changes, so that it will begin its animation
                // when the count changes.
                key: ValueKey<int>(_count),
                style: Theme.of(context).textTheme.headline4,
              ),
            ),
            ElevatedButton(
              child: const Text('Increment'),
              onPressed: () {
                setState(() {
                  _count += 1;
                });
              },
            ),
          ],
        ),
      );
    }

See also:

 *  AnimatedCrossFade, which only fades between two children, but also interpolates their sizes, and is reversible.
 *  AnimatedOpacity, which can be used to switch between nothingness and a given child by fading the child in and out.
 *  FadeTransition, which AnimatedSwitcher uses to perform the transition.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  AnimatedSwitcher

## Constructors ##

AnimatedSwitcher(\{Key key, Widget child, @required Duration duration, Duration reverseDuration, Curve switchInCurve: Curves.linear, Curve switchOutCurve: Curves.linear, AnimatedSwitcherTransitionBuilder transitionBuilder: AnimatedSwitcher.defaultTransitionBuilder, AnimatedSwitcherLayoutBuilder layoutBuilder: AnimatedSwitcher.defaultLayoutBuilder\})

Creates an AnimatedSwitcher. \[...\]

const

## Properties ##

child → Widget

The current child widget to display. If there was a previous child, then that child will be faded out using the switchOutCurve, while the new child is faded in with the switchInCurve, over the duration. \[...\]

final

duration → Duration

The duration of the transition from the old child value to the new one. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

layoutBuilder → AnimatedSwitcherLayoutBuilder

A function that wraps all of the children that are transitioning out, and the child that's transitioning in, with a widget that lays all of them out. This is called every time this widget is built. The function must not return null. \[...\]

final

reverseDuration → Duration

The duration of the transition from the new child value to the old one. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

switchInCurve → Curve

The animation curve to use when transitioning in a new child. \[...\]

final

switchOutCurve → Curve

The animation curve to use when transitioning a previous child out. \[...\]

final

transitionBuilder → AnimatedSwitcherTransitionBuilder

A function that wraps a new child with an animation that transitions the child in when the animation runs in the forward direction and out when the animation runs in the reverse direction. This is only called when a new child is set (not for each build), or when a new transitionBuilder is set. If a new transitionBuilder is set, then the transition is rebuilt for the current child and all previous children using the new transitionBuilder. The function must not return null. \[...\]

final

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedSwitcherState

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

## Static Methods ##

defaultLayoutBuilder(Widget currentChild, List<Widget> previousChildren) → Widget

The layout builder used as the default value of layoutBuilder. \[...\]

defaultTransitionBuilder(Widget child, Animation<double> animation) → Widget

The transition builder used as the default value of transitionBuilder. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/animated_switcher.dart#L145