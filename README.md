# EmetgencyTempretureShutdown
Load shedding system based on wireless infrared temperature sensor readings

The MLX90614 infrared non-contact thermometer measures the temperature of an object in the range from -70 to +380°C with an accuracy of 0.5°C and transmits the data to the controller

The controller is in a housing with a screen showing the current temperature and the shutdown temperature. The buttons on the body change the shutdown temperature (by 1-2 degrees per step, taking into account the thermometer's accuracy of about 0.5 degrees).

The relay switches on or off when a certain temperature is reached and switches back when it drops.

If desired, it is possible to implement different logic for the behavior of the relay when the temperature sensor is triggered - shutdown with a delay, shutdown for a certain time, etc.

## Control interface
Control interface consist of 32 character LCD screen (16x2) and 6 buttons:

![General view on system components](https://github.com/Brabn/EmetgencyTempretureShutdown/blob/main/Wiring_diagram/EmetgencyTempretureShutdown.Interface.jpg)

	`t=27 C`  	– current temperature sensor readingsin Celsius 
	`max 200 C` 	– temperature limit for system operation. Can be changed by pressing `up` and `down` buttons
	`Auto` 		– Automatic or manual mode. In automatic mode relay automatically turns off when the target temperature is reached. In manual mode (`Manual` displayed on the screen), the relay is turned on and off manually by pressing the `left` (on) or `right` (off) buttons. Automatic mode is turned on and off by pressing the `select` button. When manually turning on/off the relay, the mode also switches to `Manual`
	`ON` 		– current relay state (`ON` or `OFF`)

## System parameters:
* Main controller		– Arduino Uno 
* Processor 			– 16 MGh, ATmega328P
* Controller memory		– 32 KB Flash + 2 kB SRAM + 1kB EEPROM
* IR receiver			– VS1838B
* Working frequency		– 38 KGh (940 µm)
* Temperature sensor 		–MLX90614
* Operational temperature	– -40..+125°C
* Measurement range		– -70..+380°C
* Measurement accuracy	– ±0.5°C
* Viewing Angle: 		– 90 °
* Relay power			 
    - 2.2 kW AC (220 V, 10A)
    - 300 W DC (30 V, 10A)
* Dimensions			
    - 60x90x30 mm (device body)
    - 10m (temperature sensor cable length)

## Components
* Controller Arduino UNO 
* 1 channel ralay 
* Temperature sensor MLX90614
* Power supply 9V 500mA

## Wiring diagram

![Emetgency Tempreture Shutdown wiring diagram](https://github.com/Brabn/EmetgencyTempretureShutdown/blob/main/Wiring_diagram/EmetgencyTempretureShutdown.Wiring_diagram.jpg)

## Further development of the system
- [ ] Increasing the number of temperature sensors and/or relays
- [ ] Increase relay power
- [ ] Disabling and enabling the relay according to the program
- [ ] Connection to a PC with output of parameters and controls
- [ ] Writing control programs for various OS (Windows, Android)
- [ ] Organization of data transfer using Bluetooth
- [ ] Recording readings on a memory card with subsequent processing on a PC
 
## Photos

![General view on system components](https://github.com/Brabn/EmetgencyTempretureShutdown/blob/main/Photos/EmetgencyTempretureShutdown.General_view.jpg)

![Main box with controller and control elements](https://github.com/Brabn/EmetgencyTempretureShutdown/blob/main/Photos/EmetgencyTempretureShutdown.Main_box.jpg)
 
 
