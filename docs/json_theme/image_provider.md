[*description*][description]

# ImageProvider<T extends Object> class Null safety #

Identifies an image without committing to the precise final asset. This allows a set of images to be identified and for the precise image to later be resolved based on the environment, e.g. the device pixel ratio.

To obtain an ImageStream from an ImageProvider, call resolve, passing it an ImageConfiguration object.

ImageProvider uses the global imageCache to cache images.

The type argument `T` is the type of the object used to represent a resolved configuration. This is also the type used for the key in the image cache. It should be immutable and implement the `==` operator and the hashCode getter. Subclasses should subclass a variant of ImageProvider with an explicit `T` type argument.

The type argument does not have to be specified when using the type as an argument (where any image provider is acceptable).

The following image formats are supported: JPEG, PNG, GIF, Animated GIF, WebP, Animated WebP, BMP, and WBMP. Additional formats may be supported by the underlying platform. Flutter will attempt to call platform API to decode unrecognized formats, and if the platform API supports decoding the image Flutter will be able to render it.

## Lifecycle of resolving an image ##

The ImageProvider goes through the following lifecycle to resolve an image, once the resolve method is called:

1.  Create an ImageStream using createStream to return to the caller. This stream will be used to communicate back to the caller when the image is decoded and ready to display, or when an error occurs.
2.  Obtain the key for the image using obtainKey. Calling this method can throw exceptions into the zone asynchronously or into the callstack synchronously. To handle that, an error handler is created that catches both synchronous and asynchronous errors, to make sure errors can be routed to the correct consumers. The error handler is passed on to resolveStreamForKey and the ImageCache.
3.  If the key is successfully obtained, schedule resolution of the image using that key. This is handled by resolveStreamForKey. That method may fizzle if it determines the image is no longer necessary, use the provided ImageErrorListener to report an error, set the completer from the cache if possible, or call load to fetch the encoded image bytes and schedule decoding.
4.  The load method is responsible for both fetching the encoded bytes and decoding them using the provided DecoderCallback. It is called in a context that uses the ImageErrorListener to report errors back.

Subclasses normally only have to implement the load and obtainKey methods. A subclass that needs finer grained control over the ImageStream type must override createStream. A subclass that needs finer grained control over the resolution, such as delaying calling load, must override resolveStreamForKey.

The resolve method is marked as nonVirtual so that ImageProviders can be properly composed, and so that the base class can properly set up error handling for subsequent methods.

## Using an ImageProvider ##

 *link* 

Sample

The following shows the code required to write a widget that fully conforms to the ImageProvider and Widget protocols. (It is essentially a bare-bones version of the widgets.Image widget.)

*assignment*

    class MyImage extends StatefulWidget {
      const MyImage({
        Key key,
        @required this.imageProvider,
      }) : assert(imageProvider != null),
           super(key: key);
    
      final ImageProvider imageProvider;
    
      @override
      _MyImageState createState() => _MyImageState();
    }
    
    class _MyImageState extends State<MyImage> {
      ImageStream _imageStream;
      ImageInfo _imageInfo;
    
      @override
      void didChangeDependencies() {
        super.didChangeDependencies();
        // We call _getImage here because createLocalImageConfiguration() needs to
        // be called again if the dependencies changed, in case the changes relate
        // to the DefaultAssetBundle, MediaQuery, etc, which that method uses.
        _getImage();
      }
    
      @override
      void didUpdateWidget(MyImage oldWidget) {
        super.didUpdateWidget(oldWidget);
        if (widget.imageProvider != oldWidget.imageProvider)
          _getImage();
      }
    
      void _getImage() {
        final ImageStream oldImageStream = _imageStream;
        _imageStream = widget.imageProvider.resolve(createLocalImageConfiguration(context));
        if (_imageStream.key != oldImageStream?.key) {
          // If the keys are the same, then we got the same image back, and so we don't
          // need to update the listeners. If the key changed, though, we must make sure
          // to switch our listeners to the new image stream.
          final ImageStreamListener listener = ImageStreamListener(_updateImage);
          oldImageStream?.removeListener(listener);
          _imageStream.addListener(listener);
        }
      }
    
      void _updateImage(ImageInfo imageInfo, bool synchronousCall) {
        setState(() {
          // Trigger a build whenever the image changes.
          _imageInfo = imageInfo;
        });
      }
    
      @override
      void dispose() {
        _imageStream.removeListener(ImageStreamListener(_updateImage));
        super.dispose();
      }
    
      @override
      Widget build(BuildContext context) {
        return RawImage(
          image: _imageInfo?.image, // this is a dart:ui Image object
          scale: _imageInfo?.scale ?? 1.0,
        );
      }
    }

Implementers

 *  AssetBundleImageProvider
 *  FileImage
 *  MemoryImage
 *  NetworkImage
 *  ResizeImage
 *  ScrollAwareImageProvider

Annotations

 *  @optionalTypeArgs

## Constructors ##

ImageProvider()

Abstract const constructor. This constructor enables subclasses to provide const constructors so that they can be used in const expressions.

const

## Properties ##

hashCode → int

The hash code for this object. \[...\]

read-only, inherited

runtimeType → Type

A representation of the runtime type of the object.

read-only, inherited

## Methods ##

createStream(ImageConfiguration configuration) → ImageStream

Called by resolve to create the ImageStream it returns. \[...\]

@protected

evict(\{ImageCache? cache, ImageConfiguration configuration: ImageConfiguration.empty\}) → Future<bool>

Evicts an entry from the image cache. \[...\]

load(T key, DecoderCallback decode) → ImageStreamCompleter

Converts a key into an ImageStreamCompleter, and begins fetching the image. \[...\]

@protected

noSuchMethod(Invocation invocation) → dynamic

Invoked when a non-existent method or property is accessed. \[...\]

inherited

obtainCacheStatus(\{required ImageConfiguration configuration, ImageErrorListener? handleError\}) → Future<ImageCacheStatus>

Returns the cache location for the key that this ImageProvider creates. \[...\]

obtainKey(ImageConfiguration configuration) → Future<T>

Converts an ImageProvider's settings plus an ImageConfiguration to a key that describes the precise image to load. \[...\]

resolve(ImageConfiguration configuration) → ImageStream

Resolves this image provider using the given `configuration`, returning an ImageStream. \[...\]

@nonVirtual

resolveStreamForKey(ImageConfiguration configuration, ImageStream stream, T key, ImageErrorListener handleError) → void

Called by resolve with the key returned by obtainKey. \[...\]

@protected

toString() → String

Returns a string representation of this object.

override

## Operators ##

operator ==(Object other) → bool

The equality operator. \[...\]

inherited


[description]: https://github.com/flutter/flutter/blob/master/packages/flutter/lib/src/painting/image_provider.dart#L308