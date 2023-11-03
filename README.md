# wii-balance-board-recorder
This is a Windows operating application to calibrate and collect data from a Wii Balance Board (WBB, Nintendo Co., Ltd., Kyoto, Japan.) through its bluetooth connection. 

## Getting started.
To use the Wii Balance Recorder application, click the green 'code' button above. Then choose 'download as ZIP'. Unzip the folder and start up the installation procedures by clicking the .exe file inside the `Volume` folder. For further instructions how to use the software and calibrate the Wii Balance Board, refer to the [PDF manual](https://github.com/tomvredeveld/wii-balance-board-recorder/blob/main/Manual%20Wii-Balance-Board-Recorder%20(v1.0.0).pdf). 

## Connecting the Wii Balance Board & Set-up Manual
As explained in more detail in the [manual](https://github.com/tomvredeveld/wii-balance-board-recorder/blob/main/Manual%20Wii-Balance-Board-Recorder%20(v1.0.0).pdf), the software does not provide the connection with the WBB. 
For our procedures, we relied on using the WiiBalanceWalker software described here [WiiBalanceWalker, v0.5, by Schacher Liberman](https://github.com/lshachar/WiiBalanceWalker). However, other software or the primary Windows bluetooth connection tools may work for you. In our experience, connecting the WBB without the WiiBalanceWalker software was troublesome.
Our manual provides a guide how to combine WiiBalanceWalker and this Wii Balance Recorder to obtain calibrated data from the Wii Balance Board.

## The txt output file.
The `txt` output file is tab delimited, contains a time-series of the Wii Balance Board sensor registrations by row. The columns consist of the following: 

- `Time` - Time series, in milliseconds
- `CpX` - Center of Pressure in the X, or medio-lateral direction. Registration in centimeters.
- `CpY` - Center of Pressure in the Y, or antero-posterior direction. Registration in centimeters.
- `BottomLeft` - BottomLeft (BL) sensor value calibrated value after initial calibration, units in N. 
- `BottomRight` - BottomRight (BR) sensor value calibrated value after initial calibration, units in N. 
- `TopLeft` - TopLeft (TL) sensor value calibrated value after initial calibration, units in N. 
- `TopRight` - TopRight (TR) sensor value calibrated value after initial calibration, units in N. 
- `Weight` - Total weight in kilogram (kg) recorded on the Wii Balance Board. Values should approximately match the sum of BL, BR, TP, and TR values converted from N to kg.<sup>a</sup>
- `RAWBottomLeft` - Raw sensor data of the BL sensor
- `RAWBottomRight` - Raw sensor data of the BL sensor
- `RAWTopLeft` - Raw sensor data of the TL sensor
- `RAWTopRight` - Raw sensor data of the TR sensor

<sup>a</sup> Please note, due to conversion from N to kg, and truncation, weight may not exactly match the sum of the sensor data. Weight should therefore be used as an indication of correct registration by the Wii Balance Board rather than an adequate measurement of the weight placed upon it.

## Posturography Measures.
Once the Wii Balance Board is connected and the software is installed, one can obtain a `txt` file (tab delimited) to analyse, for example, the Center of Pressure (COP) of a subject performing a balance task. To select a segment and analyze frequently used COP parameters, one may use the R/Shiny web-application provided at this [GitHub repository](https://github.com/tomvredeveld/center-of-pressure-analysis-tool)  

## About.
This application was build and currently maintained by Vincent Tuinder from the Department of Human Movement Sciences at the Faculty of Behavioural and Movement Sciences, Vrije Universiteit Amsterdam. He asked me to upload and maintain the GitHub repository. 

### Disclaimer.
The software uses external dependencies for which licenses are supplied in the `.\Installer\Volume\licence`  folders. The `wii-balance-board-recorder` includes third-party dependencies with their respective licenses, which are supplied for reference. We, do not claim to be the rightful owner of these dependencies.

I have made every effort to ensure that the Wii Balance Board Recorder and its dependencies comply with applicable licenses and legal requirements. However, if you believe that any aspect of the application shared in this repository infringes on your rights or is not in compliance with relevant licenses, please contact me immediately, see the contact details below.

I am committed to addressing and rectifying any legitimate concerns regarding the ownership and licensing of the application. Your cooperation in this matter is greatly appreciated.

### Wii Balance Board.
The Wii Balance Board was produced and manufactured by Nintendo Co., Ltd., Kyoto, Japan. 

## Contact
If you have any issues installing or running the application, please let me know at: t.vredeveld[at]hva[dot]nl, create an issue or pull-request.
