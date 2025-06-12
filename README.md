# CustomDrone

Build your own drone!

<hr>

# Things Needed:
<pre>
  <b>Mandatory things:</b>
  4x 1400KV Brushless Motor
  4x ESCs (30A)
  1x Pixhawk 2.4.8 
  1x Flysky fs-i6x
  1x DJI F450 Frame
  4x 1045 Props or 9045 Props
  1x Female to Female Jumper Wire
  1x Power Module for Pixhawk
  1x 3S LiPo Battery (50-80C)
  1x LiPo balance charger
  1x Safety Switch
  1x Buzzer

  <b>Optional Things:</b>
  3x Servo (SG90 or MG90) - For Gimbal
  1x ESP32CAM (FPV Cams will also Work)- for Video
  2x HC05 - For Telemetry
  1x USB to SERIAL converter - For telemetry reciever
  1x 6-Pin DF13 Connector (Female) - For telemetry reciever
  1x GPS Module (Like the Ublox Neo-M8N, with compass) - For GPS Flight Modes
</pre>

<hr>

# Tools Needed:

<pre>
  Soldering Iron, preferably 60W+
  Soldering Flux
  Soldering Wire (Leaded or lead free)
  ELectrical tape or heat shrink tubing
  Wire Stripper
  Wire Cutter
  Allen Keys 
  Screwdriver
  Glue Gun 
  Double Sided Tape
  Multimeter
  Zip ties
</pre>

<hr>

# Important Notes:

<pre>
  1: Use a transmitter and reciever combo which can give PPM or SBUS output. If it gives PWM output, then you will also need a PPM Converter.
  2: ESP32CAM has a poor range for Video Feed.
  3: I strongly advise you to not use old Flight Controllers, like the APM series, because they are 99% of the time damaged, and will not be able to fly the drone.
  4: GPS Modules such as neo-7M, or the neo-6M, have poor performance which can cause your drone to fly poorly, or even crash in GPS based flight modes.
  5: If you do not put the GPS module, you will not be able to use many flight modes, such as RTL, Poshold, Loiter, etc.
  6: Drones draw a lot of power, so a Li-Po battery is used. however, these batteries can extremely dangerous, and even fatal, if they are shorted, over-discharged, or subject to any other condition.
  7: (VERY IMPORTANT) - Out of the 4 propellers, two have to be CW, other two have to be CCW.
  8: (VERY IMPORTANT) - Mount the pixhawk, or any FC, on the top plate; to avoid EMI generated from the ESCs.
  9: (VERY IMPORTANT) - the forward arrow on the GPS, as well as the Pixhawk should face the forward of the drone.
</pre>

<hr>

# Hardware 

<pre>
  1: Mount the 4 motors on the frame's each arm.
  2: Connect ESCs to them. Note that opposite motors have to spin in the same direction, with one pair being CW, other being CCW.
  3: Solder the ESCs onto the PDB.
  4: The Power Module has a female XT60 on side, and a male XT60 on the other side. cout the male xt60 connector, and solder the wires on the PDB of the frame.
  5: After this step, check for short circuits using a multimeter. If there are no shorts, then plug in a battery for a short amount of time to see if all ESCs get power.
  6: Screw down the top plate.
  8: Put the pixhawk in the center, with its arrow facing forward.
  9: Connect the Signal wires of the ESCs on the Main OUTS, in a cross pattern: Front-right: 1; Back-left:2; Front-left: 3; Back Right:4;
  10: Connect the gps the pixhawk.
  11: connect the power module to the pixhawk.
  12: connect the receiver's PPM out to the RC_IN on the Pixhawk.
  13: Connect the safety switch and the buzzer.
  14: Mount the three servos so that they control the yaw, pitch, and roll of the stabilized horn. 
  15: connect the leads of the servo the pixhawk's AUX out 1,2,3
  16: Connect one of the HC05 to the computer using an USB-SERIAL converter. change its baud to 57600. Optionally, you can change its name and password as well.
  17: connect the bluetooth module to the TELEM1 port of the Pixhawk.
  18: Check for shorts. if there is no short, power on the drone. ENSURE PROPS ARE NOT ON THE DRONE YET.
</pre>

# Software

<pre>
  1: Download Mission Planner's latest version.
  2: Flash the Arducopter firmware.
  3: After flashing connect again.
  4: If it connects fine, then upload the attach Parameter file. THIS FILE WILL ONLY WORK IF YOUR HARDWARE IS THE SAME AS MINE.
  5: Calibrate all sensors of the drone.
  6: Calibrate the rc.
  7: Calibrate the ESCs.
  8: Test the direction of the motors. ENSURE PROPS ARE NOT ON THE DRONE.
  9: Select the flight modes you want. Althold is a stable and reliable flight mode.
  10: If all works fine, then put the props, and go for a test flight.
</pre>
