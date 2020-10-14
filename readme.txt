POCSAG library + demo-application for si4432-based ISM modules
--------------------------------------------------------------

This arduino application can create and send send 512 bps
alphanumeric POCSAG-messages using si4432-based ISM transceivers.

It consists of:
- a library called "Pocsag", tne code to create an alpha-numeric
pocsag-message

- two demo-application to send pocsag-messages using si4432-based
RF-modules: one designed for general use use and a "ham" version 
using 430-440 Mhz.

The demo-application use the "RadioHead" arduino library:
http://www.airspayce.com/mikem/arduino/RadioHead/

Note that, as the RadioHead library by default does not allow
packets larger then 50 bytes, one line need to be changed in the
Readhead class before compiling the "pocsag" demo applications:

In the file libraries/RadioHead/RH_RF22.h:
#define RH_RF22_MAX_MESSAGE_LEN 50

Should be changed to:
#define RH_RF22_MAX_MESSAGE_LEN 512

Have fun!
