# GHS Procedures

For more description, see <https://groups.nscl.msu.edu/hira/12014/gas_handling_system_and_procedures.pdf>.

## Pumping (TURN BIAS OFF!!!)
### 0. Setup gas handling system (GHS)
	- Setup in differntial mode by moving the d-sub connector to the differentuial pressure gauge, setting the senser voltage on the control vale to 1V, and setting the display voltage to ????
	- On GHS, close V1, V5, V6, V7
	- On GHS, open V2, V3, V4, V8
	- On GHS, make sure the control valve is closed
	- On the gas inlet line close the valves to N2 and gas regulator (V16 and V17)
### 1. Merge all vacuum volumes and prepare to pump
	- Open the bypasses between TAMU and the IC/MCP volumes (V10 and V11)
	- Verify the valves on the roughing pumps are closed (V14 and V15)
	- Verify the valves on the tubo pumps are closed (V12 and V13)
	- Verify the vent valves are closed (V18 and V19)
	- Verify the interlocked gate valve is open on the controls computer (G207VV)
	- Verify H.V. for IC, Si, MCP and pre-amp. of IC is off.
	- Verify stinger gauge is on, and both ion gauges are off.
### 1. Start pumping through the MCP turbo, constantly monitoring differential pressure on GHS
	- If off, turn on both roughing pumps (Add special instructions for scroll?)
	- Open the valve on the turbo backing pump (V14)
	- Slowly open the valve on the MCP turbo (V13). You want to pump at ~1 torr/sec, making sure the pressure in the IC remains positive.
	- Once the stinger gauge reads < 50 torr, open the valve on the TAMU turbo (V12)
	- At this point, open the valve on the GHS pump (V15)
	- Wait for vacuum to get to level for turbos (400 mtorr)
### 2. Isolate each component, turn on turbos.
	- Turn on both turbos
	- Close the bypasses between TAMU and the IC/MCP (V10 and V11)
	- Wait till Stinger gauge goes off scale.
	- Close the interlocked vent valve (G207VV)
	- May inform AT-TPC to start pumping.
### 4. Reached high vacuum (1m Torr), turn on ion gauges.
	- AT-TPC may start pumping to vacuum.
	- Turn on both ion gauges.
### 5. Switch to absolute gauge.
	- Make sure control valve is off.
	- GHS: Disconnect differential gauge, and connect absolute gauge.
### 6. Prepare to vent IC with gas
	- Close V1.
### 7. Gas to IC. Adjust control valve to reach 300 mTorr. Vent. Repeat 3 times.
	- Close V4.
	- Open gas regulator.
	- Set control valve to "AUTO", and set to "0.00".
	- Open V16 (gas to GHS)
	- Adjust control valve and V8 to fill IC with 300 mTorr.
	- Set control valve to "OFF", and set to "0.00".
	- Slowly pump out the gas by opening V7 again.
	- Close V7 after IC volume is pumped.
	- Set control valve to "AUTO", and set to "0.00".
	- Go back to "Adjust control valve..." and repeat two more times.
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
	- Close V16 (gas to GHS)
	- Close gas regulator.
	- GHS: Disconnect absolute gauge, then connect differential gauge.
### 3. Pump out IC gas and purge gas line.
	- Open V8 to pump out IC volume.
	- Open V1 to pump out gas line volume.
	- Wait to pump.
	- Close V1 and V7.
### 4. Fill IC with 50 Torr of N2 with control valve. Open MCP-TAMU bypass.
	- Set control valve to "OFF", and set to "0.00".
	- Feed N2 to V17 and make sure V16 is closed.
	- Open V17.
	- Set control valve to "AUTO", and set to "50.00".
	- Open V11 (MCP-TAMU bypass) only.
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
