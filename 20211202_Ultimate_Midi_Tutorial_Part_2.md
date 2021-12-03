# "Ultimate MIDI Tutorial with Unreal Engine (PART 2)"

[![Youtube Teaser](https://github.com/videofeedback/RamirosLab/blob/main/images/yt_thumbm.jpg)](https://youtu.be/PNQPOruPuM8?sub_confirmation=1)


This is a Step-by-step tutorial of how to use one of the most underated MIDI functions (and also unknown), that allows us to have absolute precission control of our MIDI values.
You will need to have a compatible MIDI device with 360-Degree rotation knobs (Digital Encoder). An alternative to play along with this tutorial is to use a MIDI software to simulate the MIDI encoder,  (Pocket Midi will do: https://www.morson.jp/pocketmidi-webpage/)

If you are decided to buy a MIDI controller specifically suitable for Virtual Production, these are the one I recommend (None of these links are affiliated links), this is just a straightforward honest recommendation:

### UNDER $120 MIDI CONTROLLERS WITH 360-DEGREE DIGITAL ENCODERS KNOBS
------------------------------------------------------------------


Arturia BeatStep: https://www.amazon.com/Arturia-BeatStep-MIDI-Controller-Sequencer/dp/B00I88HPUO/

BEHRINGER USB (XTOUCHMINI): https://www.amazon.com/BEHRINGER-USB-Controller-Black-XTOUCHMINI/dp/B012CSKTYY/

Akai Professional MPD218: https://www.amazon.com/Akai-Professional-MPD218-Controller-Software/dp/B0116X17JW/

Arturia MiniLab MkII 25 Slim-Key Controller: https://www.amazon.com/Arturia-MiniLab-MkII-Slim-Key-Controller/dp/B01MSNIVKE/

AKAI Professional MPK Mini MK3: https://www.amazon.com/Professional-Keyboard-Controller-Production-Software/dp/B0886ZPWC8/



PART 1
------
"Ultimate, ultimate, ultimate MIDI Tutorial with Unreal Engine (PART 1)" Ul: https://www.youtube.com/watch?v=s_QxpvBqC_4


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
SUPPORT THE CHANNEL DONATING NFTs: 0x2BEf61929d96D1847c254994e048661Dd4Ca1167



#unrealengine #motioncontrol #cameratracking #vive #oculus #metaverse #realsense #lidar #dji #NFT



# Midi_Tutorial_Part2
MIDI Blueprint for Camera Control

## This is the repository for the Midi Tutorial (Part 2) Blueprint.

V2 FIXES: 
- Added "Default Values" seaparated from the active Float Values so both settings never mix each other.
- Added Focus and Focal Length Default Values
- Added Channel 2 Sun Macros (Latitude, Azimuth, Intensity)

Note: If you want to collaborate with changes, please fork this repo and let us know about the changes. Thanks.

## Warning
Only MIDI devices with 360-Degree digital encoders will be able to take advantage of this project. This blueprint uses exclusive function that takes advantage of infinite rotation knobs controllers. Here is a list of devices that will be able to work with this blueprint:


Arturia BeatStep: https://www.amazon.com/Arturia-BeatStep-MIDI-Controller-Sequencer/dp/B00I88HPUO/

BEHRINGER USB (XTOUCHMINI): https://www.amazon.com/BEHRINGER-USB-Controller-Black-XTOUCHMINI/dp/B012CSKTYY/

Akai Professional MPD218: https://www.amazon.com/Akai-Professional-MPD218-Controller-Software/dp/B0116X17JW/

Arturia MiniLab MkII 25 Slim-Key Controller: https://www.amazon.com/Arturia-MiniLab-MkII-Slim-Key-Controller/dp/B01MSNIVKE/

AKAI Professional MPK Mini MK3: https://www.amazon.com/Professional-Keyboard-Controller-Production-Software/dp/B0886ZPWC8/

The device has to be Re-Mapped to change the functionality from Default to Alternative or equivalent to each manufacturer. (Watch the tutorial for instructions).

Note of the author: I am aware that this is a big limitation, but this little unknown MIDI functionality is one of the most important to be exploded by Virtual Production. Alternatives like OSC controllers are an option that will be explored later, but the physical option that these digital encoders offers is without a doubt a remarkable feature. Look for "360-Degree" knobs or "Digital-Encoders". The list above is just an example of "Under $120" alternatives.


## Instructions
### 1) Create an Unreal Engine 4.27.1 "Virtual Production" project from templates.
### 2) Activate the MIDI plugin, and close Unreal Engine
### 3) Download the ZIP file of this Blueprint [MIDI_Connect_V2.ZIP](https://github.com/videofeedback/MIDI_Tutorial_Part2/blob/main/files/MIDI_Connect_V2.zip)
### 4) Unzip the content of this file into the "Content" folder of your project.
### 5) Re-Start the project

## 6) Place the Blueprint "MIDI_CONNECT_V2" Inside the project.

[![](https://github.com/videofeedback/MIDI_Tutorial_Part2/blob/main/images/Map_Preview.png)]

### 7) Change the following settings in the red box

[![](https://github.com/videofeedback/MIDI_Tutorial_Part2/blob/main/images/midi_connectV2_Settings.png)]

## - Replace "Arturia BeatStep" with your MIDI Device ID
## - On "Camera", Select the camera to be controlled.
## - Sun: Sellect (BP_Sky_Sphere, SkyLight and Sunlight) from your blueprint. If the selections are blank, that means that you don't have those elements available on this map. Make sure that you open the "/VprodProject/Maps/Main Map). Otherwise place those elements to control the Sun.


# WANTED! CINEMA CAMERA FUNCTIONS!

If you want to colaborate with this project, there are few things that we need to fix (or find to be more exact).
This list
- Currect Aperture
- Exposure Component
- Camera ISO
- Camera Shutter Speed
- Color Grading (Temp)
- Draw Debug Focus Plane

All these featurea can't be located at level blueprint. (I can't)... I'll appreciate your colaboration. 
Note: Yes, I can find those on the "Detail" tab of the CinemaCameraActor, but I need to grab those elements from a BLueprint. 
If you have a working solution, please make a blueprint and copy "File.uasset" and send it to videofeedback@gmail.com (Subject "WANTED") and a brief explanation of how did you found those elements.
Only five different alternatives will be accepted, but everyone can submit your solution and all the solutions will be shared with the community.
You will be rewarded with 50 (VideoFeedback's NFTs (https://opensea.io/collection/ramiroslabfirstedition) ) *

Your name or any desire information will be published to the Open Source community (if desire). 
I appreciate your contribution.


[![Wanted](https://github.com/videofeedback/MIDI_Tutorial_Part2/blob/main/images/wanted_v1.png)


*The VideoFeedback NFT project is attached to multiple projects. It doesn't represents a monetary value, but can be traded in the open market. Do not assume that these NFTs can be traded at any price. This is still a project and there is no economic promisses other that the NFT community is willing to trade.

Ramiro Montes De Oca (VideoFeedback) https://youtube.com/ramiroslab/



