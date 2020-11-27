[*description*][description]

# AnimatedOpacity class #

Animated version of Opacity which automatically transitions the child's opacity over a given duration whenever the given opacity changes.

Animating an opacity is relatively expensive because it requires painting the child into an intermediate buffer.

Here's an illustration of what using this widget looks like, using a curve of Curves.fastOutSlowIn.

 *link* 

Sample

*assignment*

    class LogoFade extends StatefulWidget {
      @override
      createState() => LogoFadeState();
    }
    
    class LogoFadeState extends State<LogoFade> {
      double opacityLevel = 1.0;
    
      void _changeOpacity() {
        setState(() => opacityLevel = opacityLevel == 0 ? 1.0 : 0.0);
      }
    
      @override
      Widget build(BuildContext context) {
        return Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            AnimatedOpacity(
              opacity: opacityLevel,
              duration: Duration(seconds: 3),
              child: FlutterLogo(),
            ),
            ElevatedButton(
              child: Text('Fade Logo'),
              onPressed: _changeOpacity,
            ),
          ],
        );
      }
    }

See also:

 *  AnimatedCrossFade, for fading between two children.
 *  AnimatedSwitcher, for fading between many children in sequence.
 *  FadeTransition, an explicitly animated version of this widget, where an Animation is provided by the caller instead of being built in.
 *  SliverAnimatedOpacity, for automatically transitioning a sliver's opacity over a given duration whenever the given opacity changes.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  StatefulWidget
 *  ImplicitlyAnimatedWidget
 *  AnimatedOpacity

## Constructors ##

AnimatedOpacity(\{Key key, Widget child, @required double opacity, Curve curve: Curves.linear, @required Duration duration, VoidCallback onEnd, bool alwaysIncludeSemantics: false\})

Creates a widget that animates its opacity implicitly. \[...\]

const

## Properties ##

alwaysIncludeSemantics → bool

Whether the semantic information of the children is always included. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final

curve → Curve

The curve to apply when animating the parameters of this container.

final, inherited

duration → Duration

The duration over which to animate the parameters of this container.

final, inherited

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

onEnd → VoidCallback

Called every time an animation completes. \[...\]

final, inherited

opacity → double

The target opacity. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createElement() → StatefulElement

Creates a StatefulElement to manage this widget's location in the tree. \[...\]

inherited

createState() → \_AnimatedOpacityState

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


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/implicit_animations.dart#L1328