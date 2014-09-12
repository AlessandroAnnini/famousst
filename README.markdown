# Famo.us package for Sublime Text
=======================

**[famo.us](http://famo.us/)** - official website

**[famousco.de](http://famousco.de/)** - first unofficial Famo.us resource website

## Installation

- Package Control: install the package "AngularJS Snippets"
- Manual: copy files to your Sublime Text User folder

## IMPORTANT

Completions won’t show in HTML unless you have added this line to your User.sublime-preferences:

	"auto_complete_triggers": [ {"selector": "text.html", "characters": "<"}, {"selector": "text.html meta.tag", "characters": " " } ]


Adds syntax highlighting and snippets to Famo.us for Sublime Text.

![](https://raw.githubusercontent.com/sun2rise/famous-atom/master/screenshots/famous-atom.gif)

![](https://raw.githubusercontent.com/sun2rise/famous-atom/master/screenshots/famnview.gif)

Contributions are greatly appreciated. Please fork this repository and open a pull request to add snippets, make grammar tweaks, etc.

Supported features
------------------

### Autocompletes

You can use autocompletes for Famo.us's variables and function in JavaScript and HTML scaffolding. See scoped-properties folder for more details.

If you type some prefix and press `ctrl` + `space`, you can use autocompletes in below.

#### JavaScript

```
Context
Engine
EventEmitter
EventHandler
OptionsManager
Modifier
RenderNode
Scene
Surface
Transform
View
ViewSequence

EventArbiter
EventFilter
EventMapper

FastClick
GenericSync
MouseSync
PinchSync
RotateSync
ScaleSync
ScrollSync
TouchSync
TouchTracker
TwoFingerSync

Matrix
Random
Quaternion
Vector

Draggable
Lift
ModifierChain
StateModifier

CanvasSurface
ContainerSurface
ImageSurface
InputSurface
SubmitInputSurface
TextareaSurface
VideoSurface

CachedMap
Easing
MultipleTransition
SnapTransition
SpringTransition
Transitionable
TransitionableTransform
TweenTransition
WallTransition

KeyCodes
Timer
Utility

Deck
EdgeSwapper
Flipper
GridLayout
HeaderFooterLayout
Lightbox
RenderController
ScrollContainer
Scroller
Scrollview
SequentialLayout

NavigationBar
TabBar
ToggleButton

click
mousedown
mousemove
mouseup
mouseover
mouseout
touchstart
touchmove
touchend
touchcancel
keydown
keyup
keypress

inQuad
outQuad
inOutQuad
inCubic
outCubic
inOutCubic
inQuart
outQuart
inOutQuart
inQuint
outQuint
inOutQuint
inSine
outSine
inOutSine
inExpo
outExpo
inOutExpo
inCirc
outCirc
inOutCirc
inElastic
outElastic
inOutElastic
inBack
outBack
inOutBack
inBounce
outBounce
inOutBounce
```

### Snippets

You can use snippets in HTML and JavaScript. See snippets folder for more details.

If you type prefix and press `tab`, It will be replaced by snippet for it.

#### HTML

##### famsca

Famo.us HTML scaffolding

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>famo.us App</title>
        <meta name="viewport" content="width=device-width, maximum-scale=1, user-scalable=no" />
        <meta name="mobile-web-app-capable" content="yes" />
        <meta name="apple-mobile-web-app-capable" content="yes" />
        <meta name="apple-mobile-web-app-status-bar-style" content="black" />

        <!-- shims for backwards compatibility -->
        <script type="text/javascript" src="http://code.famo.us/lib/functionPrototypeBind.js"></script>
        <script type="text/javascript" src="http://code.famo.us/lib/classList.js"></script>
        <script type="text/javascript" src="http://code.famo.us/lib/requestAnimationFrame.js"></script>

        <!-- module loader -->
        <script type="text/javascript" src="http://code.famo.us/lib/require.js"></script>

        <!-- famous -->
        <link rel="stylesheet" type="text/css" href="http://code.famo.us/famous/0.2.0/famous.css" />
        <script type="text/javascript" src="http://code.famo.us/famous/0.2.0/famous.min.js"></script>

        <!-- app code -->
        <link rel="stylesheet" type="text/css" href="css/app.css" />
        <script type="text/javascript">
            require.config({baseUrl: 'src/'});
            require(['main']);
        </script>

    </head>
    <body></body>
</html>

```

##### fambox

famousBox.js fast but unofficial and UNSUPPORTED scaffolding (use this only for test apps) see http://famousco.de/how-to/ for details.

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>famo.us App</title>
        <meta name="viewport" content="width=device-width, maximum-scale=1, user-scalable=no" />
        <meta name="mobile-web-app-capable" content="yes" />
        <meta name="apple-mobile-web-app-capable" content="yes" />
        <meta name="apple-mobile-web-app-status-bar-style" content="black" />

        <!-- http://famousco.de/ all-in-one famous lib -->
        <script type="text/javascript" src="http://famousco.de/fiddle/famousBox.js"></script>

        <!-- your css -->
        <!-- <link rel="stylesheet" type="text/css" href="style.css" /> -->

        <!-- your app -->
        <!-- <script type="text/javascript" src="main.js"></script> -->

    </head>
    <body></body>
</html>

```

#### JavaScript

######Snippet syntax <br>

`fam + <d|n|t|e> + name` where: <br>`d` stands for 'dependency', <br>`n` stands for 'new', <br>`t` stands for 'timer', <br>`e` stands for 'example' <br> and `name` is the same name as Famo.us object lowcase.<br><br>

| Layouts           | Names         |
|-------------------|:-------------:|
| HeaderFooterLayou |  'famnhflay'  |
| GridLayout        | 'famngridlay' |
| FlexibleLayout    | 'famnflexlay' |
| SequentialLayout  | 'famnseqlay'  |

<br> others are like:`fam + name`<br><br>

##### famdengine

```
var Engine = require('famous/core/Engine');
```

##### famdview

```
var View = require("famous/core/View");
```

##### famdsurface

```
var Surface = require('famous/core/Surface');
```

##### famdimagesurface

```
var ImageSurface = require('famous/surfaces/ImageSurface');
```

##### famdinputsurface

```
var InputSurface = require('famous/surfaces/InputSurface');
```

##### famdstatemodifier

```
var StateModifier = require('famous/modifiers/StateModifier');
```

##### famdmodifier

```
var Modifier = require('famous/core/Modifier');
```

##### famdscene

```
var Scene = require('famous/core/Scene');
```

##### famdrendernode

```
var RenderNode = require('famous/core/RenderNode');
```

##### famdtransform

```
var Transform = require('famous/core/Transform');
```

##### famdtransitionable

```
var Transitionable = require('famous/transitions/Transitionable');
```

##### famdhflay

```
var HeaderFooterLayout = require('famous/views/HeaderFooterLayout');
```

##### famdgridlay

```
var GridLayout = require('famous/views/GridLayout');
```

##### famdflexlay

```
var FlexibleLayout = require('famous/views/FlexibleLayout');
```

##### famdseqlay

```
var SequentialLayout = require('famous/views/SequentialLayout');
```

##### famdflipper

```
var Flipper = require('famous/views/Flipper');
```

##### famddeck

```
var Deck = require('famous/views/Deck');
```

#### famdtimer
```
var Timer = require('famous/utilities/Timer');
```

##### famdgenericsync

```
var GenericSync = require('famous/inputs/GenericSync');
```

##### famdmousesync

```
var MouseSync = require('famous/inputs/MouseSync');
```

##### famdtouchsync

```
var TouchSync = require('famous/inputs/TouchSync');
```

##### famdscrollsync

```
var ScrollSync = require('famous/inputs/ScrollSync');
```

##### famgenericsync

```
GenericSync.register({
    'mouse': MouseSync,
    'touch': TouchSync,
    'scroll': ScrollSync
});
```

##### famnsurface

```
var $1 = new Surface({
    size: [undefined, undefined],
    content: '',
    classes: [],
    properties: {
        color: 'white',
        textAlign: 'center',
        backgroundColor: '#FA5C4F'
    }
});
```
#### famnview
```
define(function(require, exports, module) {
    var View = require('famous/core/View');
    var Engine = require('famous/core/Engine');
    var Surface = require('famous/core/Surface');
    var Transform = require('famous/core/Transform');
    var RenderNode = require('famous/core/RenderNode');
    var StateModifier = require('famous/modifiers/StateModifier');

    $1.prototype = Object.create(View.prototype);
    $1.prototype.constructor = $1;

    $1.DEFAULT_OPTIONS = {

    };

    function $1(options) {
        View.apply(this, arguments);

        this._node = new RenderNode();
        this._node.add(new StateModifier()).add(new Surface());

        // -- ADD TO RENDER TREE
        this._add(this.nodeRoot);
    }

    module.exports = $1;
});
```

##### famnimagesurface

```
var $1 = new ImageSurface({
    size: [true, true],
    content: '/*url*/'
});
```

##### famninputsurface

```
var $1 = new InputSurface({
    size: [200, 100],
    placeholder: '',
    type: 'text' // or 'button'
});
```

##### famnstatemodifier

```
var $1 = new StateModifier({
  align: [0, 0],
  origin: [0, 0],
  transform: Transform.translate(0, 0, 0)
});
```

##### famnhflay

```
/* NEEDS EDITING */
var $1 = new HeaderFooterLayout({
    headerSize: $2,
    footerSize: $3
});

$1.header.add();
$1.content.add();
$1.footer.add();

//mainContext.add($1);
```

##### famngridlay

```
/* NEEDS EDITING */
var $1 = new GridLayout({
  dimensions: [$2, $3]
});

var surfaces = [];
// surfaces.push(new Surface());
$1.sequenceFrom(surfaces);

//mainContext.add($1);
```

##### famnflexlay

```
/* NEEDS EDITING */
var ratios = [1, 3, 5];
var $1 = new FlexibleLayout({
    ratios: ratios
});

var surfaces = [];
// surfaces.push(new Surface());
$1.sequenceFrom(surfaces);

//mainContext.add($1);
```

##### famnseqlay

```
/* NEEDS EDITING */
var $1 = new SequentialLayout({
    direction: 0
});
var surfaces = [];
$1.sequenceFrom(surfaces);
// surfaces.push(new Surface());
// mainContext.add($1);
```

##### famndeck

```
/* NEEDS EDITING */
var $1 = new Deck({
    itemSpacing: 10,
    transition: {
        method: 'spring',
        period: 300,
        dampingRatio: 0.5
    },
    stackRotation: 0.02
});
var surfaces = [];
$1.sequenceFrom(surfaces);
// surfaces.push(new Surface());
// mainContext.add($1);
```

##### famnrendernode

```
/* NEEDS EDITING */
// var surf = new Surface();
// var mod = new StateModifier();

var $1 = new RenderNode(mod);
$1.add(surf);

// $1.add(mod).add(surf);
// mainContext.add($1);
```

##### famtinterval

```
Timer.setInterval(function() {

}, $1);
```

##### famttimeout

```
Timer.setTimeout(function() {

}, $1);
```

##### famtevery

```
Timer.every(function() {

}, $1);
```

##### famtafter

```
Timer.after(function() {

}, $1);
```

##### famkeycodes

```
Engine.on('keypress', function(event) {
if (event.charCode >= KeyCodes['0'] && event.charCode <= KeyCodes['9']) {
    console.log('you hit a number');
} else {
    console.log('not a number');
}
```

##### famtransition

```
{ duration : $1, curve: Easing.linear }
```

##### fameswipe

```
/* !ONLY FOR EXAMPLE PURPOSE! */
var GenericSync     = require('famous/inputs/GenericSync');
var MouseSync       = require('famous/inputs/MouseSync');
var TouchSync       = require('famous/inputs/TouchSync');
GenericSync.register({'mouse': MouseSync, 'touch': TouchSync});

var options = {
    openPosition: -276,
    transition: {
        duration: 300,
        curve: 'easeOut'
    },
    posThreshold: 138,
    velThreshold: 0.50
};

var currentPos = new Transitionable([0, 0]);

var sync = new GenericSync(['mouse', 'touch'], {
    direction: GenericSync.DIRECTION_X
});
surf.pipe(sync);

function _handleSwipe() {
    sync.on('update', function (data) {
        var currentPosition = contentPos.get();
        contentPos.set(currentPosition + data.delta);
    }.bind(this));

    sync.on('end', (function (data) {
        var velocity = data.velocity;
        var position = contentPos.get();

        if(contentPos.get() > this.options.posThreshold) {
            if(velocity < -this.options.velThreshold) {
                this.slideLeft();
            } else {
                this.slideRight();
            }
        } else {
            if(velocity > this.options.velThreshold) {
                this.slideRight();
            } else {
                this.slideLeft();
            }
        }
    }).bind(this));
}

AppView.prototype.slideLeft = function() {
    this.pageViewPos.set(0, this.options.transition, function() {

    }.bind(this));
};

AppView.prototype.slideRight = function() {
    this.pageViewPos.set(this.options.openPosition, this.options.transition, function() {

    }.bind(this));
};
```

##### famboilerplate

```
define(function(require, exports, module) {
	// import dependencies
	var Engine = require('famous/core/Engine');
	var Modifier = require('famous/core/Modifier');
	var Transform = require('famous/core/Transform');
	var ImageSurface = require('famous/surfaces/ImageSurface');

	// create the main context
	var mainContext = Engine.createContext();

	// your app here
	var logo = new ImageSurface({
		size: [200, 200],
		content: 'http://code.famo.us/assets/famous_logo.svg',
		//classes: ['double-sided']
		properties: {
			'-webkit-backface-visibility': 'visible',
			'backface-visibility': 'visible'
		}
	});

	var initialTime = Date.now();
	var centerSpinModifier = new Modifier({
		origin: [0.5, 0.5],
		transform : function(){
			return Transform.rotateY(.002 * (Date.now() - initialTime));
		}
	});

	mainContext.add(centerSpinModifier).add(logo);
});
```

## LICENSE

The MIT License (MIT)