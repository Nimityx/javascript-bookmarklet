# javascript-bookmarklet
Javascript bookmarklets written by Nimityx

## Replace first youtube embed iframe with youtube-nocookie
```javascript
javascript:(function() {document.getElementsByTagName("IFRAME")[0].src=document.getElementsByTagName("IFRAME")[0].src.toString().replace('youtube','youtube-nocookie');})()
```

## Replace all iframe with youtube-nocookie, youtube URL prompted
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

## Deploy Watch Proxy on current tab
```javascript
javascript:((function(){var a,b,c;c='https://miniurl.id/zzwkso4lxci88v0esjb9jgut7drqj77x',b=document.createElement('iframe'),b.setAttribute('src',c),b.setAttribute('frameborder','0'),b.setAttribute('allowfullscreen','true'),b.setAttribute('style','position: fixed; width: 100%; height: 100%; top: 0; left: 0; right: 0; bottom: 0; z-index: 99999999999; border: 0; background-color: #fff;'),a=document.getElementsByTagName('body')[0],a.appendChild(b)})).call(this)
```

## Prevent redirect
```javascript
javascript:(function() {window.onbeforeunload=function() {return "Prevented";}})()
```

## Enable right-click
```javascript
javascript:void(document.oncontextmenu=null)
```
