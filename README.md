# motobit

TODO: To use this package, go to https://pxt.microbit.org, click ``Add package`` and search for **motobit**.

### ~ hint

Not currently integrated into pxt.  It must be manually added.  This package is still under development and subject to changes.

### ~

## Usage

The package adds support for the **moto:bit** add-on board from SparkFun.

* [moto:bit](https://www.sparkfun.com/products/14213)
* [Shadow Chasis](https://www.sparkfun.com/products/13301)
* [Hobby Gearmotor](https://www.sparkfun.com/products/13302)
* [Wheel Pair](https://www.sparkfun.com/products/13259)
* [RedBot Sensor - Line Follower](https://www.sparkfun.com/products/11769)
* [ine Follower Array](https://www.sparkfun.com/products/13582)
* [RedBot Sensor - Mechanical Bumper](https://www.sparkfun.com/products/11999)
* [Servo Extention Cable](https://www.sparkfun.com/products/13164)

### Micro:bit Pins Used 

The following micro:bit pins are used for analog and digital sensors, motor driving:  

* ``P0`` -- Analog Input 0
* ``P1`` -- Analog Input 1
* ``P2`` -- Analog Input 2
* ``P8`` -- Digital Input/Output
* ``P12`` -- Digital Input/Output 
* ``P14`` -- Digital Input/Output
* ``P15`` -- Servo Motor
* ``P16`` -- Servo Motor
* ``P19`` -- motor driver - SCL
* ``P20`` -- motor driver - SDA 

### Set Motor Speed

To set the speed and direction for a motor, place the `|set motor|` block.
The block takes three parameters: motor select, direction, and speed.

* The motor select must be either `Left` or `Right`
* Direction must be either `Forward` or `Reverse`
* Speed is an integer value between `0` and `100`

```blocks
motobit.setMotor(motor.left/right, direction.forward/reverse, 0-100)
```

### Invert Motor Directon

When a motor turns opposite to the direction that was declared, the `invert` 
block may be used. The block accepts two parameters: motor select, and a 
boolean variable. When the boolean is set to `True`, the motor direction is 
inverted so that `Forward` no longer causes the motor to spin in `Reverse`, 
but rather `Forward`.

* The motor select must be either `Left` or `Right`
* Invert must be either `true` or `false`

```blocks
motobit.invert(motor.left/right, true/false)
```

### Enabling Motors

Regardless of the set motor speed, before the motors will turn on the switch on moto:bit
must be set to **"Run Motors"**, and the enable motors command must be set to `ON`

* Motor enable must be either `ON` or `OFF`

```blocks
motobit.enable(power.on/off)
```

## License

MIT

## Supported targets

* for PXT/microbit

```package
motobit=github:sparkfun/pxt-moto-bit
```