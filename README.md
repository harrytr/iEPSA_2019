# iEPSA_2019
Repository for the iEPSA computational study

### Prerequisites
Request a licence for MOSEK in order for iEPSA to run. Do it here:

https://www.mosek.com/products/academic-licenses/

Once you get the .lic file, create a folder in :  C:\Users\Your_name\mosek

and put the file inside.

Open MATLAB, and add to path the folder both the data and the algorithm. 
If all is well setup, running in MATLAB command prompt

```Matlab
>> mosekdiag
```

should give you confirmation that all is well installed. Now you can run iEPSA.


## Running iEPSA

The command is:

```Matlab
[time,cpu_IP, Niter,Ze,Z0,P0,XB0,Niter_NM] = iepsa_19_d(name)
```

where "name" is the name of the benchmark problem you wish to solve (without any file extension).

The function "linprogIEPSA4" needs to be put in the same folder where the file "mosekopt.mexw64" exists, in the installation folder of the MOSEK software, that was added to path in MATLAB prior of executing iEPSA.

### References
Please cite using :

> [1] Triantafyllidis C.P. (2013). "A Non-Monotonic Infeasible Interior-Exterior Point Algorithm for Linear Programming", PhD Thesis, Dept. of Applied Informatics, University of Macedonia, Greece.

> [2] Triantafyllidis CP, Samaras N. 2020. A new non-monotonic infeasible simplex-type algorithm for Linear Programming. PeerJ Computer Science 6:e265 https://doi.org/10.7717/peerj-cs.265
