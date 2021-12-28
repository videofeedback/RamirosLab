# Ramiro's Lab (YouTube Channel)

## Unreal Engine Serial Communication Plugin (Serial COM)

[![Youtube Teaser](https://github.com/videofeedback/RamirosLab/blob/main/images/CARD-serial-com_v2.png)](https://www.youtube.com/watch?v=ElM9EQVjR-8?sub_confirmation=1)

https://www.youtube.com/watch?v=ElM9EQVjR-8

#### New FREE plugin for Arduino enthusiasts and anyone who needs professional Serial Communication from and to Unreal Engine (4.25/4.26/4.27/5.0EA).
"Communication Serial Port (Serial Com)" Unreal Engine Plugin

###### I waited for almost a year for the UE4Duino plugin to be fixed (It wouldn't work natively in UE4.26 or UE4.27, and if you didn't have the right SDK's and Visual Studio installed it wouldn't compile either when trying to import the plugin.
The need for this plugin is bigger than ever for Virtual Production. 

Native support for Serial Communication is the biggest missing feature in Unreal Engine. Having access to the Serial Port you have access to literally any peripheral with the most documented communication protocol that you will ever find. 

Yes, I can hear the screams from Epic Games developers "Use the LiveLink library!!!"... I understand. But the LiveLink library is too big and complicated for my small brain. At engineering, we learn to: "KISS"... "Keep It Simple STUPID!" ... and the Serial Communication plugin is just that, a simple method to communicate via a Serial Port. 

Since all my motion control project are going to depend on that library, I was already planning to expand the plugin, and since the plugin was last touched almost two years ago, I decided to fork the UE4Duino plugin and add all the functionalities that I will need later inside that forked plugin. 
All my love and respect goes to Gryzly32/FuzionLabs(v1), and Rodrigo Villani (v2) for making this plugin in the first place and maintaining it.

Since I am doing so much work with the Serial Port, it only makes sense for me to fork this repo and add all the add-ons myself.

So, the new Plugin is called "Communication Serial Port" and short name is "Serial Com". The version starts at v3 because it is literally a fork of EU4Duino 2.2.5 plus some extra perks that I am adding to the plugin.

If you need early access to the beta test, please ask me. I have night builds that needs beta testers. 

Feel free to ask for future requests. Either way, here or at Gigthub.

Just to clarify one thing. This is NOT EU4Duino v3. The plugin identifier is "SERIALCOM" instead and you will not be able to replace the library 1-on-1. The functions are compatible, but you will have to replace each one of the functions by hand with the similar function if you have an old project build with EU4Duino.
If Rodrigo Villani decides to make a version 3 of EU4Duino, he will be able to continue that path. I am taking a new path. I hope that is clear.


##Official Documentation of Serial Com:

# Serial Communication Plugin for Unreal Engine
Serial Com Port Library for Unreal Engine 4 and Unreal Engine 5

-----------------------------------------------------------------------------

## Downloads:

[SerialCOM LATEST DOWNLOAD](https://github.com/videofeedback/Unreal_Engine_SerialCOM_Plugin)

-----------------------------------------------------------------------------

## "Serial COM" v3.0.0.4 (Beta) (Fork of UE4Duino)


[![](https://raw.githubusercontent.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/main/SerialCOM/images/serial_com_fork_02.png)](hhttps://raw.githubusercontent.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/main/SerialCOM/images/serial_com_fork_02.png)

## List of Functions:

[![](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_list_of_functions_01.png)](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_list_of_functions_01.png)



### Renamed Functions:
-----------------------------------------------------------------------------------
	UE4Duino v2.2.5				Serial COM v 3.0.0 (Beta)
	- Close Port 				- Close Serial Port
	- Flash Port 				- Flash Serial Port
	- Open Port 				- Open Serial Port
	- ----------				- (New) Open Serial Port with Flow Control
	- Open Port with Target			- (New) Open Serial Port with Target and Flow Control
	- Get Port Number			- Get Serial Port Number
	- Get Port Baudrate			- Get Serial Port Baudrate
	- Serial Port Open			- Is Serial Port Open?
	- Print 				- Serial Print
	- Print Line				- Serial Print Line
	- Line End to String			- Serial Line End to String
	- Write a Byte				- Serial Write Byte
	- Write Bytes				- Serial Write Bytes
	- Read a Bytes				- Serial Read Byte
	- Read a Float				- Serial Read Float
	- Read a Line				- Serial Read Line
	- Read a String				- Serial Read a String
	- Bytes to Float			- Serial Bytes to Float
	- Bytes to int 				- Serial Bytes to Int
	- Float to Bytes			- Serial Float to Bytes
	- Int to Bytes				- Serial Int to Bytes
  
  
  
### "Serial COM" v3.0.0 (Beta) RELEASE NOTES

- The "Serial COM" 3.0.0 Plugin now works nativelley in Unreal Engine 4.27/4.26/4.24 (PARTIAL SUPPORT WITH UE 5EA*) without having to re-build the project and possibly not be able to re-build for the lack of missing SDK's requirements. 
* Unreal Engine 5(Early Access) still requires to rebuild the plugin. UE5 is able to rebuild the plugin. Until a new method to rebuild the plugin for UE5 is available, this is the only version compatible with UE5.

- The new plugin will appear in your plugin list as "Communication Serial Port (Serial COM)". On your blueprints, is going to be listed in the "Communication Serial" category list instead of "UE4Duino". Search for "Arduino, Serial, Communication" will also show the results for these functions. 

- Added Flow Control from the last UE4Duino 2.2.5's Pull request from "SG1EmberWolf"(https://github.com/SG1EmberWolf) 
	- Added "Open Serial Port with Flow Control"
	- Added "Open Serial Port with Target and Flow Control"
  
  - The new module name changed from "UE4Duino" to "SERIALCOM". That also means that both plugins (potentially) can live together inside a blueprint without causing conflicts, but is not recommended.

- Internally, changed naming of "Serial.h" files includes name. This "Serial.h" is very popular in many libraries. To avoid possible future corruption and confusion, it was renamed to "SerialCom.h".

- The BETA version will continue to stay in BETA mode until no serious problems get reported and the final version will be 100% compatible with this release.

GITHUB REPOSITORY (this one): https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/

-----------------------------------------------------------------------------------------------------

Known Issues:
----------------------------

- "Serial COM" 3.0.0 will not be compatible with "UE4Duino" 2.2.5 because the library doesn't share the "UE4DUINO" name anymore, using its own new "SERIALCOM" identifier. Changing to this library will make the old EU4Duino modules in red, indicating that those components are not available anymore.
Solution: Each component can be replaced with the current version by replacing each one by hand. The replacement equivalent chart is available at:
https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port  (Modules lists comparison chart)

- Arduino doesn't connects again if you close the project without closing the port.
Solution:  Use the best practice of creating an "Event End Play" with "Close Serial Port" connected to the event. This is the cleanest solution for this problem and best practice. 
For more information, visit https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port where we describe the best practices for the use of this plugin.



## Opening Port Example

[![](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_opening_port_example_02.png)](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_opening_port_example_02.png)



## Blueprint Example

Each Zip file contains the correstpondent blueprint for each UE version. Drag and drop the .uasset (Blueprint) file to your project. Read the complete insturctions inside the "BLUEPRINT" folder of this plugin.

[![](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_blueprint_example_01.png)](https://github.com/videofeedback/Unreal-Engine-Plugin-Communication-Serial-Port/blob/main/SerialCOM/images/serialcom_blueprint_example_01.png)

----------------------------------------------------------------------------------------------------------


### Serial Communication Useful information:

["Serial Communication" (Wikipedia)](https://en.wikipedia.org/wiki/Serial_communication)

["Flow Control" (Wikipedia)](https://en.wikipedia.org/wiki/Flow_control_(data))

["Software Flow Control (XON/XOFF)" (Wikipedia)](https://en.wikipedia.org/wiki/Software_flow_control)

["Serial Communication" (Contec)](https://www.contec.com/support/basic-knowledge/daq-control/serial-communicatin/)

["Serial Communication" (Sparkfun)](https://learn.sparkfun.com/tutorials/serial-communication/all)

["Serial Communication" (Adafruit)](https://learn.adafruit.com/circuit-playground-express-serial-communications/what-is-serial-communications)

["RS-232 vs TTL Serial Communication" (Sparkfun)](https://www.sparkfun.com/tutorials/215)



----------------------------------------------------------------------------------------------------------



### Useful Lab Tools:

["USB to TTL Serial Cable" (Sparkfun)](https://www.adafruit.com/product/954)

["Arduino Uno Rev3" (Arduino.cc)](https://store-usa.arduino.cc/collections/boards/products/arduino-uno-rev3)

["Arduino Mega Rev3" (Arduino.cc)](https://store-usa.arduino.cc/collections/boards/products/arduino-mega-2560-rev3)

["Arduino Portenta H7 Lite Connected" (Arduino.cc)](https://store-usa.arduino.cc/collections/boards/products/portenta-h7-lite-connected)







-----------------------------------------------------------------------------------------------------
Ramiro Montes De Oca (Ramiro's Lab)

Discord: https://discord.ramiroslab.com

YouTube: https://youtube.ramiroslab.com

Github: https://github.ramiroslab.com

----------------------------------------------------------------------------------------------------

### Copyright Notice:

[MIT License](https://github.com/videofeedback/Unreal_Engine_SerialCOM/blob/main/LICENSE)

[Copyright (c) 2015 v1 FusionLabz/Gryzly32 (UE4Duino)](https://forums.unrealengine.com/t/ue4duino-arduino-to-ue4-plugin-release/28963)

[Copyright (c) 2017-2020 v2 Rodrigo Villani Pereira (UE4Duino)](https://forums.unrealengine.com/t/free-windows-only-ue4duino-2-arduino-com-port-communication/95217#post728834)

[Copyright (c) 2021-2022 v3 Ramiro Montes De Oca (SerialCOM) fork of (UE4Duino 2.2.5)](https://github.com/videofeedback/Unreal_Engine_SerialCOM/)


  



All the projects are going to be hosted at:
http://www.github.com/videofeedback/

SUBSCRIBE AND CLAIM YOUR FREE NFT!!!
- Step #1, Subscribe to this Channel
- Step #2, Claim your FREE NFT sending a private message with your Wallet ID to this YT Channel.
Or go to https://nft.ramiroslab.com/  and get up to 20 NFTs at $5 each to support the channel.
PS: If you are new to Crypto, waif for a tutorial, but send the private message to reserve your NFT.

NOTE:
THESE NFTs ARE GOING TO BE YOUR TICKET FOR SPECIAL CONTENT OF THIS CHANNEL.
EVERY NEW SUBSCRIBER CAN RECEIVE 1(ONE) FREE NFT.

Links:

JOIN THE DISCORD SERVER!!!: https://discord.ramiroslab.com

YOUTUBE: https://youtube.ramiroslab.com

TWITTER: https://twitter.ramiroslab.com

CLUBHOUSE: @RAMIROMDO

SUPPORT THE CHANNEL BUYING NFTs: https://nft.ramiroslab.com/

SUPPORT THE CHANNEL WITH DONATIONS: 0x2BEf61929d96D1847c254994e048661Dd4Ca1167

#unrealengine #motioncontrol #cameratracking #vive #oculus #metaverse #realsense #lidar #dji #NFT
