
We have used 3 approaches to verify two models (Synthetic example and Elevator). 
We use 64-bit Windows 8.1 Pro, 8GB.
We use Cygwin terminal.


fNUSMV APPROACH

1. Install NuSMV (version 2.5.4) and add its directory to your search path, such that the following command is runnable: 
>> NuSMV -r -df -dynamic *.smv

2. Download examples_nusmv.zip and unzip it in the same directory

3. Run the tool by:
>> time NuSMV -r -df -dynamic feat2-0.smv (to check \Phi_0 property from Synthetic example)
>> time NuSMV -r -df -dynamic feat2-1.smv (to check \Phi_1 property from Synthetic example)
>> time NuSMV -r -df -dynamic feat2-2.smv (to check \Phi_2 property from Synthetic example)
>> time NuSMV -r -df -dynamic feat2-3.smv (to check \Phi_3 property from Synthetic example)
>> time NuSMV -r -df -dynamic elevator4.smv (to check P1, P2, P3, and P4 properties from Elevator example)


VERIFY and GEN-VERIFY APPROACHES

1. Synthetic Example 

- Download verify.jar then run it:
>> java -jar verify.jar 0 7
>> java -jar verify.jar 1 7
>> java -jar verify.jar 3 7
>> java -jar verify.jar 3 7 gen
Note that we pass 2 arguments to the main program:
- the first is the property we verify: use 0 for \phi_0 and 1 for \phi_1, and 
- the second is the number of available feautres (e.g. n = 2, 7, 10, 14) 
The 3rd argument is optional: use "gen" to run "Gen-Verify" procedure  

- Alternative way to test Verify and Gen-Verify approaches is to download and unzip verify_sources.zip, then run it:
>> javac *.java
>> java App 0 7
>> java App 1 7 
>> java App 3 7 gen


2. Elevator 

- Download verify_elevator.jar then run it:
>> java -jar verify_elevator.jar P1
>> java -jar verify_elevator.jar P2
>> java -jar verify_elevator.jar P3
>> java -jar verify_elevator.jar P4
Note that we pass 1 argument (the property we want to verify) to the main program, where:
-  P1 = EF(floor=1 & idle & door=closed)
-  P2 = AF(floor=1 & idle & door=closed)
-  P3 = EF ((floor=3 & !liftBut3.pressed & direction=up) -> door=closed) 
-  P4 = EF(AX(door=open))

- Alternative way to test Verify approach is to download and unzip verify_elevator_sources.zip, then run it:
>> javac *.java
>> java App P1
>> java App P2 
>> java App P3
