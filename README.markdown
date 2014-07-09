# VideoSub: HTML5 Video with SRT Subtitles #

Version: 0.9.9, Last updated: 8/26/2012

Video subtitles are an accessibility problem. In many countries websites are required by law to offer reasonable accessibility features, and one would hope that video subtitles are considered "reasonable" in 2012.

While there is a W3C and WHATWG spec in the works, none of the major browsers fully supports the new track elements and the brand new WebVTT subtitle standard. And older browsers may support video tags, but have no built in way to show subtitles over HTM5 video at all.

VideoSub is an easy solution for this problem and will get out of the way if the track element references a subtitle file in the new WebVTT standard. 

More information and examples can be found here: [http://www.storiesinflight.com/js_videosub/index.html](http://www.storiesinflight.com/js_videosub/index.html)


## Features ##

*  Standards compliant - follows the draft specification for Media Text Associations. Just add <track> tags to your videos
*  No coding required - just include VideoSub on a page with video tags
*  No outside dependencies to other frameworks, contains a minified subset of the Ender framework
*  Handles multiple videos on a single page
*  Works with common .SRT subtitle files (WebVTT support for older browsers is planned as soon as there are standards compliant tools to create WebVTT files)
*  It will stay out of the way if the track tag references a subtitle file in the new WebVTT standard
*  Supports seeking in the video
*  Dispatches a 'subtitlechanged' event upon swapping out an old subtitle line with a new one


## Code ##

### JavaScript ###

	<script src="includes/videosub.js"></script>

### HTML ###

	<video controls="controls" width="320" height="176">
		<source src="jellies.mp4" type="video/mp4" /><!-- WebKit -->
		<source src="jellies.ogg" type="video/ogg" /><!-- Firefox / Opera -->
		<track src="jellies.srt" kind="subtitle" srclang="en-US" label="English" />
		Your browser does not support HTML5 video.
	</video>

That's all you need! There are NO outside dependencies.


## Release History ##

0.9.9 - (8/26/2012) Initial GitHub Release


## License ##
Licensed under the MIT license. The contained Ender framework is licensed under MIT - copyright 2012 Dustin Diaz & Jacob Thornton [http://ender.no.de/](http://ender.no.de/)
