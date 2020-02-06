# Primary Tasks
* [MCP Test](#MCP-Test)
* [Experiment Planning](#Experiment-Planning)
* [Experiment Setup](#Experiment-Setup)
* [AT-TPC](#AT_TPC)
* [DAQ](#DAQ)
* [Gridded Ion Chamber](#Gridded-Ion-Chamber)

## MCP Test (**Rensheng**)
- [x] Setup DAQ for test
- [ ] Return MCP to unsegmented anode configuration
- [ ] Set MCP to position sensitive
- [ ] Data w/o mask
- [ ] Data w/ mask
- [ ] Populate a new voltage divider board
- [ ] Analysis and position resolution

## Experiment Planning
- [ ] LISE++ Simulations (**Chenyang**)
  - [x] Beam size
  - [ ] Comparison of simulation to data (predictive power of LISE) (**Chenyang/Joe**)
  - [ ] Check beam optics for ISO-100 Tee before/after Si detector
- [x] Foil thicknesses for various window sizes
  - [ ] Reaction rate in the foil and window (**Joe**)
  - [ ] Extrapolate reaction rate to trigger rate
- [ ] Design of gas system including pumping procedure w/ ATTPC (**Fanurs and Chenyang**)
  - [ ] Verify we have all connectors and tubing
  - [ ] Still need connections through TAMU (3 1/4 weldable VCO pieces, get part # from Zibi)  (**Sarah**)
- [ ] Verification of planned vault layout (**Adam**)

## Experiment Setup
- [ ] Setup beamline (**Allan**)
  - [ ] Gather all parts
  - [ ] Assemble in ReA3
  - [ ] Test pumping/venting procedure and check vacuum


## AT-TPC
- [x] Major surgery to replace the cathode backing for 4cm window
- [ ] Design and fabrication of 3 or 3.5 cm window
- [ ] Pressure test windows of various sizes/thicknesses
- [ ] Simulations of AT-TPC
- [ ] Purchase gas (**Joe**)
  - [ ] Do we filter and recyle gas, or just flow

## DAQ
- [ ] Setup e12014 experiment account (**Adam**)
- [ ] Setup DAQ test with AT-TPC and NSCL DAQ (**Allan**)
  - [ ] Setup of fast clear circuit between DAQs
  - [ ] Test ways of ensuring data is taken only if both DAQs are running
- [ ] Get data from linked DAQ
- [ ] Write ofline software for linking data togehter through timestamp matching (**Adam**)
- [ ] Keep an eye on DAQ group/Daniel progress (**Adam/Kyle**)

## Gridded Ion Chamber

### Design
- [ ] Design mounting structure
- [x] Finish PCB designs
- [x] Fix mistakes in prototype boards

### Fabrication
* Drawings and status list is in I:\projects\hira\wegert\New Ion Chamber (Gridded)
- [x] Get quote for lead time and cost for Rogers3000 and unbrominated G-10 for our circuit boards
- [ ] Get parts from Zibi
- [ ] Send rest of drawings to Zibi

### Assembly (**Rensheng**)
- [ ] Test anode assembly procedure
- [ ] Test Frisch grid prototype with protoype board
- [ ] Solder anode board
- [ ] Glue anode board in place
- [ ] Solder and glue small wall pieces
- [ ] Glue frisch grid boards in place
- [ ] Solder electrical connections between anode, wall, and frish grid
- [ ] Attach frish grid
- [ ] Solder large walls
- [ ] Solder window frame
- [ ] Solder window pane
- [ ] Glue window foil
- [ ] Do metal deposition on foil and make electrical connection with conductive epoxy
- [ ] Glue Window Frame
- [ ] Glue walls to window frame
- [ ] Glue cathode to bottom plate
- [ ] Glue cathode to walls

### Electronics
- [ ] Aquire enough 50mV/MeV Preamps (**Sean**)
- [ ] Assemble 3 preamp baords (15 ch total) (**Sean**)
- [ ] Modify box to hold preamps (**Sean**)
- [ ] Design mounting structure and cooling (**Sean**)
- [ ] Test premaps with pulser (**Drew/?**)
  - [ ] Use an existing test box
  - [ ] Measure noise of 50 mV/MeV preamp
  - [ ] Solve attenuation problem (we will saturate the shaper)


### Testing
- [ ] Alpha test at low pressure
- [ ] Ramp pressure with alpha to study detector
- [ ] Some sort of beam-like test?
