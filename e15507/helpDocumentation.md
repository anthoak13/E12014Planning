## Manual for E15507

* [Running the DAQ](#running-the-daq)
  * [Readout Shell](#readout-shell)
  * [SpecTcl](#spectcl)
  * [PulserGUI](#pulsergui)
  * [HV Control](#hv-control)
  * [Hornet Control](#hornet-control)
  * [ELog](#elog)
* [FAQs](#faqs)
  * [Firefox not working](#firefox)
  * [Restarting the DAQ](#restarting-daq)

### Running the DAQ

The DAQ is setup to be run from any computer on the DAQ network, including U3PC's and any spdaq computer. The general recipe for getting the DAQ up is:

1. Run [Readoutshell](#readout-shell)
2. Run and connect [SpecTcl](#spectcl) to the ring buffer
3. Take data with [Readoutshell](#readout-shell)

#### Readout shell
From the home directory of account e15507, run `./ReadoutShell`. This should open a window like ![Readoushell Image](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShell.png). 

Then press start and you should see the VME crate attach like ![ReadoutShell After Start](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShellAfterStart.png). 

If this doesn't happen, make sure the VME crate is on and look at the section for [restarting the DAQ](#restarting-daq).

You are now ready to take data. If you want to record data, make sure the record button is ticked. You can verify data is coming in by running `./dumper` from the home directory. This just outputs everything being read in by the DAQ.

#### SpecTcl

#### PulserGUI

#### HV control

#### Hornet Control

#### ELog

### FAQs

#### Firefox

#### Restarting DAQ
