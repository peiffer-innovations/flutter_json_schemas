[*description*][description]

# AnimatedSize class #

Animated widget that automatically transitions its size over a given duration whenever the given child's size changes.

 *link* 

Interactive App Sample code

This example makes a Container react to being touched, causing the child of the AnimatedSize widget, here a FlutterLogo, to animate.

To create a local project with this code sample, run:  
flutter create --sample=widgets.AnimatedSize.1 mysample

This example makes a Container react to being touched, causing the child of the AnimatedSize widget, here a FlutterLogo, to animate.

*assignment*

    class _MyStatefulWidgetState extends State<MyStatefulWidget> with SingleTickerProviderStateMixin {
      double _size = 50.0;
      bool _large = false;
    
      void _updateSize() {
        setState(() {
          _size = _large ? 250.0 : 100.0;
          _large = !_large;
        });
      }
    
      @override
      Widget build(BuildContext context) {
        return GestureDetector(
          onTap: () => _updateSize(),
          child: Container(
            color: Colors.amberAccent,
            child: AnimatedSize(
              curve: Curves.easeIn,
              vsync: this,
              duration: Duration(seconds: 1),
              child: FlutterLogo(size: _size),
            ),
          ),
        );
      }
    }

See also:

 *  SizeTransition, which changes its size based on an Animation.

Inheritance

 *  Object
 *  DiagnosticableTree
 *  Widget
 *  RenderObjectWidget
 *  SingleChildRenderObjectWidget
 *  AnimatedSize

## Constructors ##

AnimatedSize(\{Key key, Widget child, AlignmentGeometry alignment: Alignment.center, Curve curve: Curves.linear, @required Duration duration, Duration reverseDuration, @required TickerProvider vsync\})

Creates a widget that animates its size to match that of its child. \[...\]

const

## Properties ##

alignment → AlignmentGeometry

The alignment of the child within the parent when the parent is not yet the same size as the child. \[...\]

final

child → Widget

The widget below this widget in the tree. \[...\]

final, inherited

curve → Curve

The animation curve when transitioning this widget's size to match the child's size.

final

duration → Duration

The duration when transitioning this widget's size to match the child's size.

final

hashCode → int

The hash code for this object. \[...\]

@nonVirtual, read-only, inherited

key → Key

Controls how one widget replaces another widget in the tree. \[...\]

final, inherited

reverseDuration → Duration

The duration when transitioning this widget's size to match the child's size when going in reverse. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

vsync → TickerProvider

The TickerProvider for this widget.

final

## Methods ##

createElement() → SingleChildRenderObjectElement

RenderObjectWidgets always inflate to a RenderObjectElement subclass.

inherited

createRenderObject(BuildContext context) → RenderAnimatedSize

Creates an instance of the RenderObject class that this RenderObjectWidget represents, using the configuration described by this RenderObjectWidget. \[...\]

override

debugDescribeChildren() → List<DiagnosticsNode>

Returns a list of DiagnosticsNode objects describing this node's children. \[...\]

@protected, inherited

debugFillProperties(DiagnosticPropertiesBuilder properties) → void

Add additional properties associated with the node. \[...\]

override

didUnmountRenderObject(covariant RenderObject renderObject) → void

A render object previously associated with this widget has been removed from the tree. The given RenderObject will be of the same type as returned by this object's createRenderObject.

@protected, inherited

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

updateRenderObject(BuildContext context, covariant RenderAnimatedSize renderObject) → void

Copies the configuration described by this RenderObjectWidget to the given RenderObject, which will be of the same type as returned by this object's createRenderObject. \[...\]

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

@nonVirtual, inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/widgets/animated_size.dart#L54