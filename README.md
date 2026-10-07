=================================================================
       MUSICAL INSTRUMENT FREQUENCY ANALYZER
=================================================================

Mathematical Concept:
Eigenvalues of a tridiagonal stiffness matrix
and eigenvectors as vibration modes.

Real-World Application:
Musical instrument strings vibrate in different natural modes.
The natural frequencies correspond to these vibration modes.
=================================================================
INPUT PARAMETERS
----------------------------------------
Number of masses (N)       : 8
Mass of each segment (m)   : 0.01 kg
Spring stiffness (k)       : 1000.0 N/m
Modes to display            : 3
MATHEMATICAL MODEL
============================================================

We assume:

1. N identical masses are connected by identical springs.
2. Both ends of the string are fixed.
3. Each mass has mass m.
4. Each spring has stiffness k.
5. Small vibrations are considered.

The equation of motion is:

        M x'' + K x = 0

where:

        M = mass matrix
        K = stiffness matrix

For identical masses:

        M = m I

The stiffness matrix is tridiagonal:

        K = k *
            [ 2  -1   0   ...   0 ]
            [-1   2  -1   ...   0 ]
            [ 0  -1   2   ...   0 ]
            [ .   .   .    .    . ]
            [ 0   0   0   -1    2 ]

For free vibration:

        K phi = lambda M phi

Since M = mI:

        (K/m) phi = lambda phi

Therefore:

        lambda = omega^2

and

        f = omega / (2*pi)

STIFFNESS MATRIX K
==================================================
[[ 2000. -1000.     0.     0.     0.     0.     0.     0.]
 [-1000.  2000. -1000.     0.     0.     0.     0.     0.]
 [    0. -1000.  2000. -1000.     0.     0.     0.     0.]
 [    0.     0. -1000.  2000. -1000.     0.     0.     0.]
 [    0.     0.     0. -1000.  2000. -1000.     0.     0.]
 [    0.     0.     0.     0. -1000.  2000. -1000.     0.]
 [    0.     0.     0.     0.     0. -1000.  2000. -1000.]
 [    0.     0.     0.     0.     0.     0. -1000.  2000.]]
Stiffness Matrix K:
[
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
−
1000.0
0.0
0.0
0.0
0.0
0.0
0.0
−
1000.0
2000.0
]
​
  
2000.0
−1000.0
0.0
0.0
0.0
0.0
0.0
0.0
​
  
−1000.0
2000.0
−1000.0
0.0
0.0
0.0
0.0
0.0
​
  
0.0
−1000.0
2000.0
−1000.0
0.0
0.0
0.0
0.0
​
  
0.0
0.0
−1000.0
2000.0
−1000.0
0.0
0.0
0.0
​
  
0.0
0.0
0.0
−1000.0
2000.0
−1000.0
0.0
0.0
​
  
0.0
0.0
0.0
0.0
−1000.0
2000.0
−1000.0
0.0
​
  
0.0
0.0
0.0
0.0
0.0
−1000.0
2000.0
−1000.0
​
  
0.0
0.0
0.0
0.0
0.0
0.0
−1000.0
2000.0
​
  
​
 
MASS MATRIX M
==================================================
[[0.01 0.   0.   0.   0.   0.   0.   0.  ]
 [0.   0.01 0.   0.   0.   0.   0.   0.  ]
 [0.   0.   0.01 0.   0.   0.   0.   0.  ]
 [0.   0.   0.   0.01 0.   0.   0.   0.  ]
 [0.   0.   0.   0.   0.01 0.   0.   0.  ]
 [0.   0.   0.   0.   0.   0.01 0.   0.  ]
 [0.   0.   0.   0.   0.   0.   0.01 0.  ]
 [0.   0.   0.   0.   0.   0.   0.   0.01]]
EIGENVALUE CALCULATION COMPLETE
==================================================
Eigenvalues (lambda = omega^2):
[ 12061.47584  46791.11138 100000.      165270.36447 234729.63553
 300000.      353208.88862 387938.52416]

Angular frequencies omega:
[109.82475 216.31253 316.22777 406.53458 484.48905 547.72256 594.3138
 622.84711]

Frequencies in Hz:
[17.47915 34.42721 50.32921 64.70199 77.10883 87.17275 94.58798 99.1292 ]
NATURAL FREQUENCIES
================================================================================
 	Mode	Eigenvalue λ = ω²	Angular Frequency ω (rad/s)	Frequency f (Hz)
0	1	12061.47584	109.82475	17.47915
1	2	46791.11138	216.31253	34.42721
2	3	100000.00000	316.22777	50.32921
3	4	165270.36447	406.53458	64.70199
4	5	234729.63553	484.48905	77.10883
5	6	300000.00000	547.72256	87.17275
6	7	353208.88862	594.31380	94.58798
7	8	387938.52416	622.84711	99.12920
FIRST 3 HARMONICS
==================================================
Harmonic 1: λ = 12061.47584, ω = 109.82475 rad/s, f = 17.47915 Hz
Harmonic 2: λ = 46791.11138, ω = 216.31253 rad/s, f = 34.42721 Hz
Harmonic 3: λ = 100000.00000, ω = 316.22777 rad/s, f = 50.32921 Hz
FIRST 3 EIGENVECTORS / VIBRATION MODES
============================================================

Mode 1
------------------------------
Mass  1: +0.16123
Mass  2: +0.30301
Mass  3: +0.40825
Mass  4: +0.46424
Mass  5: +0.46424
Mass  6: +0.40825
Mass  7: +0.30301
Mass  8: +0.16123

Mode 2
------------------------------
Mass  1: +0.30301
Mass  2: +0.46424
Mass  3: +0.40825
Mass  4: +0.16123
Mass  5: -0.16123
Mass  6: -0.40825
Mass  7: -0.46424
Mass  8: -0.30301

Mode 3
------------------------------
Mass  1: +0.40825
Mass  2: +0.40825
Mass  3: +0.00000
Mass  4: -0.40825
Mass  5: -0.40825
Mass  6: -0.00000
Mass  7: +0.40825
Mass  8: +0.40825





EIGENVALUE EQUATION VERIFICATION
============================================================
Mode 1: error = 9.9767386243e-13
Mode 2: error = 5.1825800622e-13
Mode 3: error = 6.2720995887e-13

BENCHMARK TEST DATASET
==================================================
Instrument                    : Idealized Guitar String
Number of masses              : 8
Mass per segment (kg)         : 0.01
Spring stiffness (N/m)        : 1000.0
BENCHMARK RESULTS
============================================================
Mode 1: Eigenvalue = 12061.47584, Frequency = 17.47915 Hz
Mode 2: Eigenvalue = 46791.11138, Frequency = 34.42721 Hz
Mode 3: Eigenvalue = 100000.00000, Frequency = 50.32921 Hz
NUMERICAL VS ANALYTICAL EIGENVALUES
======================================================================
 	Mode	Numerical λ	Analytical λ	Absolute Error
0	1	12061.47584282	12061.47584282	1.091e-11
1	2	46791.11137620	46791.11137620	7.276e-12
2	3	100000.00000000	100000.00000000	1.455e-11
3	4	165270.36446661	165270.36446661	5.821e-11
4	5	234729.63553339	234729.63553339	2.910e-11
5	6	300000.00000000	300000.00000000	1.164e-10
6	7	353208.88862380	353208.88862380	1.746e-10
7	8	387938.52415718	387938.52415718	1.164e-10
======================================================================
           MUSICAL INSTRUMENT FREQUENCY ANALYZER
======================================================================

MATHEMATICAL PIPELINE

Physical string
      ↓
N masses + springs
      ↓
Stiffness matrix K
      ↓
Mass matrix M
      ↓
K φ = λ M φ
      ↓
Eigenvalues λ = ω²
      ↓
ω = √λ
      ↓
f = ω / 2π
      ↓
Natural frequencies
      ↓
Eigenvectors φ
      ↓
Vibration modes

FIRST THREE HARMONICS
--------------------------------------------------
Harmonic 1: 17.479 Hz
Harmonic 2: 34.427 Hz
Harmonic 3: 50.329 Hz

Project completed successfully!
======================================================================
