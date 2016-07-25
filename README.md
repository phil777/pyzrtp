# pyzrtp
Pythonic implementation of ZRTP (rfc 6189)

## Features
It is based on Python3, focused on protocol tampering and easy reuse.

Submodules in zrtp directory wrap cryptographic modules. Note that Skein, TwoFish, Elliptic Curves are not supported (yet). A submodule implements ZRTP parsing and unparsing.

It has sufficient flexibility to build a ZRTP "man-in-the-middle" attack, targetting weak implementations that do not check hvi value present in Commit message.

## Dependencies
AES is brought by PyCrypto.

## Sample endpoint
endpt.py implements a cacheless passive ZRTP agent. It does not support multistream mode nor preshared mode. Agent is based on asyncio, to be easily embedded in a larger asyncio SIP / websocket signalling program.
