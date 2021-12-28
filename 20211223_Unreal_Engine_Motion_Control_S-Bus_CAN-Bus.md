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


Links:

JOIN THE DISCORD SERVER!!!: https://discord.ramiroslab.com

YOUTUBE: https://youtube.ramiroslab.com

TWITTER: https://twitter.ramiroslab.com![yt_thumbm](https://user-images.githubusercontent.com/1794641/147593656-78f55400-a526-4a9b-91a2-ac559f505b96.jpg)


CLUBHOUSE: @RAMIROMDO

SUPPORT THE CHANNEL BUYING NFTs: https://nft.ramiroslab.com/

SUPPORT THE CHANNEL WITH DONATIONS: 0x2BEf61929d96D1847c254994e048661Dd4Ca1167

#unrealengine #motioncontrol #cameratracking #vive #oculus #metaverse #realsense #lidar #dji #NFT
