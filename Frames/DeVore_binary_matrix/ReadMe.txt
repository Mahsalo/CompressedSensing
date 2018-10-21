{\rtf1\ansi\ansicpg1252\cocoartf1348\cocoasubrtf170
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 LucidaGrande;}
{\colortbl;\red255\green255\blue255;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural

\f0\fs24 \cf0 This folder includes Matlab implementation of the binary DeVore measurement matrix which is proposed in [1]. The summarized explanation of DeVore\'92s matrix is found in our paper in [2]. There are three Matlab files in the folder:\
\
1) Devore_Exp.m : This file receives a prime number \'93q\'94 and the dimensionality of the unknown vector \'93n\'94 as inputs. It must be noted that in 
\f1 DeVore\'92s construction, the dimensionality of the matrix is q^2*n and n<=q^3. (q is a prime number)\
The output of this function is a q*n matrix which only keeps the indices of ones and helps reducing the memory needed to store the matrix. In DeVore matrix, each column has \'93q\'94 blocks and in each block we have exactly one 1. So the \'93B\'94 matrix keeps the indices 0:q-1 of the ones in each column of the measurement matrix. In [2], we have proposed a non-iterative recovery algorithm based on binary matrices which is super-fast compared to basis pursuit. In the non-iterative recovery algorithm, we don\'92t need to have the actual matrix \'93A\'94 thus we can use the sparse representation of this matrix which is \'93B\'94.\
\
2) Exp_mult.m : This file computes the measurement vector \'93y=Ax\'94 by only having the indices matrix \'93B\'94. So the inputs are B and x (unknown vector) and the output contains the sample values in the noise-free case.\
\
3) B_to_A.m : This file gives us the actual measurement matrix \'93A\'94 by using the index matrix \'93B\'94. In some applications, we might need to have the actual matrix \'93A\'94 instead of the sparse representation of it (\'93B\'94).\
\
-If you have any questions, feel free to contact the author by the following email:\
mafilot@gmail.com\
-If you use our code in your research, please support us by citing our paper in [2].\
\
***********References**********\
[1] Deterministic Constructions of Compressed Sensing Matrices, Ronald A. DeVore, Journal of Complexity, Vol. 23, pp. 918-925, 2007.\
[2] A Fast Non-iterative Algorithm for Compressive Sensing Using Binary Measurement Matrices, Mahsa Lotfi and Mathukumalli Vidyasagar, IEEE Transactions on Signal Processing, Vol. 66(15), pp. 4079-4089, 2018.\
\
}