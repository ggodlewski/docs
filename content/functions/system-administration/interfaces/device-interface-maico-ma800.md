---
title: "Device Interface - Maico MA800"
date: "2020-02-27T21:28:06.013Z"
url: "functions/system-administration/interfaces/device-interface-maico-ma800.html"
author: aquandt
version: 16
id: "1u7cPDkqx04cxeALGacspymwrVoHyKKwQbOW8z5XMVzY"
source: "https://drive.google.com/open?id=1u7cPDkqx04cxeALGacspymwrVoHyKKwQbOW8z5XMVzY"
menu:
    main:
        name: "Device Interface - Maico MA800"
        identifier: "1u7cPDkqx04cxeALGacspymwrVoHyKKwQbOW8z5XMVzY"
        parent: "1J0bDKTGYlGAEqJraL-CUB3x3d976F4lBdUCSRKpIv2Q"
        weight: 5540
---
This page provides instructions for retrieving results from the Teleaccoustics Maico MA800 audiometer with Enterprise Health (EH), and lists the fields that the interface retrieves.

## Instructions

### Individual Mode

To retrieve results for an individual patient:

* Go to the patient's chart and start a new Audiogram encounter.
* Click the Perform Test button in the MA800 Audio section.
* Click the Connect to Maico MA800 link.
    * The first time the device is used, run the MIE Applet and allow access to the application.
    * The first time the device is used, enter the correct COM Port. This is now the default value.
* Click the Open Port button. If successful, "Waiting for data..." appears.
* Perform the audio test on the device
* The test will automatically be transferred when completed
    * A window will appear with the test results
    * Click the "Save Results" button if correct or "Cancel" if incorrect

### Batch Mode

The MA 800 does not support batch upload.

## Collected Fields

The following fields are collected in EH:

* Left ear frequencies: 500Hz, 1kHz, 2kHz, 3kHz, 4kHz, 6kHz, 8kHz
* Right ear frequencies: 500Hz, 1kHz, 2kHz, 3kHz, 4kHz, 6kHz, 8kHz
* Test Date/Time
* Calibration Date/Time

## Installation Help

To correctly install and use the audiometer with EH the following considerations are important to note:

* The interface uses Java to interact with the device; Java must be installed on each PC that is connected to the audiometer.
* During the initial setup, ensure that the COM port settings on the device are the same as in EH

## Related Pages

For a list of all supported devices, see our??[Devices List](../../../resources/system-specifications/interface-specifications.html)

