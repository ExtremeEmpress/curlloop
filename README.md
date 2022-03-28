# curlloop
A 5 byte PoC for busylooping curl - my first fuzzy finding.
Read more about my first steps into fuzzing in my blog: https://nyget.in/2022/03/28/my-first-fuzzy-finding-busyloop-in-curl/

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
