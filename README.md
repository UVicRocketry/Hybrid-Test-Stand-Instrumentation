# Hybrid Test Stand Instrumentation

Hybrid instrumentation is a part of the hybrid test stand support project. A LabJack U6 Data Acquisition unit (DAQ) collects the output voltage of the pressure transducers, load cells, and thermocouples placed on the test stand as well as within the combustion chamber and injector. These are sent to a Raspberry Pi 3, where voltages are processed, logged, and displayed by the instrumentation software written in the block diagram coding program LabVIEW. 

## Install LabJack Hardware Support Applications at: https://labjack.com/support/software/installers/ud

The LJUD test applications will require you to run the executable and download to User>Program Files (x86)>LabJack.
For our testing purposes, the two useful applications are LJStreamUD and LJControlPanel. 

The LJUD LabVIEW library files are included in the repo to maintain references between users. It is best practice to, whenever a LJ_UD VI needs to be edited, copy and rename the VI. Also add the VI to the .lvproj file.

The "Signal Manipulation" VI can be found in the "Old Instrumentation" Folder (Used in new instrumentation as a reference for sensor gain/offset)
