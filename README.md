# javascript-bookmarklet
A group of javascript bookmarklets written by Nimityx

## Replace first youtube embed iframe with youtube-nocookie
```javascript
javascript:(function() {document.getElementsByTagName("IFRAME")[0].src=document.getElementsByTagName("IFRAME")[0].src.toString().replace('youtube','youtube-nocookie');})()
```

## Replace all youtube embed iframe with youtube-nocookie, youtube URL prompted
1
```javascript
javascript:(function() {var x = document.querySelectorAll("iframe");var i;for (i = 0; i < x.length; i++) {x[i].src = "https://miniurl.id/norobots/youtube?autoplay=0&v=" + prompt("Please enter a youtube URL");}})()
```
2
```javascript
javascript:Array.prototype.slice.call(document.querySelectorAll('iframe')).map(function(el){var id = prompt("Please enter a youtube URL", ""); el.src = 'https://miniurl.id/norobots/youtube?autoplay=0&v=' + id;});
```

## Add noreferrer value on anchor text rel attribute
```javascript
javascript:(function() {var x = document.querySelectorAll("a");var i;for (i = 0; i < x.length; i++) {x[i].relList.add("noreferrer");}})()
```

## Prevent redirect
```javascript
javascript:(function() {window.onbeforeunload=null;})()
```

## Enable right-click
```javascript
javascript:void(document.oncontextmenu=null)
```
