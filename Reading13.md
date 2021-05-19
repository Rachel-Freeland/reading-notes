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
