This repository holds some information on an old cutting plotter that uses the DM/PL protocol.

There are sample files with geometric figures that plot correctly.


### Commands
* Start of print: `;:H A L0 ECN U V10`
* Pen Up: ` U`
* Pen down: ` D`
* Go to XY: `X,Y`
* End print: `@` (maybe need adding of ` U FlastX` in front, like ` U F1288 @`)
* Resolution: The resolution is 0.0254mm per step

Example for a square with 100mm edge length:
` ;:H A L0 ECN U V10 U6044,1208 D6044,1208 D6044,5208,2044,5208,2044,1208,6044,1208 U6044,1208 U0,0 U F6044 @`

### Compensation algorithm:

If there is sharp edges in a cut, the knife needs some space to turn properly. All edges < 90 degrees therefore can be expanded a little bit
Example:

* from `2337 | 2237`
* ADD `995 | 3408`
* ADD `1004 | 3414
* via `1024 | 3408`
* ADD `1028 | 3400
* to `2487 | 3794`

