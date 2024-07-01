# V3rus
The 3rd version of a Python script/exe that'll cause a BSOD on startup. It is meant to be ran once from a USB thumb drive on the target Windows device.
It does the following:
1. It disables any possible security measures that could stop it from working, this includes: Windows Security (Simple exception) and UAC (Disables completely, Does not account for UAC passwords). 
2. It copies itself to the startup directory as a hidden file and differently named file.
3. It creates a hidden flag file, this way it'll know if it has done the above before. If the flag file is detected it'll skip the above and continue to step 4.
4. It runs a simple Windows PowerShell command that causes a BSOD. This then causes the device to restart and re-run the script, causing another BSOD, causing a loop of the device powering on and off.
