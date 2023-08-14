# OPPO A37fw Rooting Guide

**FOR OPPO A37FW ONLY (NOT A37 AND NOT A37F AND NOT FOR ANY DEVICES)**

**I DO NOT OWN ANYTHING AND THIS GUIDE IS JUST MY EXPERIENCE IN ROOTING AND FOR THOSE WHO HAD HARD TIME TO ROOT THEIR A37FW DEVICES LIKE ME, I AM NOT RESPONSIBLE TO ANY DAMAGE YOU GOT, SO TAKE IT AS YOUR OWN RISK.**

## System Requirements

- OS: Windows 10 or 11
- Disabled Driver Signature Enforcement

## Preparing

- USB Drivers: [Qualcomm](https://gsmusbdrivers.com/download/android-qualcomm-usb-driver/) or [Quectel](https://gsmusbdriver.com/install-quectel-usb-driver)
- [QFIL/QPST](https://androidmtk.com/download-qpst-flash-tool) *Use the latest version `v2.7.496`*
- [Stock ROM](https://firmwareos.com/oppo-a37f) *Use the `A37fEX_11_A.07_160614` build number(16xxxx is rooting possible)*
- [vibrateonly fix](https://github.com/diamant3/oppo-a37fw-rootguide/blob/main/vibrateonly%20fix.zip) *You need this promise because we need to intentionally flash the wrong firmware to downgrade and this is the fix*

**They have their own guide in the links to install, please follow them correctly.**

## Downgrading

**As you can see, i am using `QFIL` instead of `Msm8x39DownloadTool.exe` because it's not detecting my device.**

1. Extract the `Stock ROM` and the `vibrateonly fix` and then start `QFIL` as an administrator.
2. Connect your device(A37FW) in EDL mode(just [`adb reboot edl`](#edl) it) to your PC and it will show the Connected COM Port in `QFIL`.
    - If not showing up just click the `Select Existing Port` button and click the COM PORT showed in the textbox and click `OK`.
    - If not showing up in Select port window, check the checkbox `Show Non QDLoader\DIAG Port` to show the COM PORT and click the COM PORT showed and click `OK`.
3. In your `QFIL`, choose the `Flat Build` Build Type.
4. In your `QFIL`, click `Browse` button and then load the `prog_emmc_firehose_8936.mbn`.
5. In your `QFIL`, click `Load XML...` button and then load the `rawprogram0_MSM_15399.xml` and `patch0.xml`.
6. click `Download` button and it will show a blue progress bar and scrolling text in the textbox it means the `QFIL` are currently flashing your device with a stock ROM and **do not disconnect your device**, you need to see in textbox the `Finished Download` or `Succeeded` something like that. Disconnect the cable if `Finished Download` or `Succeeded`.
7. As you can see and feel, it's just vibrate but don't worry! You need the `vibrateonly fix`. Copy the content of the `vibrateonly fix` and then paste it inside to the directory where your stock ROM located and then click the `Replace the file the destination`.
8. This is the critical part, open the back cover of your device and then remove the connection of the battery, press and hold the volume `+` and `-` buttons(BOTH) and then reconnect your usb cable to your PC and it will show up again in the `QFIL` your COM PORT.
9. In your `QFIL`, choose the `Flat Build` Build Type.
10. In your `QFIL`, click `Browse` button and then load the `prog_emmc_firehose_8916.mbn`(NOT `prog_emmc_firehose_8936.mbn`).
11. In your `QFIL`, click `Load XML...` button and then load the `rawprogram0.xml`(NOT `rawprogram0_MSM_15399.xml`) and `patch0.xml`.
12. click `Download` button and it will show a blue progress bar and scrolling text in the textbox it means the `QFIL` are currently flashing your device with patches and **do not disconnect your device**, you need to see in textbox the `Finished Download` or `Succeeded` something like that. Disconnect the cable if `Finished Download` or `Succeeded`. You will see and feel the vibration is gone and it fixed!
13. Long press the power button(5-10 seconds) and then boom, downgraded successfully! 🥳

## Rooting

1. Download the latest [kingo-root](https://www.kingoapp.com/android-root/) app then click `One Click Root` and then wait for the progress until root succeeded, it's 100% success rate on my experience.✔️

<h2 id="edl">Rebooting into EDL Mode</h2>

- Install [ADB Drivers](https://forum.xda-developers.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/)
- Turn on Developer Options(I know you know this 😜) and turn on the `USB Debugging`.

1. Connect the device to your PC and run `adb devices` and it will show up your device's serial number.
    - If shows an `unauthorized`, check your device if needs to agree/accept or permit something like that to access your `USB Debugging`.
2. Run `adb reboot edl` then your screen will show a black screen only it means EDL Mode!

## Credits

- All the Links I put on this guide.
- [OPPO A37/A37f/A37fw Official Community](https://t.me/oppoa37community)
