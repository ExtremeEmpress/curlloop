# curlloop
A 5 byte PoC for busylooping curl

## How to reproduce
Run the following on linux with the file "poc" :

``
$ socat -u FILE:poc TCP-LISTEN:12345,reuseaddr,fork
``

Access with curl:

``
$ curl mqtt://localhost:12345
``

Observe busyloop.
