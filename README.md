# SLICE-QTC-Firmware-Upgrade
Repository for the latest released firmware for the SLICE-QTC

## Requires 
  Vescent SLICE_Firmware_Upgrade_Utility available at:
  
  https://github.com/Vescent/SLICE-FFC_Firmware_Upgrade_Utility
## Instructions
  __NOTE: Upgrading from versions prior to S2.22_QT2.51 will erase all device settings and parameters. Record them externally prior to updating firmware!__
  
  __NOTE: Upgrading from Version S1.24_QT1.38 gives the SLICE-QTC the previously unavailable ***IDN?** serial command. See Configuration S1.77_QT1.50 notes for more information.__
  
  Please see the revised user manual for instructions on how to use new features. 
  Available at:
  
  https://www.vescent.com/manuals/doku.php?id=slice:qt
  
  Left click on SLICE_Firmware_Update_Instructions.pdf and then click 'Download' to download the instructions for use. 

  __NOTE:__ If the firmware upgrade utility is unable to automatically download the upgrade files on your system, do the following steps.
  Left click on the upgrade package (SC-x-xx-QT-x-xx.zip) and then click 'Download' to download the firmware package to your hard drive.
  
  The two files in the .zip file need to be placed in the folder described in the instructions. DO NOT RENAME THEM!

## Configuration S2.30_QT2.63
Adds support for new Rotary Encoders.

## Configuration S2.29_QT2.63
 1. Fixes inoperative Output Triggers
 2. Adds polarity selection for Input and Output Triggers
 3. Adds safety critical operating mode and I2C communication monitoring and fault messaging
 4. Fixes occasional lockup when Steinhart Hart and B Value coefficients were rapidly adjuted
 5. Fixes occasional inability to adjust temperature setpoint from the Slow Servo setpoint button.
 6. Adds detection and freezing of the last good state if an open circuit in a temperature plant is detected. Last measured value is displayd with a red background until released by a button press.
 7. Fixes sluggish behavior observed when viewing the error wave form of a badly shielded plant.
 8. Fixes an occasional switch to a non requested Auto Tune at 50% completion.
 9. Adds detection and freezing of the last good state if an Out Of Range Temperature is detected. Last measured value is displayd with a red background until released by a button press.
## Configuration S2.22_QT2.51
 1. Adds Auto Tune feature for automatically calculating temperature control parameters
 2. Improves Slow Servo Input functionality to allow making adjustments to the Slow Servo Input parameters from the main or single channel pages.
 3. Changes default gain for Slow Servo Input to -30.0 dB
 4. Adds ability to do future firmware upgrades without pressing the blue button (Upgrading from versions prior to S2.22_QT2.51 still requires a blue button press.)
 5. Adds unique USB descriptor information that Identifies the Model (QTC) and Serial Number of the device 
	__NOTE: A new COM port number will be assigned to the QTC after upgrading to this version.
 6. Fixes an erroneous 3.5W Power Reading when the Current, Power, Voltage readout is switched to Power for the first time after power up
 7. Adds the ability to use either \r, \n, or \r\n to terminate serial API commands
 8. Fixes home screen rotary edit timeout which failed to return the readout border to blue color after an inactivity timeout
 9. Fixes "None" appearing in the I/O selection readout after sliding a finger to the outside of the selection drop down menu
 10: Fixes a failure to save External Input B selections in non-volatile memory during power cycles
 11. Fixes instances where multiple "Settings are Locked" message windows would be drawn requiring several OK selections to dismiss the message
 12. Adds the ability to exit a drop-down menu by touching outside the menu
 13. Improves the ability to tune noisy temperature control plants
 14. Improves inter board communication which speeds up response time to user inputs and provides smoother error plot rendering
 15. Adds Trigger In Enable / Disable temperature control functionality based on input to the Trigger In BNC connection.
 16. Adds device serial number to the general settings screen
 17  Adds SCPI *RST serial API command to restart the device without power cycling
 18. Changes the rotational direction of the Y scaling feature of the single channel summary page so that it is consistent with the Y axis adjustment on most oscilloscopes.
 19. Adds additional Y scaling increments to the single channel summary page graph scaling
 20. Fixes a bug that resulted in unplanned behavior or lockup when the user slides their finger off of a navigation button.
## Configuration S1.177_QT1.52
 1. Fixes incorrect output current reading. 
 2. Fixes corrupted front panel input voltage signal which could have adverse affects on I/O input functions.
 3. Fixes occasional false over power shutdown and display of warning message.
## Configuration S1.177_QT1.50
 1. Temperature Setpoint resolution is now 0.1 mK
 2. Fixes measured temperature corruption issue when using a non-zero Steinhart-Hart C coefficient.
 3. Fixes meter lockup when invalid Steinhart-Hart coefficients are entered
 4. Implements ***IDN?** Serial API command
   
       Returns:
    
       __Vescent Photonics, SLICE-`<model>`, `<serial number>`, `<System Controller FW Version>`, `<ICE2 FW Version>`__  
       __NOTE:__ For SLICE QTC models which were originally shipped with Version S1.24_QTC1.38 firmware, contact Vescent for  
                 assistance in loading the device serial number.
       
  5. Allows exiting a rotary knob edit by touching outside of the active rotary edit box
  6. Fixes occasional -0.0 display on error readout
  7. Adds automatic shutdown with error summary when device maximum power is exceeded.
  8. Adds **Setpoint Relative** external input mode which allows adjustment of the base temperature setpoint from the main or channel summary screen  
  9. Adds **INPUTA, INPUTB, OUTPUT1, and OUTPUT2** serial API commands. See [SLICE-QTC API](https://www.vescent.com/manuals/doku.php?id=slice:qt:api) for instructions  
  10. Adds shutdown of all menus and return to main screen when a FAULT condition is detected  
  11. Fixes Actual Temperature not updating after thermistor coefficients are changed  
  12. Fixes Rotary Edit freeze at 0.0. (Previous versions would freeze the value at 0.0 if the user continued to turn the rotary knob counter clockwise upon reaching 0.0. The user would have to exit and re-enter the rotary edit mode or use the keypad entry to increase the value.)
  
