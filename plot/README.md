Plot tools
====


scan.py
====

    python plot/scan.py output.0.10.25.00.20.00.*GeV.root

    python plot/scan.py output_100_0_1*_25.00_10.00_0.00.root


    
plot_energy.py
====

Accepts a series of root files to be read. Input Files are generated by Example07.multifit.cc 
Returns energy distribution histograms for each input file
and a histogram ploting RMS of these histograms vs. the various tunable parameters: 
[NSAMPLE, NFREQ, Amplitude, Pileup] Examples:

With one root file

    python plot/plot_energy.py output_file1.root

With many root files (you can pass it as many as you want)

     python plot/plot_energy.py output_file1.root output_file2.root output_file2.root

With many root files, using an asterisk to select them

    python plot/plot_energy.py "output_file*.root"
    python plot/plot_energy.py "output_file*.root" new_data1.root
    python plot/plot_energy.py "output_file.root" "new_data.root"

A useful selection where all parameters are fixed except one

    python plot/plot_energy.py "output_10_25.00_10.00_*.root"

    python plot/plot_energy.py "output_10_25.00_*_20.00.root"

IMPORTANT: When selecting files using the wildcard '*', 
the filename must be surrounded with quotes "" as a string, 
to protect the wildcard from being interpreted by the shell. 
When passing files one at a time with their full names, using quotes or not doesn't matter.

e.g.

    python plot/plot_energy.py  output_60_6.25_5.00_20.00.root
    
    
    
    
    
    
    
    
    
    