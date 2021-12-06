# Hands-on experiments at HRC(BL12), NM school 2021, Day 3

## Sec.1: Introduction of the MSlice software
At HRC, we are using MSlice software to visualize the inelastic scattering data, which are generally 4D matrices containing Q<sub>x</sub>,Q<sub>y</sub>,Q<sub>z</sub> (or H,K,L), and E.
MSlice is included in the Data Analysis and Visualization Environment "DAVE".

https://www.ncnr.nist.gov/dave/

## Sec.2: constant-E and constant-Q cuts
To extract dispersion relations of magnetic excitations from an observed spectrum, we make 1D-cuts of the Q-E intensity map. 
When cutting the intensity map along the Q and E directions, the 1D profiles are referred to as "constant-E" and "constant-Q" cuts, respectively.

In the following, we try constant-E cuts of the magnetic excitation spectrum of CsVCl<sub>3</sub> measured at HRC.

### Problem 1
Draw Q-E (L-E) maps of CsVCl<sub>3</sub> measured with E<sub>i</sub>=102 meV and E<sub>i</sub>=15.3 meV.
* Download (or clone) this repository and load the script "CsVCl3_contour_plot_script.txt" in gnuplot.

### Problem 2
* Draw const-E cuts of the data measured with E<sub>i</sub>=102 meV.
    * Open "CsVCl3_constE_script.txt" by a text editor.
    * Set values for "IntegE_min" and "IntegE_max", which are the minimum and maximum energies for integration with respect to E.
    * Load the script in gnuplot, and then a png file showing the const-E profile and a txt datafile of the profile will be generated.

<img width="800" src="https://user-images.githubusercontent.com/50174733/144793299-4f436985-af66-4569-b554-4db88dddb3f0.png">

* Extract peak positions of the magnetic excitations using "peakfit_script.txt".
    * Open "peakfit_script.txt" by a text editor.
    * Set the filename of the constant-E profile (txt file) to the variable "datafile". 
    * Set appropriate initial guess values for BG, q, A, HWHM. Note that "q" is the wave vector of the spin excitation, which correspond to the distance from the zone center at L=1. Specifically, the peak position L<sub>peak</sub> is 1-q.
    * Set L_min and L_min, which are the minimum and maximum L-indices used for fitting. Note that **"L_min" should be larger than that of the leftmost datapoint** in the profile which you are going to fit. 
    * Run the "peakfit_script.txt" on gnuplot
    * The result of the fitting analysis will appear as below. Copy the refined value of "q" and its error and paste them to a text file "fitting_result.txt" with the mean energy of the const-E cut.
<img width="800" src="https://user-images.githubusercontent.com/50174733/144793188-9ac3bd94-97cb-4397-a37d-53405e9ac3dd.png">

* Finally, plot the mean energy as a function of q. The dispersion relation should be fitted by the equation 4S|J|sin(pi*q), which will be maximized at q=0.5. Determine the value of J, that is the exchange interaction between magnetic moments. (S=3/2 for this system)
    * For plotting and fitting, you may use gnuplot scripts, "plot_dispersion.txt" and "fit_dispersion.txt" in the "problem2" folder, respectively. 
## Sec. 3: A short lecture on magnetic excitations in CsVCl<sub>3</sub> by Prof. Itoh
