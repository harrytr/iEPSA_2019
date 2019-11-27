# iEPSA_2019
Repository for the iEPSA computational study


Request a licence for MOSEK in order for iEPSA to run. Do it here:

https://www.mosek.com/products/academic-licenses/

Once you get the .lic file, create a folder in :  C:\Users\Your_name\mosek

and put the file inside.

Open MATLAB, and add to path the folder both the data and the algorithm. 
If all is well setup, running in MATLAB command prompt

>> mosekdiag

should give you confirmation that all is well installed. Now you can run iEPSA.

The command is:

[time,cpu_IP, Niter,Ze,Z0,P0,XB0,Niter_NM] = iepsa_19_d(name)

where "name" is the name of the benchmark problem you wish to solve (without any file extension) e.g.:
