# jscpp #

jscpp is a header-only C++ wrapper to the Javascript library JavaScriptCore.

## Simplifies the work ##

jscpp heavily simplifies the task of exposing C++ classes (or C structures, or basically anything) to Javascript. It takes care of callback functions, data type conversions and a lot of the more cumbersome parts of JavaScriptCore. It's extremely easy to expose already-written C++ classes to Javascript, and reqiuires very little code.

## jspkg - a package system (think Java classes or .NET) ##

Together with the wrapper jscpp comes an optional, simple, yet powerful, package system called jspkg. jspkg offers the possibility of writing libraries (or "packages"), for example to expose a C or C++ library.

jspkg will load the library dynamically (as a plugin) whenever a Javacript needs it.

## Why it's here ##

The idea behind jscpp and jspkg is to let people in very short time write wrappers that expose C and C++ libraries to Javascript, and that the community share these wrappers.

## Why you want it ##

If you want to expose your classes (or simple C code), and perhaps also a certain library to Javascript, jscpp and jspkg will let you do this in basically a couple of minutes for small classes.

Let's say you have written a wrapper for zlib, and a package called "zlib". To use the exposed functionality you will be able to do something like this:
```
Package.use("zlib");

var s = "text to compress";
var compressed = zlib.compress(s, zlib.HIGHEST);
```