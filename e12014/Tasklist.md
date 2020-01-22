# Primary Tasks
* [MCP Test](#MCP-Test)
* [Experiment Planning](#Experiment-Planning)
* [AT-TPC](#AT_TPC)
* [DAQ](#DAQ)
* [Gridded Ion Chamber](#Gridded-Ion-Chamber)

## MCP Test
- [ ] Setup DAQ for test
- [ ] Return MCP to unsegmented anode configuration
- [ ] Set MCP to position sensitive
- [ ] Data w/o mask
- [ ] Data w/ mask
- [ ] Populate a new voltage divider board
- [ ] Analysis and position resolution

## Experiment Planning
- [ ] LISE++ Simulations
  - [ ] Rate/beam size
- [ ] Foil thicknesses for various window sizes
  - [ ] Reaction rate in the foil and window
  - [ ] Extrapolate reaction rate to trigger rate
- [ ] Verifiction that we have all gas connections
  - [ ] Still need connections through TAMU
- [ ] Verification of planned vault layout

## AT-TPC
- [ ] Major surgery to replace the cathode backing for 4cm window
- [ ] Design and fabrication of 3 ro 3.5 cm window
- [ ] Pressure test windows of various sizes/thicknesses
- [ ] Simulations of AT-TPC
- [ ] Modification of electronics for trigger
- [ ] Purchase gas
  - [ ] Do we filter and recyle gas, or just flow

## DAQ
- [ ] Setup e12014 experiment account
- [ ] Setup DAQ test with AT-TPC and NSCL DAQ
  - [ ] Test ways of ensuring data is taken only if both DAQs are running
- [ ] Get data from linked DAQ
- [ ] Write ofline software for linking data togehter through timestamp matching
- [ ] Keep an eye on DAQ group/Daniel progress

## Gridded Ion Chamber

### Design
- [ ] Design mounting structure
- [ ] Design wall circuit boards
- [ ] Fix mistakes in prototype boards

### Fabrication
* Drawings and status list is in I:\projects\hira\wegert\New Ion Chamber (Gridded)
- [ ] Get quote for lead time and cost for Rogers3000 and unbrominated G-10 for our circuit boards
- [ ] Get parts from Zibi
- [ ] Send rest of drawings to Zibi

### Assembly
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
- [ ] Aquire enough 50mV/MeV Preamps
- [ ] Assemble boxes of ??
- [ ] Design mounting structure and cooling
- [ ] Test premaps with pulser


### Testing
- [ ] Alpha test at low pressure
- [ ] Ramp pressure with alpha to study detector
- [ ] Some sort of beam-like test?

# Old Tasks

## Old Ion chamber

### Analysis (Lead: Chenyang)
- [ ] Understand the double peak when cutting on Si PiD (**Joe**)
- [ ] Understand the purity of rates of different isotopes (**Joe**)
- [ ] Update LISE++ with physical locations on beam pipe (**Chenyang**)
- [ ] Update LISE++ with settings used in experiment (**Chenyang**)

### Hardware (Lead: Adam)
- [ ] Get baseline measurement with e15507 settings
- [ ] Get measurement with replaced decoupling capacitor
- [ ] Calculate best case energy resolution from IC
- [ ] SRIM simulation of alpha test for straggling
- [ ] Measure gain in Quad Shapers compared to Tenelec

## New Ion Chamber Lead: Rensheng?
- [ ] Finalize design
  - [ ] Finalize design of box (**Sarah**)
  - [ ] Finalize design of IC internals (**Sarah**)
  - [ ] Finalize design of prop counter internals (**Sarah**)
  - [ ] Write assembly procedure (**Sarah/Jon**)
  - [ ] Finalize design of circuit boards (**Aaron**)
- [ ] Frish grid 
  - [ ] Start design of mount for comb (**Jon**)
  - [ ] Start design of frame for wire winding (**Jon**)
  - [ ] Talk to Yassid about winding
  - [ ] Design prototype to test procedure
- [ ] Fabricate all parts (**WMU**)
  - Prioratize anode plate and build up
- [ ] Assemble IC
- [ ] Test IC with alpha and beam?
  - [ ] If no beam test until experiment, need to be able to switch IC to old

## MCP (Lead: Kyle)
- [ ] Replace anode on MCP
- [ ] Connect all cables

- [ ] Assemble all pieces
- [ ] Alpha test 
- [ ] Analyse for position resolution

## AT-TPC (Lead: Adam)

- [ ] Install copper vent pipe
- [ ] Get AHD approved

### Harware
- [ ] Purchase O2 scrubbers
- [ ] Fix AT-TPC leak
  - [ ] Calculate amount of contamination given current leak rate
- [ ] Buy H2 gas
- [ ] Finish window
  - [ ] Design of new window holder and cathode mount
  - [ ] Design modified blank to hold window
  - [ ] Fabricate holder and modified blank
  - [ ] Pick a window material and glue
  - [ ] Pressure test to 2 atm

### Software
- [ ] Do simulations of fission events
  - [ ] Write fission generator for AT-TPC
  - [ ] Everything else involved
- [ ] Design software for linking AT-TPC and NSCL analysis
- [ ] Implement and test software with simulations

## Misc
- [x] Layout plan for vault
- [ ] Finalize degrader selection
  - [ ] Get beam spot at degrader location
  - [ ] Calculate steel multiple scattering
  - [ ] Explore lapped Si
