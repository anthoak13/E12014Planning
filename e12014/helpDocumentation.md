# Manual for E12014

* [Running the DAQ](#running-the-daq)
  * [Connecting to DAQ](#connecting-to-the-daq)
  * [Readout Shell](#readout-shell)
  * [SpecTcl](#spectcl)
  * [Scalers](#scalers)
  * [Signal Switcher](#signal-switcher)
  * [PulserGUI TODO](#pulsergui)
  * [Hornet Control](#hornet-control)
  * [ELog](#elog)
  * [PanelMate](#panelmate)
  
* [Vacuum system](#vacuum-system)
  * [Pumping TODO](#pumping)
  * [Venting TODO](#venting)
  
* [Ion Chamber](#ion-chamber)
  * [HV Control TODO](#ic-hv-control)
  * [CAEN Shaper TODO](#n568-control)

* [MCP](#mcp)
  * [FP HV Control](#fp-mcp-control)
  * [S2 HV Control TODO](#s2-mcp-control)	
  
* [Analysis](#analysis)
  * [Unpacking NSCL data](#unpacking-nscl-data)
  * [Unpacking TPC data](#unpacking-tpc-data)
  * [Merging NSCL/TPC data TODO](#merging-runs)
  * [Viewing TPC data](#viewing-tpc-data)

* [FAQs](#faqs)
  * [Firefox not working](#firefox)
  * [Restarting the DAQ](#restarting-daq)
  * [Problems with slow controls](#slow-controls)
    * [Refused socket connection](#refused-socket-connection)
    

## Running the DAQ

The DAQ is setup to be run from any computer on the DAQ network, including U3PC's and any spdaq computer. The general recipe for getting the DAQ up is:

1. Run [Readoutshell](#readout-shell)
2. Run and connect [SpecTcl](#spectcl) to the ring buffer
3. Take data with [Readoutshell](#readout-shell)

### Connecting to the DAQ
For this experiment we will be running everything from Windows machines. Right now there are three computers setup for this one each in Data U3, Data U5, S2 Vault. Each of these computers is configured to allow sshing into fishtank, daq network, or at-tpc network through cygwin using pre-loaded ssh keys.

To connect to open a new cygwin terminal. There are a number of aliases to connect to other computers, they are:
```
s2: connects to the daq computer in s2
u3: connects to a daq computer in u3
u5: connects to a daq computer in u5
spdaq29: connects to the daq computer in the A1900
spdaq48: connects to the daq computer in S2
fishtank: connects to fishtank
```

To keep life simple and consistant, things like ReadoutShell and SpecTcl should be run from u5.


### Readout shell
From the DAQ network on account e12014, run `ReadoutShell`. This should open a window like 

![Readoushell Image](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShell.png). 

Then press start and you should see the VME crate attach like 

![ReadoutShell After Start](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShellAfterStart.png). 

If this doesn't happen, make sure the VME crate is on and look at the section for [restarting the DAQ](#restarting-daq).

You are now ready to take data. If you want to record data, make sure the record button is ticked. You can verify data is coming in by running `dumper` from the computer that is recording data (not necessarily the computer running ReadoutShell). This just outputs everything being read in by the DAQ. You can also pass valid dumper command arguments through this wrapped. For example `dumper --count 10` will only output the first 10 items. A full list of valid argumets can be found with `man dumper`. 

### SpecTcl

#### Launching SpecTcl

First, make sure you are on a DAQ network computer (ie u5). To launch SpecTcl, `cd ~/SpecTcl` and then `./SpecTcl`. It will take a few seconds for it to fully load.

#### Closing SpecTcl
To close SpecTcl, you should always use the purple **Exit** button on the bottom of this window 

![SpecTcl Ecit](https://github.com/anthoak13/E12014Planning/raw/master/e15507/SpecTclExit.png)

#### Using SpecTcl
In order for SpecTcl to be of any use, you have to attach a data source. Usually, this will be an online data source (a ringbuffer) or a .evt file. The data source is selected from the data source tab. Make sure that ring11 is selected and the buffer size is set to 8192.

![SpecTcl Data Source](https://github.com/anthoak13/E12014Planning/raw/master/e15507/SpecTclDataSource.png)

When connecting online, make sure the settings match those below

![SpecTcl Online](https://github.com/anthoak13/E12014Planning/raw/master/e15507/SpecTclOnline.png)

For offline, the .evt files are located in ~/experiment/run#/

![SpecTcl Offline](https://github.com/anthoak13/E12014Planning/raw/master/e15507/SpecTclOffline.png)

Data should now be coming in. At list point, you will want to load in and def-files, making sure Cumulative is checked. Now window files can be loaded too. Below is a list of def and win files.

TODO: Put in list of files

### Scalers
To launch the scalers program do `Scalers` you should see

![Scalers](https://github.com/anthoak13/E12014Planning/raw/master/e12014/pics/Scalers.png) 


### Signal Switcher
The signal switcher is a multiplexer used to look at signals in the data U. Outputs 0-4 are patched to channels ??,??,??,??, respectively.

To launch the program, run `switch`. You should see a window like 

![SignalSwitcher](https://github.com/anthoak13/E12014Planning/raw/master/e12014/pics/SignalSwitcher.png) 

You can then drag the bars to select any one of the 32 availible channels. The channel mapping can be found here. TODO put channel mapping. 

### PulserGUI

To run the pusler GUI `cd ~/pulser` and run `wish pulserGUI_BLUE_fission.tcl`. You should see a window like

![PulserGUI](https://github.com/anthoak13/E12014Planning/raw/master/e15507/PulserGUI.png)

To connect to the pulser press the **Connect** button, and then push **Pulse On** to start the pulser. The window should look like this now

![PulserOn](https://github.com/anthoak13/E12014Planning/raw/master/e15507/PulserGUIOn.png)

### HV control
The HV control GUI used is a modified version of the standard NSCLDAQ vhqControl. It was changed to add more descriptive channel names. This program works through communication over the fiber optic interface between the DAQ computer and the VME crate. This means that the program has to be run on the DAQ computer that is physically attached to the VME crate. The launch scripts `~/goHVUS` and `~/goHVDS` handle this all for you. The actual program being called is `~/HVcontrol/vhgControl` with the appropiate configuration scripts passed. All of the configuration scripts are located in `~/HVcontrol` if they need to be modified. DO NOT try to change the configuration scripts through the GUI interface!

To launch the voltage control of the focal plane MCP, run `~/goHVUS`. You should see 2 windows pop up that look like

![HVControl](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e15507/HVControl.png)

The downstream HV control works the same way as the focal plane HV control, but there are three windows. The additional one is for control of the ion chamber bias.

### Hornet Control
To launch the ion gauge control run `~/goHornet`. This launches a Tcl GUI written by Adam to monitor the pressure in the MCP and Ion Chamber sections of the chamber. When it launches, you should see a small window with two tabs. It seems to like to crash after being open for a bit, if that happens just close it and reopen it

If the IC is on, it will display and update the pressure every two seconds and look like

![HornetOn](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e15507/HornetOn.png)

If the ion gauge is off, then you should see something like

![HornetOff](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e15507/HornetOff.png)

The **On/Off** button toggles the power status. It will take up to 15 seconds to turn on, so be patient. You can also read the power status and any error from the status bar below the pressure reading.

### ELog
The server that host the elog must be launcher from fishtank. There is a script that will automate the launch. To start the elog run `elogStart`. This will open a ssh connection to `walleye` and start the server in a screen named `elog`. You may have to press enter after the screen opens to get the text to terminal to update. You should see the following

![ELogStart](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/ELogStart.png)

Alternatively, do
```
ssh e12014@walleye
./runELog.sh
```

The elog is now accessable at [http://walleye:e12014/elog](http://walleye:e12014/elog) from within the DAQ network. A shortcut to opening the elog is the command `elogOpen` which opens a firefox session on an appropiate computer. The elog looks like

![ELogOnline](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/ELogOnline.png)

Once the elog is opened the server should look like

![ELogServer](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/ELogServer.png)

and entries can be edited/added.

### PanelMate
PanelMate is part of the controls network. For this experiment it will mostly be used in pumping/venting to control the interlocked vent valve (G207VV). From one of the computers on the Controls network, open PanelMate, then open the config file S2_Vault. Navigate to page 08. You should see

![PanelMate](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/PanelMate.jpg)

To open/close the valve, select "G207VV Vent Valve" then use the buttons in the upper right to open/close it.

## Vacuum system

### Pumping

### venting

  
## Ion Chamber

### IC HV Control

### n568 Control


## MCP

### FP MCP Control
The high voltage at the FP is split between a Iseg NHS nim module and Iseg VHQ VME module. The NHS controls the HV for the MCP and E-field on channels 1 and 0, respectively. The VHQ the HV for the foil on channel A.

The NHS is controlled through the isegControl2 program, launched with the command `isegControl`. When it opens you should see this window

![IsegControl](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/IsegControl.png)

If it doesn't load the module automatically, go to Project->New. You should see a new window, then select New Connection on the bottom, then set the connection type to USB port (SCPI protocol) and set the port to ttyUSB2. Hit connect and it should detect the module and load the configuration. You should see something like

![IsegControlProject](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/IsegControlProject.png)

You should now be able to control the module. Double clicking Vset on a channel allows you to change the voltage to ramp to. You can ramp on/off by double clicking Off/On.

The HV for the foil can be launched by running `hvFPFoil.` You should see something like, but channel A should be beige not red.

![vhqFPfoil](https://raw.githubusercontent.com/anthoak13/E12014Planning/master/e12014/pics/vhqFpfoil.png)

### S2 MCP Control


## Analysis

### Unpacking NSCL Data
The data is unpacked and mapped using HiRAEVT. Unpacking is already setup, mapping will be worked on as the experiment progresses. Data is unpacked from evt files in `/mnt/rawdata/e12014`. Unpacked/mapped data can be found in `/mnt/analysis/e12014/HiRAEVT`.

1. Open a new terminal and cd to HiRAEVT code and source the enviroment script.
```
cd ~/hira/HiRAEVT
source bin/HiRAEVT.sh
```
2. From the HiRAEVT directory, run the unpacker.
```
HiRAEVTUnpacker run#
HiRAEVTUnpacker 1stRun# lastRun#
```

### Unpacking TPC Data
This is a multi-step process. The data must be mergered on the tpc side. This takes the many output files from the TPC and mergers them into a single HDF5 file. That file must then be copied from the private AT-TPC network to the NSCL side. This has to be done from the gateway machine. That file is then unpacked into a ROOT file. By default this unpacks just the raw data, and makes a simple reconstruction of 3D points. If the TPC parameters change, they have to be updated in `/mnt/simulations/attpcroot/adam/ATTPCROOTv2/parameters/ATTPC.e12014.par` 

1. Merge the file. *This will be the responsibily of the TPC person on shift.*
2. Copy file from gateway to /mnt/events/e12014/tpc/ *TODO: Need correct path*
3. From a new terminal ssh into fishtank, go to the ATTPC-ROOT directory and source the enviroment file.
```
fishtank
cd /mnt/simulations/attpcroot/adam/ATTPCROOTv2
source env.sh
```
4. Move to the unpacker directory and run. This assumes the HDF 5 file is in `/mnt/events/e12014/tpc/`, and unpacks the data to `/mnt/analysis/e12014/TPC/unpacked`

```
cd /mnt/simulations/attpcroot/adam/ATTPCROOTv2/compiled/E12014Unpacker/bin
./unpackTPC 258
```
### Merging Runs
Coming soon!

### Viewing TPC Data
This has to be done using a macro. Trying to compile failed miserably.

1. From a new terminal ssh into fishtank, go to the ATTPC-ROOT directory and source the enviroment file.
```
fishtank
cd /mnt/simulations/attpcroot/adam/ATTPCROOTv2
source env.sh
```
2. Go to the e12014 macro directory. `cd /mnt/simulations/attpcroot/adam/ATTPCROOTv2/macro/e12014`
3. Run the visualizer, passing the unpacked run you would like to view.
```
root 'run_eve.C("/mnt/analysis/e12014/TPC/unpacked/run_0309.root")'
```

## FAQs

Below is a list of common problems I've encountered and how to fix them. As we find more problems, I'll add them to the list
### Firefox

Because all of the computers share a home directory, I've found firerfox can often screw up its locks. To fix this problem `cd ~/.mozilla/firefox` and delete the files `lock` and `.parentlock` from the profile directory. I've found that the right profile to try is `2rbkukgx.Kyle`.

### Restarting DAQ
If you see something like this 

![Readoutshell error](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShellError.png)

then you'll need to, probably, fully restart the DAQ. This often occurs when there is already a process registered as the producer for the e15507 ringbuffer. Either beacuse the DAQ crashed, or there is a readoutshell open somewhere else connected to ringbuffer e15507. 

To restart the DAQ, start by `~/GoSpdaq`. Then type `ringbuffer status`. You should see some output like
```
<spdaq48:~ >ringbuffer status
+------+------------+-------+-------------+--------+---------+---------+------+-------------+
|Name  |data-size(k)|free(k)|max_consumers|producer|maxget(k)|minget(k)|client|clientdata(k)|
+------+------------+-------+-------------+--------+---------+---------+------+-------------+
|e15507|8194        |8167   |100          |29294   |26       |26       |-     |-            |
|-     |-           |-      |-            |-       |-        |-        |29308 |26           |
+------+------------+-------+-------------+--------+---------+---------+------+-------------+
```
Kill the process that is registered as the producer `kill 29294` and delete the ringbuffer `ringbuffer delete e15507`. You should then be able to use ReadoutShell to attach to the ringbuffer.

### Slow Controls

#### Refused socket connection

Most problems with the slow controls stem from another copy of the program being open elsewhere. This is difficult to track down if you do not know where the program was opened last. This is particularly true of the PuslerGUI and Hornet Control as they both connect to a terminal server that only allows one connection at a time. When you try to connect to the terminal server if there is an existing open connection you will see an error like
```
<u3pc2:~ >./goHornet 
Error in startup script: couldn't open socket: connection refused
    while executing
"socket $terminalName.nscl.msu.edu 2001"
    (procedure "start" line 6)
    invoked from within
"start $server"
    (file "/user/e15507/hornetIG/hornetGUI.tcl" line 47)
```

The challenge is tracking down the open process. The best way I've found is to ssh into each computer it might be open on (s2pc2, u3pc2, u3pc3) and kill any offending processes. You can find potential process IDs with the command `ps aux | grep wish`. This should fix the problem.
