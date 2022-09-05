# A list of some old SVG Bugs which are fixed in most browsers but not it Safari/Webkit
**While working on a project that uses a lot of SVG text and other features, we have encountered some browser specific bugs, mainly Safari/Webkit,
most are very old reported bugs and all of them already reported and fixed in Chromium.**



## SVG textLength not working correctly (Opened 2017, Chromium fixed 2017)

Safari - [Bug 171805: SVG textLength not working correctly](https://bugs.webkit.org/show_bug.cgi?id=171805)  
Chromium - [Issue 719522: SVG textLength not working correctly](https://bugs.chromium.org/p/chromium/issues/detail?id=719522)

In this specific bug (Just to prove a point) the soultion is super simple, it's an off-by-one calculation error, so I took the time to install a local webkit environment, and ported the extremely simple Chromium solution to the Webkit issue, and it works.  
All it's missing is fixing the tests.

*As a part of researching this bug I found another related bug - Webkit is taking trailing line break chars into account when calculating textLength.  
**TODO: Need to open a ticket or find an existing one***

[textLength off by one + trailing line break example Codepen](https://codepen.io/tombigel/pen/QWQQaGM)



## SVG Text non-scaling-stroke doesn't work (Opened 2014, Chromium fixed 2015)

Safari - [Bug 139322: Setting the "vector-effect" attribute in the SVG `<text>` tag to "non-scaling-stroke" has no effect](https://bugs.webkit.org/show_bug.cgi?id=139322)  
Chromium - [Issue 475203: SVG Text non-scaling-stroke doesn't work](https://bugs.chromium.org/p/chromium/issues/detail?id=475203)

[Text non scaling stroke example Codepen](https://codepen.io/tombigel/pen/wvjwWYZ)


## Layer content inside HTML in SVG foreignObject renders in the wrong place (Opened 2009, Chromium fixed 2018)

Safari - [Bug 23113: Layer content inside HTML in SVG foreignObject renders in the wrong place](https://bugs.webkit.org/show_bug.cgi?id=23113)  
Chromium - [Issue 771852: Self-painting PaintLayers underneath `<foreignObject>` do not position or size correctly](https://bugs.chromium.org/p/chromium/issues/detail?id=771852)

[foreignObject + video + clip example Codepen](https://codepen.io/tombigel/pen/qBodyPY)


## clip-path on `<text>` referenced via `<use>` in `<clipPath>` is ignored (Chromium fixed 2016)

Safari - *Couldn't find a ticket*  
Chromium - [Issue 604679: clip-path on `<text>` referenced via `<use>` in `<clipPath>` is ignored](https://bugs.chromium.org/p/chromium/issues/detail?id=604679)  
and [Issue 604677: `<text>` referenced via `<use>` in `<clipPath>` is ignored](https://bugs.chromium.org/p/chromium/issues/detail?id=604677)  

 *There is a ticket maybe related to this one [Bug 141929: Changing presentation attributes of shape referenced by `<use>` in `<clipPath>` breaks clipping](https://bugs.webkit.org/show_bug.cgi?id=141929)*
 
  ***TODO: Open a ticket.*** 
 
 [SVG Clip Path with `<use>` referencing a `<text>` doesn't show example Codepen](https://codepen.io/tombigel/pen/WNJbrLv)
  
 
