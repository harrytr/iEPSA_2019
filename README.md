# iEPSA_2019

=============================================
Repository for the iEPSA computational study.
=============================================

Request a licence for MOSEK in order for iEPSA to run. Do it here:

https://www.mosek.com/products/academic-licenses/

Once you get the .lic file, create a folder in :  C:\Users\Your_name\mosek

and put the file inside.

Open MATLAB, and add to path the folder both the data and the algorithm. 
If all is well setup, running in MATLAB command prompt

>> mosekdiag

should give you confirmation that all is well installed. Now you can run iEPSA.

The command is:

[time,cpu_IP, Niter,Ze,Z0,~,~,Niter_NM] = iepsa_19_d(name)

where "name" is the name of the benchmark problem you wish to solve (without any file extension) e.g.: 


[time,cpu_IP, Niter,Ze,Z0,~,~,Niter_NM] = iepsa_19_d('degen2')

The output should look like :


=================================================================
[time,cpu_IP, Niter,Ze,Z0,P0,XB0,Niter_NM] = iepsa_19_d('degen2')
Starting iEPSA, v. Nov/2019
Slack variables have been added.
Selecting initial basis:
Selection done.
Elapsed time is 0.160105 seconds.
Searching for an interior point...
IPM converged to the specified Tol.
Elapsed time in seconds:
    0.0699

Corrector direction crosses FR.
Starting iEPSA optimizer...

  --------------------------------------------------------------------------------------------------
  Iter:    f(IP)          f(B)          status      sN<0 xB<0     NRE(B)      NRE(IP)       time     
  --------------------------------------------------------------------------------------------------
   1   -1.327775E+03 -1.110490E+03  feas direction  166   74  0.000000E+00 2.414217E-11   0.293790
 338   -1.406947E+03 -1.432883E+03  feas direction    4    0  1.831733E-14 2.632988E-01   0.855372
Starting original EPSA...
 390    ------------ -1.435178E+03  --------------    0    0  1.831733E-14 ------------   0.975785
Total time in seconds:
    0.9751


time =

    0.9751


cpu_IP =

    0.0699


Niter =

   390


Ze =

  -1.4352e+03


Z0 =

  -1.3278e+03


P0 =

   166


XB0 =

    74


Niter_NM =

   338
