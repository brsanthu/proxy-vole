## Introduction ##
A Java library to auto detect the platform network proxy settings. The library provides some proxy setting search strategies to read the proxy settings from the system config (Windows, KDE, Gnome, OSX), browser config (Firefox, IE), or environment variables, ... and provides you an ready to use proxy selector.

Java wants to be "The Internet Programming" language and wants to stay relevant for desktop applications / the RIA market. This can only be achieved with painless out of the box internet connectivity.

## Motivation ##
Today more and more applications try to take direct advantage of internet connectivity and webservices to bring webcontent to your desktop. Java has very good network and internet connectivity with build in APIs for http, https, ftp and a webservices stack. But the first thing that you need, to use all this fantastic technology, is a working internet connection. And this is where Java lacks a lot in my opinion. When you develop an applet or an Java Webstart application the situation is quite good. The new Java Plugin will use the proxy settings and connections as used by the browser, but for standalone applications the situation is quite unsatisfactionary. You have to ask your users to twiddle with System Properties and every Java application has it's own way of setting proxy configuration. In business environments where you often can find proxy configuration scripts you are stuck.

## Current Situation ##
To set the proxy settings in Java you can use some (documented but hard to find) System Properties on application startup. At runtime you can use the `ProxySelector` API to configure the proxy settings. Java even comes with a system property to detect the system proxy settings automatically but this one is poorly documented and unreliable in its behaviour.

## The Solution ##
To provide network connectivity out of the box for you Java application you can use the Proxy - Vole library. It provides some strategies for autodetecting the current proxy settings. There are many configureable strategies to choose from. At the moment Proxy - Vole supports the following proxy detection strategies.

  * Read platform settings (Supports: Windows, KDE, Gnome, OSX)
  * Read browser setting (Supports: Firefox 3.x+, Internet Explorer; Chrome and Webkit use the platform settings)
  * Read environment variables (often used variables on Linux / Unix server systems)
  * Autodetection script by using WPAD/PAC (Not all variations supported)

## Project Status ##

The project is still evolving in it's feature set (IP6 support) but very stable and a lot of people use it already in production environments. Some feature are still missing or need improvement. Please see also the [Issue Tracker](http://code.google.com/p/proxy-vole/adminIssues).

## Dependencies ##
  * Java 1.5 but Java 1.6 is recommended
  * If you want to use WPAD / PAC scripts then you need the Apache [Rhino](http://www.mozilla.org/rhino/) Javascript engine on your classpath. (is included in the project)
This is only needed for Java 1.5. With Java 1.6 we use the javascript engine that is already bundled with the JRE6
  * On windows a dll with native code is used to read the IE proxy settings by invoking Winhttp API functions. So the `WinHttp` API is needed on Windows (Should be the case on all windows systems starting with Windows XP and newer)

## More documentation ##
For some simple usage examples look at the UsageExamples. If you need further information you can read the [JavaDoc](http://proxy-vole.googlecode.com/svn/trunk/proxy_vole/doc/api/index.html).

## Participation ##
I could need some help in a variety of areas. The following open items need to be addressed:

  * Help and feedback is also welcome for testing the library on different platforms and versions of Windows, KDE, Gnome, OSX, in 32 and 64bit environements...
  * Some help with the documentation would be great to. Give me hints what is unclear or needs improvement.
  * Good ideas, bugreports, patches and code contributions are always welcome too.

Have fun,

- Bernd Rosstauscher