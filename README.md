# PTtools
These are codes for analytical predictions of compressed sensing Phase Transitions and various function for the analysis of PT datasets

To install the R package of PT from github:
```
> install.packages("devtools")
> library(devtools)
> install_github("monajemi/CompressedSensing", subdir="PTtools/R/PT")
> library(PT)

> predictPT(1/2,'R')
[1] 0.1928448
```

There is also a MATLAB version of this prediction.

```
>> predictPT(1/2,'R')
```


# Frames
These are codes for construction of various frames that I have used in my publications 

# Example: 
```
% build a real USE matrix
A = buildFrame(16,64,'USE','R');

% build a Complex DG frame of size 32x128
A = buildFrame(32,32*4,'DG','C');


% build 'non-strictly' regular (best effort) LDPC matrices of degree 3
A = buildFrame(504,1008, 'LDPC','R',[],3,1);
A = buildFrame(504,1008, 'LDPC','R',[],3);


% build 'strictly' regular LDPC matrices of degree 3
A = buildFrame(504,1008, 'LDPC','R',[],3,0);

```


## References: 

"Deterministic matrices matching the compressed sensing phase transitions of Gaussian random matrices", Monajemi et al. 2013
