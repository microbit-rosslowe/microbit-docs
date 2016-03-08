#uBit.buttonA

##Overview

##Message Bus ID

##Message Bus Events

##API
[comment]: <> ({"className":"MicroBitButton"})
##Constructor
<br/>
####MicroBitButton( <div style='color:#008080; display:inline-block'>uint16_t</div> id,  <div style='color:#008080; display:inline-block'>PinName</div> name)
#####Description
Constructor. Create a pin representation with the given ID.  MicroBitButton
#####Parameters

>  <div style='color:#008080; display:inline-block'>uint16_t</div> *id* - the ID of the new  MicroBitButton  object. 

>  <div style='color:#008080; display:inline-block'>PinName</div> *name* - the physical pin on the processor that this butotn is connected to. 
#####Example
```c++
 buttonA(MICROBIT_ID_BUTTON_A,MICROBIT_PIN_BUTTON_A); //a number between 0 and 200 inclusive 

```
<br/>
####MicroBitButton( <div style='color:#008080; display:inline-block'>uint16_t</div> id,  <div style='color:#008080; display:inline-block'>PinName</div> name,  <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> eventConfiguration)
#####Description
Constructor. Create a pin representation with the given ID.  MicroBitButton
#####Parameters

>  <div style='color:#008080; display:inline-block'>uint16_t</div> *id* - the ID of the new  MicroBitButton  object. 

>  <div style='color:#008080; display:inline-block'>PinName</div> *name* - the physical pin on the processor that this butotn is connected to. 

>  <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> *eventConfiguration*
#####Example
```c++
 buttonA(MICROBIT_ID_BUTTON_A,MICROBIT_PIN_BUTTON_A); //a number between 0 and 200 inclusive 

```
<br/>
####MicroBitButton( <div style='color:#008080; display:inline-block'>uint16_t</div> id,  <div style='color:#008080; display:inline-block'>PinName</div> name,  <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> eventConfiguration,  <div style='color:#008080; display:inline-block'>PinMode</div> mode)
#####Description
Constructor. Create a pin representation with the given ID.  MicroBitButton
#####Parameters

>  <div style='color:#008080; display:inline-block'>uint16_t</div> *id* - the ID of the new  MicroBitButton  object. 

>  <div style='color:#008080; display:inline-block'>PinName</div> *name* - the physical pin on the processor that this butotn is connected to. 

>  <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> *eventConfiguration*

>  <div style='color:#008080; display:inline-block'>PinMode</div> *mode* - the configuration of internal pullups/pulldowns, as define in the mbed PinMode class. PullNone by default.
#####Example
```c++
 buttonA(MICROBIT_ID_BUTTON_A,MICROBIT_PIN_BUTTON_A); //a number between 0 and 200 inclusive 

```
##isPressed
<br/>
####<div style='color:#FF69B4; display:inline-block'>int</div> isPressed()
#####Description
Tests if this Button is currently pressed. 
#####Returns
1 if this button is pressed, 0 otherwise.
#####Example
```c++
 if(uBit.buttonA.isPressed()) 
 print("Pressed!"); 

```
##setEventConfiguration
<br/>
####<div style='color:#FF69B4; display:inline-block'>void</div> setEventConfiguration( <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> config)
#####Description
Changes the event configuraiton of this button to the given value. All subsequent events generated by this button will then be informed by this configuraiton.
#####Parameters

>  <div style='color:#008080; display:inline-block'>MicroBitButtonEventConfiguration</div> *config* - The new configuration for this button. Legal values are MICROBIT_BUTTON_ALL_EVENTS or MICROBIT_BUTTON_SIMPLE_EVENTS.
#####Example
```c++
 // Configure a button to generate all possible events. 
 uBit.buttonA.setEventConfiguration(MICROBIT_BUTTON_ALL_EVENTS); 
 
 // Configure a button to suppress MICROBIT_BUTTON_EVT_CLICK and MICROBIT_BUTTON_EVT_LONG_CLICK events. 
 uBit.buttonA.setEventConfiguration(MICROBIT_BUTTON_SIMPLE_EVENTS); 

```
##~MicroBitButton
<br/>
####~MicroBitButton()
#####Description
Destructor for  MicroBitButton
____
[comment]: <> ({"end":"MicroBitButton"})