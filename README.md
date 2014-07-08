lsocket
=======
from http://www.tset.de/lsocket/

lsocket - simple and easy socket support for lua

### What is it?

lsocket is a library to provide socket programming support for lua. It is not intended to be a complete socket api, but easy to use and good enough for most tasks. Both IPv4 and IPv6 are supported, as are tcp and udp, and also IPv4 broadcasts and IPv6 multicasts. Also, lsocket is almost nonblocking, meaning that nothing blocks except for nameserver lookups.

### What's new in version 1.1

lsocket.connect() is now also nonblocking, apart from nameserver lookups.
socket:status() method added to query sockets for errors (necessary because of non-blocking connect(), but also handy for other situations)
nicer SIGPIPE handling, using socket or send options where possible, and disabling SIGPIPE for the send/sendto operation only where options are not available.
the included rshttpd.lua example httpd library now supports keepalive connections.
### What's new in version 1.0.2

just 2 more examples, one http client and one http server, to illustrate the hoops you have to jump through in order to take advantage of the non-blocking nature of lsocket.
### What's new in version 1.0.1

enhance check of whether a nslookup is needed, should now cover all cases
modified select() to ignore closed sockets, also calling select() without open sockets and without timeout is now an error (instead of blocking forever).
added constant _VERSION, which contains the full version number for lsocket.
fixed an issue that would keep the Mac's from compiling this
some cleanup in the 5.1/5.2 compatibility department as suggested by lhf
### Documentation

[README][1]
lsocket README file
### Download

You can get lsocket-1.1 by clicking on this [link][2], or eventually by installing it from the luarocks repository. If you fetch it from here, the included README gives hints on how to build it.

### License

The lsocket module and all accompanying documentation and additional source code is released under the MIT/X11 license.

Copyright (c) 2013 Gunnar Zötl <gz@tset.de>

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
    
### Contact

If you have anything to say about this, comments, bug reports, whatever, feel free to email them to gz@tset.de


  [1]: http://www.tset.de/lsocket/README.html
  [2]: http://www.tset.de/downloads/lsocket-1.1-1.tar.gz
