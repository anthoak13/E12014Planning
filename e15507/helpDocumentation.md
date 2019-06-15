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
If you see something like this ![Readoutshell error](https://github.com/anthoak13/E12014Planning/raw/master/e15507/ReadoutShellError.png)

then you'll need to, probably, fully restart the DAQ. This often occurs when there is already a process registered as the producer for the e15507 ringbuffer. Either beacuse the DAQ crashed, or there is a readoutshell open somewhere else connected to e15507. 

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
