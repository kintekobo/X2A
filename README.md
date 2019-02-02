# X2A
Convert G-Code X moves to rotary A moves

This is a DotNet program and runs on Mac/PC/Linux provided the Net environment is installed. It is a simple command line program which read in a G-Code text file and repaces all of the X moves with A moves. This enables the simple milling of round parts using a fourth axis stepper system.

Usage on a PC is - X2A filetoconvert

  e.g. X2A testfile.nc
  
Usage on a Mac is - mono X2A.exe filetoconvert

  e.g. mono X2A testfile.nc
  
The file is read in, scanned and altered and written out.


An example of the process is shown below -

==================================================
Original file

%
(1001)
(GrXduXted DiXl)
N10 G90 G94
N11 G17
N12 G21

(EngrXve3)
N13 M9
N14 T1 M6
N15 S16500 M3
N16 G54
N17 G0 X3.489 Y17.501
N18 Z10
N19 Z3
N20 G1 Z-0.913 F635
N21 X3.603 Y17.38 Z-0.904
N22 X3.703 Y17.281 Z-0.898
N23 X3.784 Y17.21 Z-0.895
N24 X3.85 Y17.157 Z-0.893
N25 X3.933 Y17.099 Z-0.89
N26 X3.993 Y17.062 Z-0.887
N27 X4.059 Y17.029 Z-0.884
N28 X4.137 Y16.996 Z-0.88
N29 X4.209 Y16.971 Z-0.876
N30 X4.311 Y16.943 Z-0.87
N31 X4.395 Y16.925 Z-0.866
N32 X4.513 Y16.904 Z-0.861
N33 X4.679 Y16.882 Z-0.855
N34 X4.752 Y16.874 Z-0.853
N35 X4.803 Y16.873 Z-0.854
N36 X4.877 Y16.879 Z-0.857
N37 X5.053 Y16.901 Z-0.866
N38 X5.171 Y16.921 Z-0.872
N39 X5.246 Y16.938 Z-0.875
N40 X5.315 Y16.957 Z-0.878
N41 X5.393 Y16.983 Z-0.88
N42 X5.471 Y17.016 Z-0.882


==================================================
Converted File

(1001)
(GrAduAted DiAl)
N10 G90 G94
N11 G17
N12 G21

(EngrAve3)
N13 M9
N14 T1 M6
N15 S16500 M3
N16 G54
N17 G0 A3.489 Y17.501
N18 Z10
N19 Z3
N20 G1 Z-0.913 F635
N21 A3.603 Y17.38 Z-0.904
N22 A3.703 Y17.281 Z-0.898
N23 A3.784 Y17.21 Z-0.895
N24 A3.85 Y17.157 Z-0.893
N25 A3.933 Y17.099 Z-0.89
N26 A3.993 Y17.062 Z-0.887
N27 A4.059 Y17.029 Z-0.884
N28 A4.137 Y16.996 Z-0.88
N29 A4.209 Y16.971 Z-0.876
N30 A4.311 Y16.943 Z-0.87
N31 A4.395 Y16.925 Z-0.866
N32 A4.513 Y16.904 Z-0.861
N33 A4.679 Y16.882 Z-0.855
N34 A4.752 Y16.874 Z-0.853
N35 A4.803 Y16.873 Z-0.854
N36 A4.877 Y16.879 Z-0.857
N37 A5.053 Y16.901 Z-0.866
N38 A5.171 Y16.921 Z-0.872
N39 A5.246 Y16.938 Z-0.875
N40 A5.315 Y16.957 Z-0.878
