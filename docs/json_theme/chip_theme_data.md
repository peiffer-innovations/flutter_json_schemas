[*description*][description]

# ChipThemeData class #

Holds the color, shape, and text styles for a material design chip theme.

Use this class to configure a ChipTheme widget, or to set the ThemeData.chipTheme for a Theme widget.

To obtain the current ambient chip theme, use ChipTheme.of.

The parts of a chip are:

 *  The "avatar", which is a widget that appears at the beginning of the chip. This is typically a CircleAvatar widget.
 *  The "label", which is the widget displayed in the center of the chip. Typically this is a Text widget.
 *  The "delete icon", which is a widget that appears at the end of the chip.
 *  The chip is disabled when it is not accepting user input. Only some chips have a disabled state: InputChip, ChoiceChip, and FilterChip.

The simplest way to create a ChipThemeData is to use copyWith on the one you get from ChipTheme.of, or create an entirely new one with ChipThemeData.fromDefaults.

 *link* 

Sample

*assignment*

    class CarColor extends StatefulWidget {
      @override
      State createState() => _CarColorState();
    }
    
    class _CarColorState extends State<CarColor> {
      Color _color = Colors.red;
    
      @override
      Widget build(BuildContext context) {
        return ChipTheme(
          data: ChipTheme.of(context).copyWith(backgroundColor: Colors.lightBlue),
          child: ChoiceChip(
            label: Text('Light Blue'),
            onSelected: (bool value) {
              setState(() {
                _color = value ? Colors.lightBlue : Colors.red;
              });
            },
            selected: _color == Colors.lightBlue,
          ),
        );
      }
    }

See also:

 *  Chip, a chip that displays information and can be deleted.
 *  InputChip, a chip that represents a complex piece of information, such as an entity (person, place, or thing) or conversational text, in a compact form.
 *  ChoiceChip, allows a single selection from a set of options. Choice chips contain related descriptive text or categories.
 *  FilterChip, uses tags or descriptive words as a way to filter content.
 *  ActionChip, represents an action related to primary content.
 *  CircleAvatar, which shows images or initials of entities.
 *  Wrap, A widget that displays its children in multiple horizontal or vertical runs.
 *  ChipTheme widget, which can override the chip theme of its children.
 *  Theme widget, which performs a similar function to ChipTheme, but for overall themes.
 *  ThemeData, which has a default ChipThemeData.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ChipThemeData(\{@required Color backgroundColor, Color deleteIconColor, @required Color disabledColor, @required Color selectedColor, @required Color secondarySelectedColor, Color shadowColor, Color selectedShadowColor, bool showCheckmark, Color checkmarkColor, EdgeInsetsGeometry labelPadding, @required EdgeInsetsGeometry padding, @required ShapeBorder shape, @required TextStyle labelStyle, @required TextStyle secondaryLabelStyle, @required Brightness brightness, double elevation, double pressElevation\})

Create a ChipThemeData given a set of exact values. All the values must be specified except for `shadowColor`, `selectedShadowColor`, `elevation`, and `pressElevation`, which may be null. \[...\]

const

ChipThemeData.fromDefaults(\{Brightness brightness, Color primaryColor, @required Color secondaryColor, @required TextStyle labelStyle\})

Generates a ChipThemeData from a brightness, a primary color, and a text style. \[...\]

factory

## Properties ##

backgroundColor → Color

Color to be used for the unselected, enabled chip's background. \[...\]

final

brightness → Brightness

The brightness setting for this theme. \[...\]

final

checkmarkColor → Color

Color of the chip's check mark when a check mark is visible. \[...\]

final

deleteIconColor → Color

The Color for the delete icon. The default is Color(0xde000000) (slightly transparent black) for light themes, and Color(0xdeffffff) (slightly transparent white) for dark themes. \[...\]

final

disabledColor → Color

Color to be used for the chip's background indicating that it is disabled. \[...\]

final

elevation → double

The elevation to be applied to the chip. \[...\]

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

labelPadding → EdgeInsetsGeometry

The padding around the Chip.label widget. \[...\]

final

labelStyle → TextStyle

The style to be applied to the chip's label. \[...\]

final

padding → EdgeInsetsGeometry

The padding between the contents of the chip and the outside shape. \[...\]

final

pressElevation → double

The elevation to be applied to the chip during the press motion. \[...\]

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

secondaryLabelStyle → TextStyle

An alternate style to be applied to the chip's label. For example, this style is applied to the text of a selected ChoiceChip. \[...\]

final

secondarySelectedColor → Color

An alternate color to be used for the chip's background, indicating that it is selected. For example, this color is used by ChoiceChip when the choice is selected. \[...\]

final

selectedColor → Color

Color to be used for the chip's background, indicating that it is selected. \[...\]

final

selectedShadowColor → Color

Color of the chip's shadow when the elevation is greater than 0 and the chip is selected. \[...\]

final

shadowColor → Color

Color of the chip's shadow when the elevation is greater than 0. \[...\]

final

shape → ShapeBorder

The border to draw around the chip. \[...\]

final

showCheckmark → bool

Whether or not to show a check mark when SelectableChipAttributes.selected is true. \[...\]

final

## Methods ##

copyWith(\{Color backgroundColor, Color deleteIconColor, Color disabledColor, Color selectedColor, Color secondarySelectedColor, Color shadowColor, Color selectedShadowColor, Color checkmarkColor, EdgeInsetsGeometry labelPadding, EdgeInsetsGeometry padding, ShapeBorder shape, TextStyle labelStyle, TextStyle secondaryLabelStyle, Brightness brightness, double elevation, double pressElevation\}) → ChipThemeData

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

## Static Methods ##

lerp(ChipThemeData a, ChipThemeData b, double t) → ChipThemeData

Linearly interpolate between two chip themes. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/chip_theme.dart#L174