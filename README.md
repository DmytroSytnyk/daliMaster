# daliMaster

This is an Arduino™ library to control your DALI lamps with the brand new [daliMaster](www.ebay.d) shield, with buit-in DALI bus supply system. b:boom::boom:m!

## Description

### What is DALI?

DALI (Digital Addressable Lighting Interface) is a powerful protocol to control lighting. Through DALI you can dimmer your led lamps, ask them status, recall a predefined scenario and so on. Of course, the ballast that powers your lamp must be DALI compatible and acts as a DALI slave. You want more information about DALI, don't you? I thinks this is not the right place for that but I'm gonna leave you some useful links to the bottom of this page.

### Can I use DALI with my Arduino™?

Well, the answer is YES.

### How?

With [daliMaster](www.ebay.d)! As the name suggests, that shield transforms your Arduino™ in a DALI master, acting as a bridge between I2C interface and DALI bus. This shield is powered by [LW14](http://shop.codemercs.com/media/files_public/okutobbwyxn/LW14_Datasheet.pdf) chip by [Code Mercenaries](https://www.codemercs.com/en/). Let's make an example to explain how it works.

## Getting Started

* Fit [daliMaster](www.ebay.d) on your Arduino™

* Make connections (You can find an example schema [here](www.ebay.d))
  * Connect your lamps to their ballasts
  * Connect your ballast to mains..be careful!
  * Connect your ballasts and [daliMaster](www.ebay.d) to DALI bus
  * Connect your AC/DC 24V power supply to mains and to [daliMaster](www.ebay.d)..again, be careful! The shield will do the rest in order to power DALI bus.

* If I'm right, now you should have all of lamps On. Let's turn them off.

* Connect Arduino™ to your computer.

* Download this library and load *daliMaster/examples/serialControl.ino*

 * Now open serial monitor, select 115000 as baudrate and write:
```
-b 0 0
```
If everything went well your lamps now are off. But we don't like darkness, so let's switch them on to the minimum:
```
-b 0 1
```
Cool! Let's push them to maximum:
```
-b 0 254
```
Easy, isn't it? Now you can modulate all lamps from 0 up to 254 with those simple commands. :thumbsup:

## Next

See more informations about serial commands [here](/) and [here](daliCommands.h). See also the following links to know more about DALI and LW14 commands.

## Useful links

### LW14
* [LW14 datasheet](http://shop.codemercs.com/media/files_public/okutobbwyxn/LW14_Datasheet.pdf)

### DALI
* [main commands](http://www.tanzolab.it/www/CM3-HOME_test/dali_commands.pdf)
* DALI international standard (English/French) [60929 © IEC:2006](http://jnhb.fszjzx.com/upload/biaozhun/pdf/IEC60929Y2006.PDF)

## Built With

* [Eclipse IDE for C/C++ Developers](https://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/lunar)
* [Arduino IDE](https://www.arduino.cc/en/main/software)

## Versioning

* v.1 First release 21/01/2018

## Credits

* **Code Mercenaries** - *Original Raspberry Pi library for LW14 Modules* - [LED-Warrior14](https://www.codemercs.com/en/33-led-warrior/270-led-warrior14-2)

* **Code Mercenaries** - *Original Raspberry Pi library for LW14 Modules* - [LED-Warrior14](https://www.codemercs.com/en/33-led-warrior/270-led-warrior14-2)

see the [CREDITS.md](CREDITS.md) file for details

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
