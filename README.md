# Arduino-example

The following is an example of creating a basic Arduino project using hardware from the Telus IoT Starter Kit. This project will use the Nucleo L496ZG microcontroller board and the X-NUCLEO-IKS01A2 sensor board to collect temperature data and display it on the Arduino IDE serial monitor using an example sketch file written by STMicroelectronics. Later, consider learning some of the basics of Arduino with videos from this [youtube playlist](https://www.youtube.com/watch?v=fJWR7dBuc18&list=PLGs0VKk2DiYw-L-RibttcvK-WBZm8WLEP).

- [Telus IoT Starter Kit](https://www.avnet.com/shop/us/products/avnet-engineering-services/aes-bg96-iot-sk2-g-3074457345636408150?INTCMP=tbs_low-power-wide-area_button_buy-your-kit)
- [Nucleo L496ZG microcontroller](https://os.mbed.com/platforms/ST-Nucleo-L496ZG/)
- [X-Nucleo IKS01A2 sensor board](https://www.st.com/en/ecosystems/x-nucleo-iks01a2.html)

![image](https://user-images.githubusercontent.com/53897474/166283647-21528042-ed2a-4b43-836f-c65470029f3d.png)
![image](https://user-images.githubusercontent.com/53897474/166283557-e5f2f534-3732-4d73-932f-d146ae28053c.png)

## Download Arduino IDE
-	Download the latest version of [Arduino IDE](https://www.arduino.cc/en/software) and install it. This quick tutorial uses `Arduino IDE 1.8.19`.

## Download the Microcontroller board library and configure board settings
-	Since the Arduino IDE does not natively support the Nucleo L496ZG microcontroller board, a library must be installed so that it can be used correctly. 
-	In the Arduino window, navigate to: `File > Preferences > Additional Boards Manager URLs`, and paste the following URL into the box:
    -	`https://raw.githubusercontent.com/stm32duino/BoardManagerFiles/main/package_stmicroelectronics_index.json`
    -	[Reference](https://www.youtube.com/watch?v=1x-aNEtag88)
-	In the Arduino window, navigate to: `Tools > Board > STM32 boards groups > Nucleo-144`.
-	In the Arduino window, navigate to: `Tools > Board part number > Nucleo L496ZG`.
-	Restart the Arduino IDE by closing and opening it again.
-	The microcontroller is now ready.

## Download the sensor board library
-	This tutorial uses the X-NUCLEO-IKS01A2 sensor board (shield). STMicroelectronics has created a library to make it easier to control this sensor board.
-	Navigate to the [Github repository](https://github.com/stm32duino/X-NUCLEO-IKS01A2), select: `Code > Download ZIP`.  
![image](https://user-images.githubusercontent.com/53897474/166289207-c7876312-11b9-488a-8efd-da08d5e5a840.png)
-	Unzip the ZIP file.
-	Move the unzipped folder into your Arduino `libraries` folder which can be found here: `C:\Users\Brian\Documents\Arduino\libraries`.
-	Restart the Arduino IDE by closing and opening it again.
-	The sensor board is now ready.

## Open example files
**Open the HelloWorld example sketch.**
-	In the Arduino window, navigate to: `File > Open`.
-	Navigate to the `examples` folder which can be found here: `C:\Users\Brian\Documents\Arduino\libraries\X-NUCLEO-IKS01A2-main\examples`.
-	This folder contains code examples of different functions for operating the sensor board. 
-	Open `X_NUCLEO_IKS01A2_HelloWorld` and open the subsequent `.ino` file.
-	This code reads sensor data and prints it to the Arduino serial monitor as a string.

**Upload the sketch to the L496ZG microcontroller**
-   Connect the Nucleo L496ZG microcontroller to your computer using a USB cable. Lights on the board should be on or blinking.
-	Navigate to: `Tools > Port`. There should be one device connected, showing `COM7` (your number may be different).
-	Verify that the microcontroller is connected by disconnecting and reconnecting it to the computer, checking to see that the `Port` status changes.  
![image](https://user-images.githubusercontent.com/53897474/166289876-b512629d-0c69-4771-b8ab-28f062b64d91.png)
-	Once connected successfully, upload the sketch by navigating to: `Sketch > Upload`. 

**View the data in the serial monitor.**
-	Navigate to: `Tools > Serial Monitor`.
-	At the bottom of the serial monitor window, change the baud rate to `115200`.  
![image](https://user-images.githubusercontent.com/53897474/166290335-3d5e060f-e6b2-4bd8-b298-06ed93312533.png)
-	New lines of data should be printed into the serial monitor every second.
-	That is the end of this quick example project! 

### Notes:
-	[Troubleshoot](https://support.arduino.cc/hc/en-us/articles/4403361259538-I-can-upload-a-sketch-but-the-IDE-serial-monitor-does-not-open-Windows-) if serial monitor is not working. 
