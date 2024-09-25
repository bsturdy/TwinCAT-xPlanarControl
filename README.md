# AxisControl

## What is this repository for? ##

* xPlanarControl program in Beckhoff TwinCAT 3.1
* A sample PLC program that provides an xPlanar controlling object filled with methods and properties for manipulating an xPlanar system

## How do I get set up? ##

+ Minimum requirements (as tested) 
	* Visual Studio 2019
    * TwinCAT XAE Shell 3.1.4024.56

## How do I use this? ##

* xPlanarControl function block has references internally that link to the mover objects. These need to be linked in the NC. Once this link has been made inside of the NC, the methods can be called to control the axis. The function block does not need to be called directly
* Calling CyclicUpdate() every cycle is required. This method updates the internal state of the function block
* Include libraries for access to functions that are used internally.: 
- Tc3_Mc3PlanarMotion, 
- Tc3_Physics, 
- Tc3_XPlanarStandard, 
- Tc3_XPlanarUtility

## Who do I talk to? ##

* Beckhoff UK - Ben Sturdy