--------------------------------------------------------------------------------
There are 2 CK waveform file formats: STD and RAMP. 
For TN4 MEMS, all the waveforms are defined as rows in 5 files stored in C:\Users\vm080160\dev\CK_ATE\Waveforms\521
RMP_DOWN, RMP_UP, STD_DOWN, STD_UP, STD_UP&DOWN

A script references the waveforms defined in files above.
The script is called during the actual test sequence, such as R0, R10, R39 or Butterfly
--------------------------------------------------------------------------------
"script PullDown41v
    Generate BRise41v20u
    Generate BHi41v28u
end script"

# source filename: STD_DOWN
# BHi means bottom hi
# WaveformName	DCVoltageValue	DurationValue
BHi41v28u	0	28e-6

# source filename: RMP_DOWN
# WaveformName	RampStartVoltageValue	RampEndVoltageValue	DurationValue
# 
BRise41v20u	0	41	20e-6

--------------------------------------------------------------------------------
"script BeamsOff
      Generate AllLow
end script

# source filename: STD_UP&DOWN
# WaveformName	DCVoltageValue	DurationValue(X2)
AllLow	0	4.2e-6"


