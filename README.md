
![Creator logo](docs/creatorlogo.png)

# Led Controller application

## Overview
Led controller application runs on Ci40 board. One MikroE board acts as awalwm2m client to simulate button. Controller application acts as awalwm2m server and observes any button presses on MikroE board, and whenever there is a change, controller gets a notification for the same, and change led state to ON or OFF present on Ci40 board.

| Object Name     | Object ID      | Resource Name | Resource ID |
| :----           | :--------------| :-------------| :-----------|
| "Digital Input" | 3200           | "Counter"      | 5501        |

## Revision History
| Revision  | Changes from previous revision |
| :----     | :------------------------------|
| 0.9.1     | External Beta Trial Release    |

## Prerequisites
Prior to running button gateway application, make sure that:
- Awalwm2m server daemon(awa_serverd) is running.
- Awalwm2m bootstrap daemon(awa_bootstrapd) is running.

**NOTE:** Please do "ps" on console to see "specific" process is running or not.

## API guide

Led Controller documentation is available as a Doxygen presentation which is generated via the following process.

  1. Install [Doxygen ](http://www.stack.nl/~dimitri/doxygen/download.html): ```` sudo apt-get install doxygen````
  2. Generate the documentation:

        $ led-controller: mkdir build
        $ led-controller/build: cd build
        $ led-controller/build: cmake ../docs
        $ led-controller/build: make docs

The output can be found in the build/html directory and viewed by opening index.html with your web browser.

## Running Application on Ci40 board
Led Controller Application is getting started as a daemon. Although we could also start it from the command line as :

*$ led_controller*

Output looks something similar to this :
```
Led Controller Application

------------------------


Server session established


Defining flow objects on server

Waiting for constrained device 'ButtonDevice' to be up

Constrained device ButtonDevice registered

Button state has changed

Going to glow led on Ci40 board

Button state has changed

Going to off led on Ci40 board

Button state has changed

Going to glow led on Ci40 board

Button state has changed

Going to off led on Ci40 board
```
