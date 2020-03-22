Open in LXC
===========

Start an LXC container wrapping a directory in the host.

Usage: `open-in-lxc <flags>`

Where:
  * `-n <name>`: container name (default LXD's choice)
  * `-i <image>`: LXD image to use (default latest Ubuntu LTS)
  * `-m <host_path:guest_path>`: mount host to guest (default $PWD:/home/host)
  * `-u <guest_user:guest_group:host_user:host_group>`: UID map (default ubuntu:ubuntu:current-uid:current-gid)
  * `-l <language:region:kb_layout:kb_model:tz>`: Locale (default host's configuration)
  * `-e`: Spawn an ephemeral container (gets destroyed when you exit the shell)

Calling `open-in-lxc` with no arguments will create a new Ubuntu LTS container
with the current directory mounted under `/home/host`, and log you into a shell
as user `ubuntu` in that container, in `/home/host`.



Requirements
------------

You must have LXD installed: `snap install lxd`



License
-------

MIT License:

Copyright 2020 Karl Stenerud

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
