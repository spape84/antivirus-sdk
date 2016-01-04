# Antivirus Plugins for Kerio Products

Antivirus plugins for Kerio products are used for communication between Kerio products (Kerio Connect, Kerio Control) and external antivirus program.

## Supported versions and platforms

We successfully compiled it on Debian GNU/Linux 8 and Ubuntu 14.04 (Trusty)

* Kerio Connect 7.1 and newer

## Content

* `api/` -- The API a plugin must implement
* `clam/` -- ClamAV plugin
* `sample/` -- Skeleton of a new plugin

## How to compile

* Get CMake build tool.

			apt-get install cmake        
    
* Get Boost libraries. (Only for ClamAV plugin, not needed for sample.)

			apt-get install libboost-all-dev        

   **NOTE:** We tested versions 1.55
 
* Run `cmake .` inside plugin's source directory (where `CMakeLists.txt` resides) -- in `clam/` or in `sample/`.
* Build binary using `make`.

## Installation

Once you compile the plugin (`avir_*.so`), copy it to `/opt/kerio/mailserver/plugin/avserver/avirs/` and run the administration console. You may want to change the default settings in (`Antivirus -> Select antivirus... -> Options...`). Then start the plugin in the administration console.

See [ClamAV Kerio KB article](http://kb.kerio.com/article.php?id=282) for further instructions.

## Copyright

Copyright © 1997-2012 Kerio Technologies s.r.o.

Licensed and distributed under the New BSD License.

## License

    Copyright (c) 1997-2012, Kerio Technologies s.r.o.
    All rights reserved.

    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:
        * Redistributions of source code must retain the above copyright
          notice, this list of conditions and the following disclaimer.
        * Redistributions in binary form must reproduce the above copyright
          notice, this list of conditions and the following disclaimer in the
          documentation and/or other materials provided with the distribution.
        * Neither the name of the Kerio Technologies nor the
          names of its contributors may be used to endorse or promote products
          derived from this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
    ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
    WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
    DISCLAIMED. IN NO EVENT SHALL KERIO TECHNOLOGIES BE LIABLE FOR ANY
    DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
    (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
    LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
    ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
    (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
    SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

