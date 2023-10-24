# PEPT-toolbox
Toolbox for post-processing experimental and simulated trajectories. Compatible with Windows.
To download the toolbox navigate to PEPT-toolbox/PEPTToolbox/for_restribution and download PEPTToolboxInstaller.exe.
Once downloaded, run the installer and it will prompt you to download Matlab runtime.

The toolbox is capable of handling large amounts of particle trajectory data.
The experimental data input should be a .csv file with columns |t|x|y|z|
The data is imported via file -> import -> experimental data
once imported, you can manually tweak an array of settings before pushing the calculate velocities button.
It is important that the characteristic size field should be large enough to encompass the range of trajectory data.
Calculate velocities will calculate the velocities of the particle, discretise the system, and time-average through voxels.
The statistics of interest are velocity plots, number of passes, occupancies, dispersion, displacement, and mixing effectiveness.

The simulated data should be a .csv file with columns |id|t|x|y|z|
the data is imported via file -> import -> cfd data
The data is handled similarly to the experiment data.
Push calculate velocities and the app will determine velocities, discretize the system, and time-average into voxels.

If both experiment and simulated data is post-processed, the parity plot will also be plotted for each variable.
The r^2 and Q_sim statistics indicate the strength of the relationship between experiment and simulation.
For comparing Q_sim, it is important to ensure that the trajectory time-lengths between experiment and simulation are similar.
This can be controlled by selecting the amount of data to load, or by thresholding the CFD start time.

Tomographies can be exported for a desired frame-rate:
  file -> export -> tomographies -> parameter of interest

plot data can be exported similarly using the export functionality in file -> export.

