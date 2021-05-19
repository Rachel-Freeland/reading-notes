# Local Storage

## References

<cite><http://diveinto.html5doctor.com/storage.html></cite>

- Native applications such as OS provide an abstraction layer for storing and retrieving application-specific data like... preferences or runtime state.
- Values are stored as _key : pair_ values in the registry, INI, and XML files or wherver that particular platform provides.
- Cookies were invented were invented early in the history of the web and CAN be used for persistent local storage. HOWEVER, they have 3 cons:
  1. Cookies can slow down your web app because they needlessly transmit the same data over and over since they are included in every HTTP request
  2. Cookies, included with every HTTP request, send data unencrypted
  3. Limited to about 4 KB of data

## History of Local Storage Hacks

- Microsoft invented something called DHTML (Dynamic HTML) Behaviors which, as a group, encapsulate specific functionality or behavior on a page.
  - These behaviors enhance the behavior of an element in an HTML providing you a way to add a custom element to a web page. 
  - One such behavior was called _userData_
    - Allows a web page to store up to 64 KB of data per domain
    - Trusted domains can store up to 640 KB
- Flash cookies were a feature of Flash6 that was introduced by Adobe in 2002
  - a.k.a. _Local Shared Objeces_
  - Allowed storage of up to 100 KB of data per domain
- In 2007, Google launced an open source browser plug in called _Gears_
  - Provides an ***API (Application Programming Interface)*** to an embedded SQL database (based on SQLite).
  - Can store unlimited amounts of data per domain using the SQ: database tables


## HTML5 Storage

- Referred to as DOM Storage
- This is a way for web pages to store named key/value pairs locally on the client web browser
- This data persists even after you browse to another site, close your browser tab, exit the browser, or whatever...
- Unlike cookies, these stored key/value pairs are never transmitted to a remote server
- Can be accessed through a `localStorage` object on the global _window object_
- Before using HTML5 storage when using js, you should check whether the browser supports it

```js
function supports_HTML5_storage() {
  try {
    return 'localStorage' in windown && window['localStorage'] != null;
  } catch (e) {
    return false;
  }
}
```

- Another way to check is using Modernizr <http://diveinto.html5doctor.com/detect.html#modernizr>

```js
if(Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 
  // maybe try dojox.storage or a 3rd-party solution
}
```


