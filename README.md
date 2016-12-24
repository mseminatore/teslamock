# teslamock
Express app that mimics (or mocks) the Tesla REST API for local testing and experimentation.

## Tesla API Documentation

The Tesla REST API encapusulated by this library was documented through the collaboration of many Tesla owners.  Please
thank and support them for their efforts.  The current REST API documentation can be found at:

    http://docs.timdorr.apiary.io/

## Known Issues

1. Auth always succeeds
2. Model X not yet supported
3. No support for multiple vehicles
	
# teslamock.js

This sample is an Express app that mimics the Tesla servers and implements the full REST API surface area.  There is now a
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


