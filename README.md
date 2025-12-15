# Hack-club-drone
This is a schematic with its code for the pcb of a drone. Shoutout to BenCaunt for his help.

Disclaimer
This project is in its infancy and nearly everything is subject to massive overhauls

While testing, make sure your OpenDrono's propellers are off to ensure your safety. Then adjust the + and - signs in the motor mixing section of the code (such as the following). This makes sure that the feedback from each fo the individual controllers moves the drone in the correct direction. Failure to do this will cause great instability and will likely damage your OpenDrono or yourself (True Story).

    frontRightSpeed = heightPower - rollPower - pitchPower - yawPower;
    frontLeftSpeed = heightPower + rollPower - pitchPower + yawPower;
    backRightSpeed = heightPower - rollPower + pitchPower + yawPower;
    backLeftSpeed = heightPower + rollPower + pitchPower - yawPower; 
