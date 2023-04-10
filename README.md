Bitcoin node on Nintendo Switch
=============

This tutorial will allow you to excute a complete Bitcoin node on Nintendo switch.

Prerequisites
---------------------

- A computer
- A Nintendo Switch (V1)
- A 1TB SD card (Less for a pruned node)
- [Ubuntu Bionic](https://download.switchroot.org/ubuntu/switchroot-ubuntu-5.0.0-2022-12-23.7z)
- The latest version of [Hekate](https://github.com/CTCaer/hekate/releases)
- A payload sending application for Switch
- [RCM jig](https://www.amazon.com/Switch-Nintendo-Modify-Archive-Simulator/dp/B09GVHZ5B1/ref=sr_1_5?crid=1U506NUGSW4OB&keywords=rcm+switch&qid=1681136130&sprefix=rcm+sw%2Caps%2C443&sr=8-5)

Let's start
---------------------

### Make sure that your switch is a V1

To make sure that a switch is modifiable you can go to this [site](https://ismyswitchpatched.com).

If your Switch is not patched you can continue this guide!

If your Switch is patched you can still use this guide however your Switch will require soldering which will not be covered by this guide. I'll let you do your own research on the subject.

### Put your Switch in RCM mode

Pour commencer il faut faire entrer votre Switch en mode RCM pour cela on va utilser le RCM jig :

1) Drag the jig on the [right port](https://github.com/Retropex/BitcoinOnSwitch/blob/main/Pitcures/Switch%20jig.jpeg) of the Switch.
2) Hold the `Vol+` button.
3) While holding the `VOL+` button and press the `Power` button.
4) Release all the buttons.

If your Switch turned on when you press the Power button, it may be that your jig is not pressed enough in the right port or that your Switch is patched.
If after released all the buttons, the screen of your Switch remained black, it is because the operation probably went well.

Now we are going to inject a payload!

### Inject payload

This part depends on your OS and the software you use.

Here is a list of those you can use:
-  [TegraRcmGUI](https://github.com/eliboa/TegraRcmGUI)(Windows)
-  [JTegraNX](https://github.com/dylwedma11748/JTegraNX)(Windows/macOS/Linux)
-  [NXloader](https://github.com/DavidBuchanan314/NXLoader)(Android)

Using the software you have chosen, you will have to inject the `Hekate` payload.

For most software, all you have to do is press a button to inject the payload. I'll let you refer to the documentation of the chosen software.

You should come across this screen:

<img src="Pitcures/hakate.png" width="50%" height="50%" />

### Prepare the SD card

**Be careful, all the data on your SD card will be erased, it is recommended to use an SD card specifically for this use.**

1) Insert the SD card into the Switch.
2) Go to `Tools` -> `Partition SD Card`.
3) Partition the SD card according to the needs of your node.
4) Unzip the `Ubuntu bionic` archive and copy it to the SD card. (You can remove the SD card without switching off the Switch)
5) Now go to `Tools` -> `Partition SD Card` -> `Flash linux`.
6) Finally go in `home` -> `Nyx options` -> `Dump Joy-con BT`
