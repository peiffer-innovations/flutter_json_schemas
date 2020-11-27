[*description*][description]

# ThemeData class #

Defines the configuration of the overall visual Theme for a MaterialApp or a widget subtree within the app.

The MaterialApp theme property can be used to configure the appearance of the entire app. Widget subtree's within an app can override the app's theme by including a Theme widget at the top of the subtree.

Widgets whose appearance should align with the overall theme can obtain the current theme's configuration with Theme.of. Material components typically depend exclusively on the colorScheme and textTheme. These properties are guaranteed to have non-null values.

The static Theme.of method finds the ThemeData value specified for the nearest BuildContext ancestor. This lookup is inexpensive, essentially just a single HashMap access. It can sometimes be a little confusing because Theme.of can not see a Theme widget that is defined in the current build method's context. To overcome that, create a new custom widget for the subtree that appears below the new Theme, or insert a widget that creates a new BuildContext, like Builder.

 *link* 

Sample

In this example, the Container widget uses Theme.of to retrieve the primary color from the theme's colorScheme to draw an amber square. The Builder widget separates the parent theme's BuildContext from the child's BuildContext.

![theme_data.png][]

*assignment*

    Theme(
      data: ThemeData.from(
        colorScheme: ColorScheme.fromSwatch(primarySwatch: Colors.amber),
      ),
      child: Builder(
        builder: (BuildContext context) {
          return Container(
            width: 100,
            height: 100,
            color: Theme.of(context).colorScheme.primary,
          );
        },
      ),
    )

 *link* 

Sample

This sample creates a MaterialApp widget that stores `ThemeData` and passes the `ThemeData` to descendant widgets. The AppBar widget uses the primaryColor to create a blue background. The Text widget uses the TextTheme.bodyText2 to create purple text. The FloatingActionButton widget uses the accentColor to create a green background.

![material_app_theme_data.png][]

*assignment*

    MaterialApp(
      theme: ThemeData(
        primaryColor: Colors.blue,
        accentColor: Colors.green,
        textTheme: TextTheme(bodyText2: TextStyle(color: Colors.purple)),
      ),
      home: Scaffold(
        appBar: AppBar(
          title: const Text('ThemeData Demo'),
        ),
        floatingActionButton: FloatingActionButton(
          child: const Icon(Icons.add),
          onPressed: () {},
        ),
        body: Center(
          child: Text(
            'Button pressed 0 times',
          ),
        ),
      ),
    )

See [material.io/design/color/][material.io_design_color] for more discussion on how to pick the right colors.

Mixed in types

 *  Diagnosticable

Annotations

 *  @immutable

## Constructors ##

ThemeData(\{Brightness brightness, VisualDensity visualDensity, MaterialColor primarySwatch, Color primaryColor, Brightness primaryColorBrightness, Color primaryColorLight, Color primaryColorDark, Color accentColor, Brightness accentColorBrightness, Color canvasColor, Color shadowColor, Color scaffoldBackgroundColor, Color bottomAppBarColor, Color cardColor, Color dividerColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, InteractiveInkFeatureFactory splashFactory, Color selectedRowColor, Color unselectedWidgetColor, Color disabledColor, Color buttonColor, ButtonThemeData buttonTheme, ToggleButtonsThemeData toggleButtonsTheme, Color secondaryHeaderColor, Color textSelectionColor, Color cursorColor, Color textSelectionHandleColor, Color backgroundColor, Color dialogBackgroundColor, Color indicatorColor, Color hintColor, Color errorColor, Color toggleableActiveColor, String fontFamily, TextTheme textTheme, TextTheme primaryTextTheme, TextTheme accentTextTheme, InputDecorationTheme inputDecorationTheme, IconThemeData iconTheme, IconThemeData primaryIconTheme, IconThemeData accentIconTheme, SliderThemeData sliderTheme, TabBarTheme tabBarTheme, TooltipThemeData tooltipTheme, CardTheme cardTheme, ChipThemeData chipTheme, TargetPlatform platform, MaterialTapTargetSize materialTapTargetSize, bool applyElevationOverlayColor, PageTransitionsTheme pageTransitionsTheme, AppBarTheme appBarTheme, BottomAppBarTheme bottomAppBarTheme, ColorScheme colorScheme, DialogTheme dialogTheme, FloatingActionButtonThemeData floatingActionButtonTheme, NavigationRailThemeData navigationRailTheme, Typography typography, CupertinoThemeData cupertinoOverrideTheme, SnackBarThemeData snackBarTheme, BottomSheetThemeData bottomSheetTheme, PopupMenuThemeData popupMenuTheme, MaterialBannerThemeData bannerTheme, DividerThemeData dividerTheme, ButtonBarThemeData buttonBarTheme, BottomNavigationBarThemeData bottomNavigationBarTheme, TimePickerThemeData timePickerTheme, TextButtonThemeData textButtonTheme, ElevatedButtonThemeData elevatedButtonTheme, OutlinedButtonThemeData outlinedButtonTheme, TextSelectionThemeData textSelectionTheme, DataTableThemeData dataTableTheme, bool fixTextFieldOutlineLabel, bool useTextSelectionTheme\})

Create a ThemeData that's used to configure a Theme. \[...\]

factory

ThemeData.dark()

A default dark theme with a teal secondary ColorScheme color. \[...\]

factory

ThemeData.fallback()

The default color theme. Same as new ThemeData.light. \[...\]

factory

ThemeData.from(\{@required ColorScheme colorScheme, TextTheme textTheme\})

Create a ThemeData based on the colors in the given `colorScheme` and text styles of the optional `textTheme`. \[...\]

factory

ThemeData.light()

A default light blue theme. \[...\]

factory

ThemeData.raw(\{@required VisualDensity visualDensity, @required Color primaryColor, @required Brightness primaryColorBrightness, @required Color primaryColorLight, @required Color primaryColorDark, @required Color canvasColor, @required Color shadowColor, @required Color accentColor, @required Brightness accentColorBrightness, @required Color scaffoldBackgroundColor, @required Color bottomAppBarColor, @required Color cardColor, @required Color dividerColor, @required Color focusColor, @required Color hoverColor, @required Color highlightColor, @required Color splashColor, @required InteractiveInkFeatureFactory splashFactory, @required Color selectedRowColor, @required Color unselectedWidgetColor, @required Color disabledColor, @required ButtonThemeData buttonTheme, @required Color buttonColor, @required ToggleButtonsThemeData toggleButtonsTheme, @required Color secondaryHeaderColor, @required Color textSelectionColor, @required Color cursorColor, @required Color textSelectionHandleColor, @required Color backgroundColor, @required Color dialogBackgroundColor, @required Color indicatorColor, @required Color hintColor, @required Color errorColor, @required Color toggleableActiveColor, @required TextTheme textTheme, @required TextTheme primaryTextTheme, @required TextTheme accentTextTheme, @required InputDecorationTheme inputDecorationTheme, @required IconThemeData iconTheme, @required IconThemeData primaryIconTheme, @required IconThemeData accentIconTheme, @required SliderThemeData sliderTheme, @required TabBarTheme tabBarTheme, @required TooltipThemeData tooltipTheme, @required CardTheme cardTheme, @required ChipThemeData chipTheme, @required TargetPlatform platform, @required MaterialTapTargetSize materialTapTargetSize, @required bool applyElevationOverlayColor, @required PageTransitionsTheme pageTransitionsTheme, @required AppBarTheme appBarTheme, @required BottomAppBarTheme bottomAppBarTheme, @required ColorScheme colorScheme, @required DialogTheme dialogTheme, @required FloatingActionButtonThemeData floatingActionButtonTheme, @required NavigationRailThemeData navigationRailTheme, @required Typography typography, @required CupertinoThemeData cupertinoOverrideTheme, @required SnackBarThemeData snackBarTheme, @required BottomSheetThemeData bottomSheetTheme, @required PopupMenuThemeData popupMenuTheme, @required MaterialBannerThemeData bannerTheme, @required DividerThemeData dividerTheme, @required ButtonBarThemeData buttonBarTheme, @required BottomNavigationBarThemeData bottomNavigationBarTheme, @required TimePickerThemeData timePickerTheme, @required TextButtonThemeData textButtonTheme, @required ElevatedButtonThemeData elevatedButtonTheme, @required OutlinedButtonThemeData outlinedButtonTheme, @required TextSelectionThemeData textSelectionTheme, @required DataTableThemeData dataTableTheme, @required bool fixTextFieldOutlineLabel, @required bool useTextSelectionTheme\})

Create a ThemeData given a set of exact values. All the values must be specified. They all must also be non-null except for `cupertinoOverrideTheme`. \[...\]

const

## Properties ##

accentColor → Color

The foreground color for widgets (knobs, text, overscroll edge effect, etc). \[...\]

final

accentColorBrightness → Brightness

The brightness of the accentColor. Used to determine the color of text and icons placed on top of the accent color (e.g. the icons on a floating action button).

final

accentIconTheme → IconThemeData

An icon theme that contrasts with the accent color.

final

accentTextTheme → TextTheme

A text theme that contrasts with the accent color.

final

appBarTheme → AppBarTheme

A theme for customizing the color, elevation, brightness, iconTheme and textTheme of AppBars.

final

applyElevationOverlayColor → bool

Apply a semi-transparent overlay color on Material surfaces to indicate elevation for dark themes. \[...\]

final

backgroundColor → Color

A color that contrasts with the primaryColor, e.g. used as the remaining part of a progress bar.

final

bannerTheme → MaterialBannerThemeData

A theme for customizing the color and text style of a MaterialBanner.

final

bottomAppBarColor → Color

The default color of the BottomAppBar. \[...\]

final

bottomAppBarTheme → BottomAppBarTheme

A theme for customizing the shape, elevation, and color of a BottomAppBar.

final

bottomNavigationBarTheme → BottomNavigationBarThemeData

A theme for customizing the appearance and layout of BottomNavigationBar widgets.

final

bottomSheetTheme → BottomSheetThemeData

A theme for customizing the color, elevation, and shape of a bottom sheet.

final

brightness → Brightness

The overall theme brightness. \[...\]

read-only

buttonBarTheme → ButtonBarThemeData

A theme for customizing the appearance and layout of ButtonBar widgets.

final

buttonColor → Color

The default fill color of the Material used in RaisedButtons.

final

buttonTheme → ButtonThemeData

Defines the default configuration of button widgets, like RaisedButton and FlatButton.

final

canvasColor → Color

The default color of MaterialType.canvas Material.

final

cardColor → Color

The color of Material when it is used as a Card.

final

cardTheme → CardTheme

The colors and styles used to render Card. \[...\]

final

chipTheme → ChipThemeData

The colors and styles used to render Chips. \[...\]

final

colorScheme → ColorScheme

A set of thirteen colors that can be used to configure the color properties of most components. \[...\]

final

cupertinoOverrideTheme → CupertinoThemeData

Components of the CupertinoThemeData to override from the Material ThemeData adaptation. \[...\]

final

cursorColor → Color

The color of cursors in Material-style text fields, such as TextField.

final

dataTableTheme → DataTableThemeData

A theme for customizing the appearance and layout of DataTable widgets.

final

dialogBackgroundColor → Color

The background color of Dialog elements.

final

dialogTheme → DialogTheme

A theme for customizing the shape of a dialog.

final

disabledColor → Color

The color used for widgets that are inoperative, regardless of their state. For example, a disabled checkbox (which may be checked or unchecked).

final

dividerColor → Color

The color of Dividers and PopupMenuDividers, also used between ListTiles, between rows in DataTables, and so forth. \[...\]

final

dividerTheme → DividerThemeData

A theme for customizing the color, thickness, and indents of Dividers, VerticalDividers, etc.

final

elevatedButtonTheme → ElevatedButtonThemeData

A theme for customizing the appearance and internal layout of ElevatedButtons.

final

errorColor → Color

The color to use for input validation errors, e.g. in TextField fields.

final

fixTextFieldOutlineLabel → bool

A temporary flag to allow apps to opt-in to a [small fix][] for the Y coordinate of the floating label in a TextField OutlineInputBorder. \[...\]

final

floatingActionButtonTheme → FloatingActionButtonThemeData

A theme for customizing the shape, elevation, and color of a FloatingActionButton.

final

focusColor → Color

The focus color used indicate that a component has the input focus.

final

hashCode → int

The hash code for this object. \[...\]

read-only, override

highlightColor → Color

The highlight color used during ink splash animations or to indicate an item in a menu is selected.

final

hintColor → Color

The color to use for hint text or placeholder text, e.g. in TextField fields.

final

hoverColor → Color

The hover color used to indicate when a pointer is hovering over a component.

final

iconTheme → IconThemeData

An icon theme that contrasts with the card and canvas colors.

final

indicatorColor → Color

The color of the selected tab indicator in a tab bar.

final

inputDecorationTheme → InputDecorationTheme

The default InputDecoration values for InputDecorator, TextField, and TextFormField are based on this theme. \[...\]

final

materialTapTargetSize → MaterialTapTargetSize

Configures the hit test size of certain Material widgets.

final

navigationRailTheme → NavigationRailThemeData

A theme for customizing the background color, elevation, text style, and icon themes of a NavigationRail.

final

outlinedButtonTheme → OutlinedButtonThemeData

A theme for customizing the appearance and internal layout of OutlinedButtons.

final

pageTransitionsTheme → PageTransitionsTheme

Default MaterialPageRoute transitions per TargetPlatform. \[...\]

final

platform → TargetPlatform

The platform the material widgets should adapt to target. \[...\]

final

popupMenuTheme → PopupMenuThemeData

A theme for customizing the color, shape, elevation, and text style of popup menus.

final

primaryColor → Color

The background color for major parts of the app (toolbars, tab bars, etc) \[...\]

final

primaryColorBrightness → Brightness

The brightness of the primaryColor. Used to determine the color of text and icons placed on top of the primary color (e.g. toolbar text).

final

primaryColorDark → Color

A darker version of the primaryColor.

final

primaryColorLight → Color

A lighter version of the primaryColor.

final

primaryIconTheme → IconThemeData

An icon theme that contrasts with the primary color.

final

primaryTextTheme → TextTheme

A text theme that contrasts with the primary color.

final

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

scaffoldBackgroundColor → Color

The default color of the Material that underlies the Scaffold. The background color for a typical material app or a page within the app.

final

secondaryHeaderColor → Color

The color of the header of a PaginatedDataTable when there are selected rows.

final

selectedRowColor → Color

The color used to highlight selected rows.

final

shadowColor → Color

The color that the Material widget uses to draw elevation shadows. \[...\]

final

sliderTheme → SliderThemeData

The colors and shapes used to render Slider. \[...\]

final

snackBarTheme → SnackBarThemeData

A theme for customizing colors, shape, elevation, and behavior of a SnackBar.

final

splashColor → Color

The color of ink splashes. See InkWell.

final

splashFactory → InteractiveInkFeatureFactory

Defines the appearance of ink splashes produces by InkWell and InkResponse. \[...\]

final

tabBarTheme → TabBarTheme

A theme for customizing the size, shape, and color of the tab bar indicator.

final

textButtonTheme → TextButtonThemeData

A theme for customizing the appearance and internal layout of TextButtons.

final

textSelectionColor → Color

The color of text selections in text fields, such as TextField.

final

textSelectionHandleColor → Color

The color of the handles used to adjust what part of the text is currently selected.

final

textSelectionTheme → TextSelectionThemeData

A theme for customizing the appearance and layout of TextField widgets.

final

textTheme → TextTheme

Text with a color that contrasts with the card and canvas colors.

final

timePickerTheme → TimePickerThemeData

A theme for customizing the appearance and layout of time picker widgets.

final

toggleableActiveColor → Color

The color used to highlight the active states of toggleable widgets like Switch, Radio, and Checkbox.

final

toggleButtonsTheme → ToggleButtonsThemeData

Defines the default configuration of ToggleButtons widgets.

final

tooltipTheme → TooltipThemeData

A theme for customizing the visual properties of Tooltips. \[...\]

final

typography → Typography

The color and geometry TextTheme values used to configure textTheme, primaryTextTheme, and accentTextTheme.

final

unselectedWidgetColor → Color

The color used for widgets in their inactive (but enabled) state. For example, an unchecked checkbox. Usually contrasted with the accentColor. See also disabledColor.

final

useTextSelectionTheme → bool

A temporary flag to allow apps to opt-in to the new TextSelectionTheme, with its new defaults for the cursorColor and textSelectionHandleColor. \[...\]

final

visualDensity → VisualDensity

The density value for specifying the compactness of various UI components. \[...\]

final

## Methods ##

copyWith(\{Brightness brightness, VisualDensity visualDensity, Color primaryColor, Brightness primaryColorBrightness, Color primaryColorLight, Color primaryColorDark, Color accentColor, Brightness accentColorBrightness, Color canvasColor, Color shadowColor, Color scaffoldBackgroundColor, Color bottomAppBarColor, Color cardColor, Color dividerColor, Color focusColor, Color hoverColor, Color highlightColor, Color splashColor, InteractiveInkFeatureFactory splashFactory, Color selectedRowColor, Color unselectedWidgetColor, Color disabledColor, ButtonThemeData buttonTheme, ToggleButtonsThemeData toggleButtonsTheme, Color buttonColor, Color secondaryHeaderColor, Color textSelectionColor, Color cursorColor, Color textSelectionHandleColor, Color backgroundColor, Color dialogBackgroundColor, Color indicatorColor, Color hintColor, Color errorColor, Color toggleableActiveColor, TextTheme textTheme, TextTheme primaryTextTheme, TextTheme accentTextTheme, InputDecorationTheme inputDecorationTheme, IconThemeData iconTheme, IconThemeData primaryIconTheme, IconThemeData accentIconTheme, SliderThemeData sliderTheme, TabBarTheme tabBarTheme, TooltipThemeData tooltipTheme, CardTheme cardTheme, ChipThemeData chipTheme, TargetPlatform platform, MaterialTapTargetSize materialTapTargetSize, bool applyElevationOverlayColor, PageTransitionsTheme pageTransitionsTheme, AppBarTheme appBarTheme, BottomAppBarTheme bottomAppBarTheme, ColorScheme colorScheme, DialogTheme dialogTheme, FloatingActionButtonThemeData floatingActionButtonTheme, NavigationRailThemeData navigationRailTheme, Typography typography, CupertinoThemeData cupertinoOverrideTheme, SnackBarThemeData snackBarTheme, BottomSheetThemeData bottomSheetTheme, PopupMenuThemeData popupMenuTheme, MaterialBannerThemeData bannerTheme, DividerThemeData dividerTheme, ButtonBarThemeData buttonBarTheme, BottomNavigationBarThemeData bottomNavigationBarTheme, TimePickerThemeData timePickerTheme, TextButtonThemeData textButtonTheme, ElevatedButtonThemeData elevatedButtonTheme, OutlinedButtonThemeData outlinedButtonTheme, TextSelectionThemeData textSelectionTheme, DataTableThemeData dataTableTheme, bool fixTextFieldOutlineLabel, bool useTextSelectionTheme\}) → ThemeData

Creates a copy of this theme but with the given fields replaced with the new values. \[...\]

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

estimateBrightnessForColor(Color color) → Brightness

Determines whether the given Color is Brightness.light or Brightness.dark. \[...\]

lerp(ThemeData a, ThemeData b, double t) → ThemeData

Linearly interpolate between two themes. \[...\]

localize(ThemeData baseTheme, TextTheme localTextGeometry) → ThemeData

Returns a new theme built by merging the text geometry provided by the `localTextGeometry` theme with the `baseTheme`. \[...\]


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/material/theme_data.dart#L191
[theme_data.png]: https://flutter.github.io/assets-for-api-docs/assets/material/theme_data.png
[material_app_theme_data.png]: https://flutter.github.io/assets-for-api-docs/assets/material/material_app_theme_data.png
[material.io_design_color]: https://material.io/design/color/
[small fix]: https://github.com/flutter/flutter/issues/54028