# DiGiVOR
DiGiCo OSC converter and formatter for getvor.app

DiGiVOR is only supported on MacOS currently. Testing has only been done on Apple Silicon using MacOS Monterey

## Install
Download and unzip DiGiVOR.zip, then move application to the computers application folder. (Unexpected performace may come up if placed somewhere else.)

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

On the master screen, click "Setup", "External Control", "Add Device", "DiGiCo Pad". Enter the name for the device, I.E. VOR, DiGiVOR, dope external recording software, etc... Enter your device's IP Address, followed by the send port and recicieve port. DiGiVOR's default ports are Send:8000 Recicive:9000. Once that is done make sure to enable the device. 

##### DiGiVOR and DiGiCo's iPad editor app cannot run at the same time per DigiCo's limitations. DiGiVOR only works with DiGiCo Pad configuration. Other OSC will NOT work with DiGiVOR.

#### DiGiVOR Setup
When DiGiVOR is open, set the Console IP and ports in the user input box. (Console Recicive Port in DiGiVOR would be the send port on the console.) Once user input has been inputted, click "Connect" and the console name should populate under DiGiVOR.

#### Vor Setup
Create two Cusome OSC intagrations. Intagration 1 will contain Control Group 1-9 fader levels and names as well as the current snapshot number and name. Intagration 2 will contain Control Group 10-12 fader levels and names. It is up to the user to specify and format these in Vor or to use the attached Vor file.


#### Troubleshooting
If the DiGiVOR does not connect, confirm your network settings are correct and your IP is in the same subnet as the DiGiCo Console. Also confirm that all network settings in DiGiVOR match the console.

If faders are not populating correctly, click the "Refresh Console" button. This will send a request to the console to repopulate all fields.
