# GHS Procedures

For more description, see <https://groups.nscl.msu.edu/hira/12014/gas_handling_system_and_procedures.pdf>.

## Pumping
### 0. Initialization. Merge IC, TAMU, MCP, GHS volumes.
	- Make sure AT-TPC is at atmospheric pressure with bias off.
	- Open: V2, V3, V4, V8 on GHS
	- Close: V1, V5, V6, V7 on GHS
	- Close gas regulator on gas bottle
	- Open V10 and V11 (IC-TAMU and MCP-TAMU by-passes)
	- Close V12 - V18
	- Turn on both mech. pumps; Turn off both turbo pumps.
	- Turn off control valve.
	- Connect differential gauge; disconnect absolute gauge.
	- Off: H.V. for IC, Si, MCP and pre-amp. of IC.
	- On: H.V. for HPGe.
	- On: Stinger gauge for TAMU; Off: Both ion gauges (TAMU & MCP)
### 1. Start pumping. Wait till 500 mTorr. Monitor differential pressure.
	- Open V13 (turbo for MCP)
	- Open V14 (mech. to turbos)
	- Open V15 (mech. to GHS)
### 2. Isolate each component, turn on turbos.
	- Open V12 (turbo for TAMU)
	- Close V10 (IC-TAMU bypass)
	- Close V11 (MCP-TAMU bypass)
	- Read: Stinger gauge for TAMU, make sure below 500 mTorr.
	- Turn on both turbos
	- Wait to reach 1 mTorr; May inform AT-TPC to start pumping.
### 4. Reached high vacuum (1m Torr), turn on ion gauges.
	- AT-TPC may start pumping to vacuum.
	- Turn on both ion gauges.
### 5. Switch to absolute gauge.
	- Make sure control valve is off.
	- GHS: Disconnect differential gauge, and connect absolute gauge.
### 6. Purge gas line. Repeat 3 times.
	- One purge cycle: Open V1, wait, then close V1.
	- Close V1 before proceeding next step.
### 7. Gas to IC. Adjust control valve to reach 300 mTorr. Vent. Repeat 3 times.
	- Set control valve to "AUTO", and set to "0.00".
	- Open gas regulator.
	- Open V16 (gas to GHS)
	- Adjust control valve and V8 to fill IC with 300 mTorr.
	- Set control valve to "OFF", and set to "0.00".
	- Vent IC slowly with V7.
	- Repeat above procedures 2 more times.
	- Once done, set IC at 300 mTorr.
### 8. Congratulations! You may run your experiment now.
	- Remember to turn on H.V. for IC, Si, MCP and pre-amp. of IC.

## Venting
### 1. Prepare for venting. Turn off delicate items.
	- Make sure AT-TPC has been vented, and bias is off.
	- Off: H.V. for IC, Si, MCP and pre-amp. of IC.
	- Off: Both ion gauges.
### 2. Prepare GHS venting. Switch to differential gauge.
	- Set control valve to "OFF".
	- GHS: Disconnect absolute gauge, connect differential gauge.
	- Close V16 (gas to GHS)
	- Close gas regulator.
### 3. Vent IC gas and purge gas line.
	- Open V1.
	- Wait to vent.
	- Close V1.
### 4. Fill IC with 50 Torr of N2 with control valve. Open MCP-TAMU bypass.
	- Close V7.
	- Open V11 (MCP-TAMU bypass) only.
	- Connect N2 to V17 (flush beforehand), and open V17.
	- Use control valve to fill IC to 50 Torr of N2.
### 5. Turn off turbos and slow down.
	- Turn off both turbos.
	- Close V12 and V13 (turbos to TAMU and MCP).
	- Close V15 (mech to GHS).
### 6. Vent TAMU with N2 to 600 Torr, then air to atmospheric pressure.
	- Close V14 (mech. to turbos).
	- Connect N2 to V18.
	- Open V18 slowly to vent.
	- Read: Stinger gauge for TAMU, wait until 600 Torr.
	- Vent quickly with air/N2.
### 7. Vent backing line. Open TAMU lid.
	- Open V12 and V13 (turbos for TAMU and MCP).
	- Open TAMU lid.
