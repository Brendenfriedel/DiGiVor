# DiGiVor

DIGIVOR IS NOT READY FOR COMMERCIAL USE. IT IS STILL IN BETA AS IT HAS NOT BEEN TESTED ON CONSOLES OTHER THAN SD10. IF YOU WOULD LIKE TO HELP BETA TEST, PLEASE REACH OUT. 


DiGiCo OSC converter and formatter for [getvor.app](https://getvor.app)

DiGiVor is only supported on MacOS currently. Testing has only been done on Apple Silicon using MacOS Monterey. To view hardware requriements, please visit [docs.getvor.app](https://docs.getvor.app/vor/minimum-requirements-1080p)

## Install
Download and unzip DiGiVor.dmg, then move DiGiVor4.0 to the computers application folder. (Unexpected performace may come up if placed somewhere else.)

## Commands
| Name                       | Command               |Byte   | Default Port  |
| :--------------------------|:----------------------| :-----|:--------------|
|Control Group Name CH 1-9   |/Control_Groups/Name/  | 1-9   | 53101
|Control Group Level CH 1-9  |/Control_Groups/Level/ | 1-9   | 53101
|Control Group Name CH 10-12 |/Control_Groups/Name/  | 10-12 | 53102
|Control Group Level CH 10-12|/Control_Groups/Level/ | 10-12 | 53102
|Current Snapshot Number     |/Snapshots/number      |Int    | 53101
|Current Snapshot Name       |/Snapshots/name        |String | 53101

## Setup

#### DiGiCo Setup

On the master screen, click "Setup", "External Control", "Add Device", "DiGiCo Pad". Enter the name for the device, I.E. Vor, DiGiVor, dope external recording software, etc... Enter your device's IP Address, followed by the send port and receive port. These are configured in the main screen of DiGiVor. Once that is done make sure to enable the device, and that external control is enabled. 

#### DiGiVor Setup
When DiGiVor is open, set the Console IP and ports in the user input box. (Console Recicive Port in DiGiVor would be the send port on the console.) Once user input has been inputted, click "Connect" and the console name should populate under DiGiVor.

#### Vor Setup
Create two Cusome OSC integrations. Integration 1 will contain Control Group 1-9 fader levels and names as well as the current snapshot number and name. Intagration 2 will contain Control Group 10-12 fader levels and names. It is up to the user to specify and format these in Vor or to use the attached Vor file.

##### iPad Setup
DiGiVor now offers iPad pass-through in order to still control the console while documenting. To set up iPad pass-through click "Adv Settings", enter the IP Address of the iPad, enter a send port for the iPad, and enter a receive port. Note, that these ports must not be the same as the console send and receive. On the iPad, enter the IP of the computer that resides in the same subnet as DiGiVor, enter the send port, enter the receive port, and click the console name. 

#### Troubleshooting
If the DiGiVor does not connect, confirm your network settings are correct and your IP is in the same subnet as the DiGiCo Console. Also confirm that all network settings in DiGiVor match the console.

If faders are not populating correctly, click the "Refresh Console" button. This will send a request to the console to repopulate all fields.

Make sure commands were loaded for ipad_SDv2 or ipad_Q.

#### Tested Console's
DiGiCo SD10
DiGiCo SD9
DiGiCo SD8
DiGiCo SD11i
DiGiCo Q225
