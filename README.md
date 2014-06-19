# About x-camera
A X-Tag based Web Component to access a camera using `getUserMedia`.

## Methods
### play()
The `play` Method simply starts video streaming.

### pause()
The `pause` Method stops streaming.

## Attributes
### videowidth
`videowidth` sets the width of `<video>`

### videoheight
`videoheight` sets the height of `<video>`

## Events
`canplay` will be fired when video is ready to play.

# Example

```
<!-- basic -->
<x-camera></x-camera>

<!-- do not start streaming -->
<x-camera play="false"></x-camera>

<!-- set videoCanvas size to width/height (defaults to 480x320) -->
<x-camera videowidth="480" videoheight="320"></x-camera>

<!-- hide internal video element -->
<x-camera video="hidden"></x-camera>

```

The component asks for permission for the camera and renders the video. If you just want to access the Video
Canvas you could get it as described below:

```
document.addEventListener('DOMComponentsLoaded', function(){
    var myVideo = document.querySelector('x-camera'); // Or use an id.
    var videoCanvas = myVideo.videoCanvas;
});
```
 Just take a
look at `demo-canvas.html`.

# Download it



# Dev Setup

```
Fork this repo, rename it, then clone it.

$ npm install	// install bower tasks
$ bower install	// install components
$ grunt build   // build
$ grunt bump-push  // bump the version number, tag it and push to origin master

```



# Links

[Yeoman X-Tag Generator](https://github.com/x-tag/x-tag-generator)

[X-Tags Docs](http://x-tags.org/docs)

[Guide for creating X-Tag Components](https://github.com/x-tag/core/wiki/Creating-X-Tag-Components)

[Using X-Tag components in your applications](https://github.com/x-tag/core/wiki/Using-our-Web-Components-in-Your-Application)


