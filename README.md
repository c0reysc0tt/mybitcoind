# mybitcoind
The Dockerfile builds Bitcoin Core in an Ubuntu 14.04 container.

NOTES
---------------------
This image is a proof of concept only.  For space reasons, it doesn't mount a volume for the blockchain.  It's based on Ubuntu:14.04 and Bitcoin Core has been compiled from scratch.

To run the image in interactive mode with a bash prompt:
```bash
docker run --name mybitcoind -it c0reysc0tt/mybitcoind /bin/bash
```

Testing from bash within the container should look something like this:
```bash
root@055619d7d030:/# bitcoind -version
Bitcoin Core Daemon version v0.15.99.0-a892218
Copyright (C) 2009-2017 The Bitcoin Core developers

Please contribute if you find Bitcoin Core useful. Visit
<https://bitcoincore.org> for further information about the software.
The source code is available from <https://github.com/bitcoin/bitcoin>.

This is experimental software.
Distributed under the MIT software license, see the accompanying file COPYING
or <https://opensource.org/licenses/MIT>

This product includes software developed by the OpenSSL Project for use in the
OpenSSL Toolkit <https://www.openssl.org> and cryptographic software written by
Eric Young and UPnP software written by Thomas Bernard.

root@055619d7d030:/# test_bitcoin
Running 272 test cases...

*** No errors detected
```
