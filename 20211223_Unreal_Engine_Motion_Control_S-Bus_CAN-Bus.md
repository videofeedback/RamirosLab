# Unreal Engine Motion Control S-BUS and CAN-BUS Fundamentals


[![Youtube Teaser](https://github.com/videofeedback/RamirosLab/blob/main/images/CARD-MOTION-CONTROL.png)](https://www.youtube.com/watch?v=UsrVjOOhUB4?sub_confirmation=1)

https://www.youtube.com/watch?v=UsrVjOOhUB4

#### Unreal Engine Motion Control S-BUS and CAN-BUS Fundamentals

###### Unreal Engine Motion Control S-BUS and CAN-BUS
Today we start learning the fundamentals of S-BUS and CAN-BUS that we are going to use to control external devices from Unreal Engine.

Today we start with the fundamentals of the S-BUS and CAN-BUS protocol. 
Those are the tools that we are going to use to remote control our external equipment. 

The final goal is to have a brand agnostic open source motion control system. 
I am reverse-engineering DJI Protocol, but the plan is to do this with all the brands possible. 

Since DJI is the only brand with so much information for developers is that DJI is the first brand that I will focus on, but I am extending the offer to all the brands. Even if your company has its own remote control system, I think is beneficial to open the protocol for developers who wants to use your equipment for custom solutions.
If your company wants to be part of this open-source ecosystem, please contact me directly. 

I am not asking for freebies or asking for sponsorship, just technical details so we can include your equipment on the open-source ecosystem. 
If anyone wants to help to decode their preferred equipment, watch this video to understand how to reverse engineer their communication so you can later use this information for your system, and please share the information with the community.


----------------------------------------------------------------------

## DJI Documentation

##### This document was a key find to reverse engineer the DJI Ronin-S CAN Bus Protocol. Not everything match, but is close enough. 
Decoding the focus control was the first step, and that helps to decode the rest of the information.

[![Download PDF: DJI R SDK](https://github.com/videofeedback/RamirosLab/blob/main/images/DJI_R_SDK.png)](https://github.com/videofeedback/RamirosLab/blob/main/pdfs/DJI_R_SDK_Protocol_and_User_Interface_EN.pdf)
Download PDF: DJI R SDK (https://github.com/videofeedback/RamirosLab/blob/main/pdfs/DJI_R_SDK_Protocol_and_User_Interface_EN.pdf)



----------------------------------------------------------------------

## Workflow



![](https://github.com/videofeedback/RamirosLab/blob/main/images/workflow_01.png)

##### The workflow that we are using on these tutorials is intended to be as follw: Midi as controller with Unreal Engine's blueprints, and communicating via SerialCOM plugin to contral all manual position for motion control units.




![](https://github.com/videofeedback/RamirosLab/blob/main/images/pwm_ppm_workflow.png)

##### PWM (Pulse Width Modulation) and PPM (Pulse Position Modulation) is the last piece of control in the workflow. 
They can be controlled directly or inderectly through a S-Bus protocol and/or CAN Bus protocol. 


----------------------------------------------------------------------------

## S-Bus Protocol


![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_futaba_protocol.png)

##### The S-Bus Protocol as defined by FUTABA on their website.

----------------------------------------------------------------------------

## DJI Ronin-S S-Bus Direct control


![](https://github.com/videofeedback/RamirosLab/blob/main/images/sbus_direct_connection.png)

##### This is the setup for direct control of the DJI Ronin-S S-Bus.

----------------------------------------------------------------------------

## FlySky FS-IA6B


![](https://github.com/videofeedback/RamirosLab/blob/main/images/flysky_amazon.png)

##### The FlySky FS-IA6B is used for reverse engineer the S-Bus Protocol. The followed link is not affiliated.
(https://www.amazon.com/Flysky-Receiver-Antenna-Compatible-Transmitter/dp/B07GBQ94GZ/)

----------------------------------------------------------------------------


## DJI Forum (S-Bus)

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_dji_forum.png)

##### This DJI Forum's thread was very helpful to understand how DJI Ronin deals with the S-Bus protocol.
Link: (https://forum.dji.com/thread-167232-1-1.html)

----------------------------------------------------------------------------

## S-Bus inverted signal

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_inverted.png)

##### The S-Bus signal is inverted in relation with the industry standard UART communication. In order to read the signal with the standard UART library, the signal has to be inverted. A simple NPN transistor can be used to electrically reverse the signal. It would be nice to have a S-Bus library that doesn't needs to reverse the signal. In order to do this, the whole library has to be changed. STM32 libraries are easier to modify, but an Arduino library has to be re-written from scratch. 
This is a "nice to have" in the to do list.

----------------------------------------------------------------------------


## S-Bus Protocol Analyzer Setup

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_protocol_analyzer.png)

##### In order to communicate S-Bus with the DJI Ronin-S, you have to connect via the focus control wheel's S-Bus/CAN-Bus connector and move the selection to "S-Bus" position.

 Two protocol analyzers are used for this documentation.  One os the Selaea Logic 8, and the second one is the Digilent Analog Discovery with the Oscilloscope probes extension. 

----------------------------------------------------------------------------

## S-Bus Demo Setup with Saleae Logic 8

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_setup_saleae.png)

##### In order to communicate S-Bus with the DJI Ronin-S, you have to connect via the focus control wheel's S-Bus/CAN-Bus connector and move the selection to "S-Bus" position.

 Two protocol analyzers are used for this documentation.  One os the Selaea Logic 8, and the second one is the Digilent Analog Discovery with the Oscilloscope probes extension. 



----------------------------------------------------------------------------

## S-Bus #1 Google result

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_arm_result.png)

##### One of the biggest problems with the lack of documentation of the S-Bus protocol is that everyone depends heavely in "Dudes on the Internet"... and thte #1 Google result of "Futaba S-Bus Protocol" search is this "Dude on the internet", where the information is wrong. This is going to cause not only a lot of confusion for developers, but a lot of wasting time once they figure out that the information is wrong (if they didn't gave up at that point).

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_wrong.png)

The key wrong piece of data is the Startbyte is [00001111 (0x0F) Decimal = 15] instead of 11110000 (0xF0). This mistake hasn't been corrected on the original post and eded up being the #1 result in google to the query "Futaba S-Bus protocol". This is just a cautionary tale of just relying on Google search. 




----------------------------------------------------------------------------

## S-Bus String

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_protocol_long.png)

##### This is the complete string analyzed in the tutorial. 
  - 25 Bytes Total
  - Byte 1 = Sart Byte
  - Bytes 2-23 Non-Individual Data Bytes
    - Bytes 2-23 (22 Bytes) are divided by 16 = 11 Bits per Data representing 16 Channels.
  - Byte 24 = Individual Data Byte
  - Byte 25 = End Byte always (0x00)
   

![](https://github.com/videofeedback/RamirosLab/blob/main/images/s-bus_protocol_First.png)
##### On this image the first byte is decoded as 0x0F (Decimal 15) and the rest of the data is decoded taking 8 bits from the first Byte plus 3 bits from the second byte and so on. A total of 176 bits will be devided by 11 bits to have 16 Data channels. Note that is impossible to read the actual values without reconstructing the bit structure. 

(Even Parity bit + 2 Stop bits + Start bits in purple) are excluded/ignored for the final reading of information.

----------------------------------------------------------------------------




----------------------------------------------------------------------------

# CAN Bus Protocol

![](https://github.com/videofeedback/RamirosLab/blob/main/images/can-bus_bosch.png)

##### The CAN Bus protocol was introduced by the German company BOSCH in 1986. Is one of the most trusted protocols in the industry and is being used in every modern car, trucks and heavy duty equipment, the gaming industry, building automatation, manufacturing industry, robotics and space rockets. CAN Bus is one of the most documented protocols in the industry and protocol-wise, is very easy to analyze the electrical properties and data stream. 

##### This doesn't means that is the easiest protocol to read, since data is device-oriented, and depends on each manufacturer to release the method to decode their stream of data. On top of that, the protocol can also be encrypted, adding a layer of security but a potential layer of complication for reverse engineering a CAN-Bus device. Fortunatelley, not all the information is encrypted in the DJI protocol that we are going to analyze. 






----------------------------------------------------------------------------

Links:

JOIN THE DISCORD SERVER!!!: https://discord.ramiroslab.com

YOUTUBE: https://youtube.ramiroslab.com

CLUBHOUSE: @RAMIROMDO

SUPPORT THE CHANNEL BUYING NFTs: https://nft.ramiroslab.com/

SUPPORT THE CHANNEL WITH DONATIONS: 0x2BEf61929d96D1847c254994e048661Dd4Ca1167

#unrealengine #motioncontrol #cameratracking #vive #oculus #metaverse #realsense #lidar #dji #NFT
