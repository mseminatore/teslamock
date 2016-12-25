# teslamock

[![Version](http://img.shields.io/npm/v/teslamock.png)](https://www.npmjs.org/package/teslamock)
[![License](https://img.shields.io/npm/l/teslamock.svg)](https://github.com/mseminatore/teslamock/blob/master/LICENSE)

Express app that mimics (or mocks) the Tesla REST API for local testing and experimentation.

# Installation

In order to use the app and/or samples you must first download and install [NodeJS](http://nodejs.org).

An installable module for [npm](http://npmjs.org) is now available.  To download and install the library 
and all of its dependencies to a local project directory use the following:

    npm install teslamock

You may also install directly from the GitHub [source](https://github.com/mseminatore/teslamock).  Either 
download and unzip the source, or clone the repository.

>Remember, whether you install via npm, ZIP source or Git clone you must install the dependencies before using teslamock.

To install dependencies via npm, from the root level of the library directory type:

    npm install

This app is under development.  New features and bug fixes are being added periodically.  To ensure 
that you have the very latest version of teslamock and it's dependencies be sure to update frequently. To do so,
from your project directory type:

    npm update

## Tesla API Documentation

The Tesla REST API encapusulated by this library was documented through the collaboration of many Tesla owners.  Please
thank and support them for their efforts.  The current REST API documentation can be found at:

    http://docs.timdorr.apiary.io/

## Known Issues

1. Auth always succeeds
2. Model X not yet supported
3. No support for multiple vehicles
	
# teslamock.js

This is a simple Express app that mimics the Tesla servers and implements the full REST API surface area.  There is now a
web interface for this app.  Point your web browser to http://127.0.0.1:3000.

>Note: the app is still fairly basic and in many cases simply returns success results.  It does not validate input 
>parameters including the OAuth token and vehicleID.  Streaming is not yet emulated.  It does now track vehicle 
>state changes on the server.  The web interface does not yet allow for changing vehicle state values.

Note that at this time the sample uses the [JADE](http://www.npmjs.com/package/jade) templating engine.  Jade has recently
been renamed to [PUG](http://www.npmjs.com/package/pug).  The sample will be updated in a future release.  Until then you 
must explicitly npm install JADE under Express.

Usage:

    node teslamock.js [options]

    Options:
	
    -h, --help               output usage information
    -P, --port               port for the server (default: 3000)


