https_tproxy
------------
transparent proxy gateway program that transmits http, https 
traffics into specific uplink http proxy.

```
GOMAXPROCS=4 https_proxy -in [::]:3128 -out gw.local:8080
```

If omitted, `in` defaults to :3128 by default to which port you'll
set the tproxy iptables rule. 
You can use HTTP_PROXY, HTTPS_PROXY environment variables to set
`out` uplink proxy.

```
HTTP_PROXY=http://gw_http.local:8080 HTTPS_PROXY=http://gw_https.local:8080 GOMAXPROCS=4 https_proxy
```

Quick how-to is [available](http://qiita.com/kwi/items/b7c770d6b92c16c334fb)
in Japanese.

License is BSD 3 clause license.


License
-------
Copyright (c) 2015, Hiroaki KAWAI
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
