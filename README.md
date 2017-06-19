# Stubby Arduino software

Arduino based source code for the [stubby project](https://hackaday.io/project/770-stubby-the-teaching-hexapod).

Original AVR code can be found [here](https://github.com/thebiguno/stubby)

Many of the files were removed and replaced for arduino specific for the described hardware above. I kept only the core logic for the reverse kinematics and some more like the serial protocol for calibration

Recommended using PlatformIO as a IDE

## Hardware

1. 2x [Adafruit 16-Channel 12-bit PWM/Servo Driver - I2C interface - PCA9685](https://www.adafruit.com/product/815) also can be found as a cheaper chinese on [Aliexpress](https://www.aliexpress.com/item/Smart-Electronics-PCA9685-16-Channel-12-bit-PWM-Servo-Driver-I2C-Interface-for-Arduino-Raspberry-Pi/32464046768.html?spm=2114.13010608.0.0.1lZ7kS)
2. 1x [Triple-axis Magnetometer (Compass) Board - HMC5883L](https://www.adafruit.com/product/1746). Cheaper chinese on [Aliexpress](https://www.aliexpress.com/item/GY-273-3V-5V-HMC5883L-Triple-Axis-Compass-Magnetometer-Sensor-Module-For-Arduino/32786802981.html). Note: a few years ago I bought 5 of these for 85 cents, I can't say why it was so absurdly cheap at that time
3. 1x [Arduino Nano ATMega328](https://www.aliexpress.com/item/Free-shipping-10PCS-Nano-3-0-controller-compatible-for-arduino-nano-CH340-USB-driver-NO-CABLE/32251038344.html?spm=2114.13010608.0.0.qYmkZa). I usually buy manu of these to base my projects. Planning on to migrate to Arduino Pro Mini (3v or 5v) to better power consumption
4. 18x [MG90S 9g Servos](https://www.aliexpress.com/item/Free-Shipping-10pcs-lot-Metal-gear-Digital-MG90S-9g-Servo-Upgraded-SG90-For-Rc-Helicopter-plane/32272693848.html?spm=2114.13010608.0.0.qYmkZa) This looks way better than the classic SG90 due to the metal gears for pratically the same cost
5. 1x [Bluetooth HC-05](https://www.aliexpress.com/item/HC05-HC-05-master-slave-6pin-JY-MCU-anti-reverse-integrated-Bluetooth-serial-pass-through-module/1738587842.html?spm=2114.13010608.0.0.2qeNLh) Hopefully upgrading to a [HM-10 BLE](https://www.aliexpress.com/item/Bluetooth-4-0-For-Arduino-Android-IOS-HM-10-BLE-CC2540-CC2541-Serial-Wireless-Module/32669503177.html?spm=2114.13010608.0.0.nJ18IQ) for Bluetooth-4 and low power consumption when it arrives from China
6. 1x [LM2596 Bulk converter](https://www.aliexpress.com/item/Free-shipping-Mini-Converter-Adjustable-DC-DC-Step-down-Power-Supply-Module-replace-LM2596/32379817867.html?spm=2114.13010608.0.0.nJ18IQ/) for the power source
7. 1x [2S BMS](https://www.aliexpress.com/item/2S-3A-Li-ion-Lithium-Battery-7-4v-8-4V-18650-Charger-Protection-Board-bms-pcm/32672245074.html?spm=2114.13010608.0.0.d0Zbne) for the power source
8. 2x 18650 batteries - be carefull with fake mah descriptions. Buy a better one around 2500~3200 mah from a trusted manufacturer such as LG or Samsung
9. 1x [HC-SR04](https://www.banggood.com/10Pcs-HC-SR04-Ultrasonic-Ranging-Sensor-Ultrasonic-Module-For-Arduino-p-942912.html?rmmds=myorder) future improvement?
10. 1x [Laser diode](https://www.banggood.com/10Pcs-DC-5V-5mW-650nm-6mm-Red-Copper-Head-Tube-Laser-Dot-Diode-Module-p-945069.html?rmmds=myorder) for future improvement?

## Libraries

1. [Adafruit-PWM-Servo-Driver-Library](https://github.com/adafruit/Adafruit-PWM-Servo-Driver-Library)
2. [Adafruit_Sensor](https://github.com/adafruit/Adafruit_Sensor)
3. [Adafruit_HMC5883_Unified](https://github.com/adafruit/Adafruit_HMC5883_Unified)
