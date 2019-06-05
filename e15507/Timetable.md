# Timetable for the setup of e15507

### Outstanding questions
- [x] When will Greg move his stuff out of S2?
  - Kyle emailing Mark? and Greg
- [x] Need a beamline -> iso 100 adapter to couple chamber, and Hornet
  - Will get Friday
- [x] When can we borrow the Masytecs from Thomas?
  - Kyle asking
- [x] Is there someone who can be in charge of the electronics?
  - The DAQ config is already written and the control of HV for IC and MCP is solved downstream
  - Chenyang and Fanurs
- [x] When will we get the HPGe?
  - Hopefully Friday before 6/14 
- [ ] Talk to Elaine about borrowing the old Si as a beamstop (Kyle)
- [x] Talk to Jim V about modifying gains on cable driver (Bill)
- [ ] Zibi comming Thursday 6/6
- [ ] Venting only through the interlocked system
- [ ] Who will be expert in
  - [ ] Computer system (DAQ, Hornet GUI, Modified HV control, Django runlog)
  - [ ] MCP and MCP electronics
  - [ ] IC and IC electronics
  - [ ] HPGe and HPGe electronics
  - [ ] Si stack and Si electronics


## Week 4 (5/13 - 5/17)
### Hardware Setup
- [x] Move TAMU chamber to S2 5/15
- [x] Attach both crosses to TAMU in vault 5/17 (JW/AP)
- [x] Move both roughing pumps to S2 5/17 (JW/AP)
- [x] Move both turbo pumps to S2 5/17 (JW/AP)
- [x] Attach pumps w/o GHS 5/17 (JW/AP)
- [x] Attach Hornet 5/17 (JW/AP)
- [x] Pressure test empty and not coupled over weekend 5/17 (KB)

### Electronics Setup
- [x] Move a rack with pressure gauge to S2 5/17 (JW/AP)
- [x] Talk to Jim V about reducing gain in cable driver 5/17 (AA/BL)

## Week 3 (5/20 - 5/24)
### Hardware Setup
- [x] Couple to beam line 5/22 (JW/AP/AA)
- [x] Verify flanges are correct 5/20 (AA)
- [x] Move P-10 bottle to S2 vault 5/24 (AA)
- [x] Vacuum test while empty 5/20 - 5/22 (JW/AP/AA)
- [x] Attach MCP mounting hardware 5/22 (JW/AP/AA)
- [x] Repair the cable on the MCP 5/24 (JW/AA)
- [x] Check the upstream chamber alignment with MCP (JW/AP/AA) 
- [x] Redo the chamber foil 5/24 (JW/AA)
- [x] Add the bypass to the chamber 5/24 (JW/AP/FT)
- [x] Add the MCP 5/24 (JW/AA)
- [x] Add a source to alpha test 5/24 (KB)

### Electronics Setup
- [x] Isolation test of chamber 5/20 (CN/FT)
- [x] Move the other electronic rack to S2 5/20 (CN/FT)
- [x] Add the VME modules 5/20 (CN/FT)
- [x] Setup the DAQ again 5/24 (AA)

## Week 2 (5/27 - 5/31)
### Hardware Setup
- [x] Modify upstream MCP so it fits backwards 5/27 (AA)
- [x] Modify downstream MCP so it fits backwards (AA)
- [x] Align the MCP with the telescope 5/29 (JW/AP/AA)
- [x] Gather electronics for FP 5/29 (AA)
- [x] Unpack from WMU Test 5/30 (JW/AP/AA/CN)
  - [x] GHS to S2
  - [x] Gas connections to S2
  - [x] Chiller to S2
- [x] Re-add the ICs and align 5/31 (JW/AP/AA)


### Electronics Setup
- [x] Write interface for Hornet 5/27 (AA)
- [x] Write vhqControl config files 5/27 (AA)
- [x] Verify DAQ with pocket pulser (MCP) 5/27 (CN/FT)
- [x] Pulser test of Si stack 5/30 (CN/FT)
- [x] Verify IC electronics 5/30 (NC/FT)
- [x] Verify Si electronics 5/30 (CN/FT)

## Week 1 (6/3 - 6/7)
### Hardware Setup
- [x] Add T and thermocouple to pump to measure backing pressure 6/3 (FT)
- [ ] Hook up exhaust tubing for pumps 6/3 (FT)
- [x] Repair leak at isolating iso-100 o-ring 6/3 (JW/AP/AA)
- [ ] Leak test with final connections 6/3 (JW/AP/AA)
- [ ] Pump down in "statis" mode 6/7 (JW/AP/AA)
- [x] Build stand for HPGe (SW)
#### MCP
- [ ] Test MCP with alpha trigger 6/3 (AA)
- [ ] Remove the alpha source 6/4 (KB)
- [ ] Identify and fix issue at E-field > 2800V (sparking?) 6/3
#### Ion Chamber
- [x] Pressure test new gas connections 5/31 (AA/JW/AP)
- [ ] Repair the new IC 6/3 (AA)
- [x] Modify new IC with new connections 6/3 (JW)
- [ ] Repair the old IC 6/3 (AA)
- [x] Modify old IC with new connections 6/4 (JW)
- [ ] Alpha test old IC 6/4 (AA/JW/AP)
- [ ] Add the chamber foil 6/4 (JW/AP)
- [ ] Attach GHS with no IC 6/4 (JW/AP)
- [ ] Pressure test system with closed loop 6/4 (AA/JA/AP)
- [ ] Add ICs and pressure test 6/5 (JW/AP/AA)
- [ ] Add the cooling bar 6/6 (JW/AP)
- [ ] Pressure test with final connections 6/6-6/7 (JW/AP/AA)

### Electronics Setup
- [ ] Verify IC DAQ with preamp boxes 6/3 (FT/CN)
- [ ] Have DAQ with MCP signal function by 6/4 (CN/FT/AA)
- [ ] Identify amount of attenuation needed for ICs 6/4 (AA)
- [ ] Add attenuation to ICs 6/4 (AA)
- [ ] Full pulser test of IC DAQ with attenuation 6/4-6/5 (CN/FT)
- [ ] Run cables between Data U and vault (CN/FT)
- [ ] Set up multiplexer for looking at signals in data U (CN/FT)
- [x] Run lines between FP box and data U (KB/JW/AP)
- [x] Patch lines together (KB/JW/AP)
- [x] Measure delay and set Windows for FP MCP (JW/AP/AA)

## Week 0 (6/10 - 6/14)
### Hardware Setup
- [ ] Add downstream Si 5/31 (AA/KB/CN)
- [ ] Install HPGe
- [ ] Install FP MCP
- [ ] Calibrate HPGe
- [ ] Calibration pulser of ICs
- [ ] Calibration pulser of Si

### Electronics Setup
- [ ] Verify HPGe DAQ with alpha source
- [ ] Write Spectcl scripts for dE-ToF plots

## Expirement (6/16-6/18)
- [ ] Ramp MCP voltages with stable beam
- [ ] Verify one blob with PiD with stable

