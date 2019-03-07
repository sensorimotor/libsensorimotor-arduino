# Sensorimotor-arduino

![Arduino Nano](doc/images/nano.jpg)

Sensorimotor-arduino is the arduino-library to control the sensorimotor boards.

## Documentation

For the full documentation, see the [documentation folder](doc/README.md) and the [example projects](example/README.md).

## Quick start:

### Installation

Clone this repository as a new folder called "SensoriMotor" under the folder named "libraries" in your Arduino sketchbook folder. Create the folder "libraries" in case it does not exist yet.

### Usage

To use the library in your own sketch, select it from Sketch > Import Library.

You can initialize a new Motorcord class like this:

```cpp
#include <sensorimotor.h>

// instantiate the motor cord
Motorcord motors;

void setup() {
	// find boards and configure them
	motors.init();
}

void loop() {
	// perform communication and control
	motors.apply(); // should be run at least twice per millisecond
}
```

this will automatically query for motors on the bus.

now you can use the motors class to access all connected motors:

```cpp
motors.get(id)
```
