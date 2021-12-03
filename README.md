# Hands-on experiments at HRC(BL12), NM school 2021, Day 3

## Sec.1: Introduction of the DAVE software
## Sec.2: constant-E and constant-Q cuts

### Problem 1
Draw Q-E (L-E) maps of CsVCl<sub>3</sub> measured with E<sub>i</sub>=102 meV and E<sub>i</sub>=15.3 meV.
* Download (or clone) this repository and load the script "CsVCl3_contour_plot_script.txt" in gnuplot.

### Problem 2
* Draw const-E cuts of the data measured with E<sub>i</sub>=102 meV.
    * Open "CsVCl3_constE_script.txt" by a text editor.
    * Set values for "IntegE_min" and "IntegE_max", which are the minimum and maximum energies for integration with respect to E.
    * Load the script in gnuplot, and then a png file showing the const-E profile and a txt datafile of the profile.

<img width="800" src="https://user-images.githubusercontent.com/50174733/144559576-035106f4-7612-488b-9e4c-c33d3867dc2c.png">

* Extract peak positions of the magnetic excitations using "peakfit_script.txt".
    * Open "peakfit_script.txt" by a text editor.
    * Set the filename of the constant-E profile (txt file) to the variable "datafile". 
    * Set appropriate initial guess values for BG, q, A, HWHM.
    * Run the "peakfit_script.txt" on gnuplot
    * The result of the fitting analysis will appear as below. Copy the refined value of "q" and its error and paste them to a text file with the mean energy of the const-E cut.
<img width="800" src="https://user-images.githubusercontent.com/50174733/144569380-93766229-9e31-4d3f-99b7-4028ebeddc94.png">

* Finally, plot the mean energy as a function of q. The dispersion relation should be fitted by the equation

## Sec. 3: A short lecture on magnetic excitations in CsVCl<sub>3</sub> by Prof. Itoh
