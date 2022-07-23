LabVIEW_LJUD - LabVIEW drivers/examples for LabJackUD
support@labjack.com

October 16, 2020

Compatible with LabVIEW 7.1 or higher.  Requires the
LabJack UD driver.

Note that National Instruments provides a driver called NI-DAQ
for their hardware.  We have to provide our own driver, called
LabJack UD, for our hardware.  LabVIEW can talk to either driver,
but realize that some NI tools like Measurement & Automation
Explorer and DAQ Assistant are part of NI-DAQ and thus do
not apply to LabJacks.

These VIs use the LabJackUD Driver for Windows.  Before using
the VIs, you should look at Section 4 of the U3/U6/UE9 Datasheet,
and get an understanding of how the LabJackUD driver
interacts with the hardware:

https://labjack.com/support/datasheets

This LabVIEW archive is kept as close as possible to all of
our other programming examples.  At its core, LabVIEW is just
a graphical representation of C or similar, so although
Section 4 of the user's guides is written in a text syntax,
it maps very well to LabVIEW.

The downloadable zip file "LabVIEW_LJUD.zip" extracts to a single
folder called "LabVIEW_LJUD" which contains this readme file, a
.mnu file, and a few subdirectories.  The folder can be stored
anywhere, but if you want icons to show up on the LabVIEW function
palette (after restarting LabVIEW), place this folder under:

...\national instruments\labview #\vi.lib\addons\

If the function palette icons are not required, a common place to
store this folder is ...\LabJack\examples\.  We have found that most
people, including us, just do this.  Instead of using palette icons
to select LabJack VIs, most people just:

   1)  copy and paste from examples,

... and

   2) use the "Select a VI..." balloon from the function palette.


We recommend not having more than one copy of the VIs,and not changing
these VIs.  Make a copy in a different directory if, for instance, you
wish to modify one of the example VIs.  If you download new VIs
from labjack.com, delete and replace the entire LabVIEW_LJUD folder.


6000 is added to the LabJack errorcodes to shift them into the LabVIEW
user range of 5000-9999.


The \LabJackUD DLL Functions\ directory contains simple VIs that do little
more than call functions from the LabJackUD driver DLL.

The \UE9 Raw OutIn VIs\ directory contains VIs that make calls to some of
the UE9 low level functions (Section 5 of the UE9 User's Guide) through
the UD driver.  The UD driver has two IOTypes called RAW_OUT and RAW_IN
that allow raw bytes to be sent and received.  This allows the user to
make calls, through the UD driver, to any low level function on any 
LabJack supported by the UD driver.  This method should generally only
be used when the desired low level functionality is not otherwise
supported by the UD driver (through a different IOType).

The \Utility VIs\ directory contains VIs that encapsulate some useful
functions.  These will often be placed in a user's VI, and require
an initial call to open a LabJack.

The \Examples\ directory has various examples.  Generally these can
be run stand-alone.  Generally examples cannot be dropped into your
program as a sub-VI.  Rather, they demonstrate how to incorporate
the driver sub-VIs in your VI, or serve as a starting point for your
own VI.

