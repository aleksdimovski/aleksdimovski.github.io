
fNUSMV approach

1. Install NuSMV (version 2.5.4) and add its directory to your search path, such that the following command is runnable: 
>> NuSMV -r -df -dynamic *.smv

2. Download examples_nusmv.zip and unzip it in the same directory

3. Run the tool by:
>> time NuSMV -r -df -dynamic feat2-0.smv


Verify approach

1. Download verify.jar then run it:
>> java -jar verify.jar 0 7
>> java -jar verify.jar 1 7
Note that we pass 2 arguments to the main program:
- the first is the property we verify: use 0 for \phi_0 and 1 for \phi_1, and 
- the second is the number of available feautres (e.g. n = 2, 7, 10, 14) 

2. Alternative way to test Verify approach is to download and unzip verify_sources.zip, then run it:
>> javac *.java
>> java App 0 7
>> java App 1 7 
