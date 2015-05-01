## Change History ##

This page show a change history for all major changes done in new releases.
I use the following convention:<br>
<b><code>*</code></b> <code>=</code> Program change, <b>+</b> <code>=</code> new feature, <b>-</b> <code>=</code> removed feature<br>
<br>
<h3>Current Repository Version</h3>

+ We now support on Linux Gnome the dconf settings format<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=55'>issue 55</a> : Improved shExpMatch method<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=51'>issue 51</a> :	UnsatisfiedLinkError if dll was cleaned up by another instance that is closed.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=50'>issue 50</a> : Mixed white list with "local bypass" enabled<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=48'>issue 48</a> : Expiry date for redownload of pac script content was broken.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=47'>issue 47</a> : If no PAC selector is available ignore the whitelist settings (OSX only).<br>
<br>
<code>*</code> Preparing migration to Maven<br>
<br>
<h3>20131209</h3>

<code>*</code> Fixed issue with myIPAddress() returning 127.0.0.1 instead of the real address on linux<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=46'>issue 46</a> : Handle cleanup of temp files more robust<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=44'>issue 44</a> : Selecting bluetooth interface in OS/X 10.8<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=39'>issue 39</a> : Default timeout is used when fetching PAC script, causes 5 minute delay<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=38'>issue 38</a> : Detect invalid PAC scripts early and abort<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=36'>issue 36</a> : methods returned java.lang.String objects instead of JS strings<br>
<br>
<h3>20121203</h3>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=31'>issue 31</a> : Improved the support for "no proxy" definitions.<br>
<br>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=29'>issue 29</a> : KDE settings file was not found on KDE4. This is solved now.<br>
<br>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=25'>issue 25</a> : Disabled DTD and schema validation in settings parsers.<br>
<br>
<h3>20120920</h3>
<code>*</code> Improved the fix for <a href='https://code.google.com/p/proxy-vole/issues/detail?id=26'>issue 26</a>: PAC download recursion bug<br>
<br>
<h3>20120905</h3>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=26'>issue 26</a> : Implemented (hopefully) better fix for PAC download recursion bug<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=27'>issue 27</a> + 22 : JavaProxySearch was used always even if no http.proxyHost property was set.<br>
<br>
<h3>20120727</h3>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=19'>issue 19</a> : Added check to return null if no KDE settings are available.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=20'>issue 20</a> : Fix in isInNet method. Resolve host names to IP addresses.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=21'>issue 21</a> : Improved handling of empty/invalid URIs<br>
<br>
<h3>20111102</h3>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=14'>issue 14</a> : Added code to cleanup temporary dll files that were not deleted on VM exit.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=18'>issue 18</a> : Added code to support the https.proxy system properties too.<br>
<br>
<code>*</code> Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=9'>issue  9</a> : IE PAC file urls are now patched to be in line with Firefox URLs.<br>
<br>
+ Added support for automatic retry if PAC returns a list of fallback proxies.<br>
<br>
+ Started to implement IPv6 support<br>
<br>
<h3>20110515</h3>
+ Added (experiemental) support for Max OSX. This is not very well tested yet but should work.<br>
<br>
+ Fixed  <a href='https://code.google.com/p/proxy-vole/issues/detail?id=15'>issue 15</a> : The Firefox proxy search lacked support for socks proxy. This is now available.<br>
<br>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=12'>issue 12</a>: The PAC JavaScript method isInNet did not work for all patterns. This is fixed now.<br>
<br>
<h3>20110210</h3>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=11'>issue 11</a>: Parsing was unreliable when a PAC script returned more than one proxy<br>
<br>
<code>*</code> Some code cleanup to fix some minor problems (platform detection issues and others)<br>
<br>
+ Added a debug system property "com.btr.proxy.pac.overrideLocalIP" for the PAC parser<br>
<br>
+ Added Support for the IE "Bypass Proxy Server for local addresses" feature<br>
<br>
<br>
<h3>20100914</h3>
+ PAC support on Java 1.6 will now use the javax.script framework and the internal javascript engine that is shipped with JRE6. This will allow you to support PAC without bundling the Rhino engine which will dramatically reduce the footprint of the library.<br>
Java 1.5 will still be supported but then you need to bundle it with the Rhino engine.<br>
<br>
+ Added contributed dlls to support 64 windows version for the IE proxy detection.<br>
<br>
<code>*</code> Some fixes for the http client that is used to download PAC scripts from a webserver. We accept now all content-type send by the server and we support now different charsets for the scripts.<br>
<br>
<code>*</code> Fixed some unit tests that did not pass and did some other small fixes.<br>
<br>
<h3>20100724</h3>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=5'>issue 5</a>: PAC Parser was not working correctly in multithreaded environments. <br>

<h3>20100411</h3>
<code>*</code> Fixed <a href='https://code.google.com/p/proxy-vole/issues/detail?id=4'>issue 4</a>: Improved parser used to parse proxy urls from environment varibales and other places  <br>

<h3>Older</h3>
Did not track changes for older releases