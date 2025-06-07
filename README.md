# DiGiVor

DiGiCo OSC converter and formatter for [getvor.app](https://getvor.app)

DiGiVor is only supported on MacOS currently. DiGiVor Supports MacOS Ventura and up. To view hardware requriements, please visit [docs.getvor.app](https://docs.getvor.app/vor/minimum-requirements-1080p)

## Install
visit [Releases](http://github.com/Brendenfriedel/DiGiVor/releases) and download the .pkg. When launched, you will need to go to System -> Privacy -> and scroll down and allow DiGiVor to open.

## Commands
| Name                       | Command                  |Argument |
| :--------------------------|:-------------------------|:--------|
|Output 1-24                 | /DiGiVor/Output/{number} |{Output Type} (ie CG, Input, etc), {Output Name}, {Output Level}, {Output Mute Status} |
|Console Info                | /DiGiVor/Output/Console  | {Console Name}, {Session Title} |
|Snapshot Info               | /DiGiVor/Output/Snapshots| {Snapshot Number}, {Snapshot Name} |

## Setup

#### DiGiCo Setup

On the master screen, click "Setup", "External Control", "Add Device", "DiGiCo Pad". Enter the name for the device, I.E. Vor, DiGiVor, dope external recording software, etc... Enter your device's IP Address, followed by the send port and receive port. These are configured in the main screen of DiGiVor. Once that is done make sure to enable the device, and that external control is enabled. 

#### DiGiVor Setup
When DiGiVor is open, set the Console IP and ports in the user input box. (Console Recicive Port in DiGiVor would be the send port on the console.) Once user input has been inputted, click "Connect" and the console name should populate under DiGiVor.

#### Vor Setup
To take advantage of of all available DiGiVor Outputs, you will need two "Cusome OSC" intergrations. Arguments send to both. By default, the second intergration will be the next port after the user input. I.E. If you configure Vor to recicive on port 8001, it will send on both port 8001 and port 8002.

##### iPad Setup
DiGiVor now offers iPad pass-through in order to still control the console while documenting. To set up iPad pass-through click "Adv Settings", enter the IP Address of the iPad, enter a send port for the iPad, and enter a receive port. Note, that these ports must not be the same as the console send and receive. On the iPad, enter the IP of the computer that resides in the same subnet as DiGiVor, enter the send port, enter the receive port, and click the console name. 

#### Troubleshooting
If the DiGiVor does not connect, confirm your network settings are correct and your IP is in the same subnet as the DiGiCo Console. Also confirm that all network settings in DiGiVor match the console.


Make sure commands were loaded for ipad_SDv2 or ipad_Q.

