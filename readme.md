```
 SSSSS  kk                            tt
SS      kk  kk yy   yy nn nnn    eee  tt
 SSSSS  kkkkk  yy   yy nnn  nn ee   e tttt
     SS kk kk   yyyyyy nn   nn eeeee  tt
 SSSSS  kk  kk      yy nn   nn  eeeee  tttt
                yyyyy
```
======

# Skynet Hub

======

Allows you to connect a device (Computer, Raspberry Pi, etc.) to Skynet.im

It also provides a simple [plugin system](./plugins.md) to connect devices that would otherwise not be able to communicate with Skynet directly

[Here](https://www.npmjs.org/search?q=skynet-plugin) is a list of known plugins.


--------------------


## Installing

Clone the git repository, then:

```bash
$ npm install
$ node server.js
```

--------------------


## Subdevices

A Skynet hub can have subdevices attached to it.  A subdevice is a configured instance of a [plugin](./plugins.md).  It could be anything from a Philips hue lighting system to an arduino to a simple javascript function that just calls a shell script on the skynet hub itself.  

You can have as many subdevices on the hub as you wish, as long as hub has the plugin type installed that you want to use for your subdevice.


You message subdevices directly from skynet by sending a normal skynet message to the skynet hub and specifing:

```javascript
{
  devices: 'xxxxxx-uuid-of-a-skynet-hub-xxx',
  subdevice: 'living_Room_Lights',
  payload: { setState: {lightNumber: 1, on: true} }
}
```


LICENSE
-------

(MIT License)

Copyright (c) 2014 Octoblu <info@octoblu.com>

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
