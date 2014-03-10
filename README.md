NG-AUDIO
===

Play your sounds with an angular directive.

Description
---
The ngAudio module comes with two handy components, a **directive** for playing sounds using the dom, and a **service** for handling sound inside your code.

ngAudio Directive
-----
The ngAudio directive can be added to the dom as an element or an attribute. It has different effects depending on how you use it.

###Defining Sounds with the Directive

The ngAudio directive on an element is just like creating an audio element.

```html
<ngAudio src='mysound.mp3'>
</ngAudio>
```

Is exactly like

```html
<audio src='mysound.mp3'>
</audio>
```

Except it is now more powerful.

```html
<ngAudio src='mysound.mp3' volume='0.7' startAt='3'>
</ngAudio>
	<!-- You can't do that with just an audio tag-->
```

You can also apply an ngAudio tag to an existing audio elements for the same great futures on a native dom element.

```html
<audio ngAudio src='mysound.mp3' volume='0.7' startAt='3'>
</audio>
	<!-- You are good to go -->
```

###ngAudio Directive Supported Attributes
*none yet*

### Playing Sounds with the Directive

You can add the `ngAudio` attribute to any normal dom element. In this case, clicking the element will play the sound identified by the ngAudio attribute.

```html
<button ngAudio="mySound">
</button>
	<!--Clicking this will play a sound-->
```

ngAudio will first look for an audio or ngAudio element with an id equal to the value passed. If there is no element, it will try to load a file as though the value is a url.

```html
<button ngAudio="audio/mySound.wav">
</button>
	<!--Clicking this will play a sound-->
```

This is also OK.


Usage
-----

```html
<script src='lib/angular.js'></script>
<script src='lib/angular.audio.js'></script>

<audio id='click1'>
  <source src="audio/click.mp3" type="audio/mp3">
</audio>

<button ng-audio='click1'>Click me and a sound will play</button>

//No JavaScript required
```

Is it Really That Easy?
-----
It's really that easy.

Tested in:
Chrome