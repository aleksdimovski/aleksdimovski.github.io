
AVP+SPIN

1. Install SPIN (Version 6.4.5) and add its directory to your search path, such that the following commands are runnable: 
>> spin -a *.pml
>> gcc -o pan pan.c
>> ./pan -a -n -N p

2. Download ARP.zip, Lib.zip, BenchmarksARP.zip; and unzip them in the same directory

3. BenchmarksARP.zip contains:
  - various versions of synthetic example: fwarm2-0.pml has 2 features and checks the assertion i>=0
										   fwarm24-1.pml has 24 features and checks the assertion i>=1
  - minepump example: minepumpARP.pml
  - elevator example: elevatorARP.pml

4. Run the tool by:
>> java -cp "antlr-4.5.3-complete.jar:." Root fwarm2-1.pml

5. The assertions and deadlock-freedom for fwarm*-*.pml and minepumpARP.pml are checked automatically without specfying additional arguments.
>> java -cp "antlr-4.5.3-complete.jar:." Root minepumpARP.pml

6. To verify some LTL properties for minepumpARP.pml and elevatorARP.pml, select as a second argument to Root the property number 
(p2 for \phi_2, p3 for \phi_3, p4 for \phi_4, p5 for \phi_5, where \phi_2, \phi_3, \phi_4, \phi_5 are properties described in our paper FASE'17 and TOSEM). For example,
>> java -cp "antlr-4.5.3-complete.jar:." Root minepumpARP.pml p2
>> java -cp "antlr-4.5.3-complete.jar:." Root elevatorARP.pml p1


AVP+UPPAAL

1. Install UPPAAL (Version 4.0.13) and add its directory to your search path.

2. Download train.zip; and unzip it.

3. train.zip contains:
  - all variants of train-gate example: train-gate1.xml to train-gate16.xml
  - join abstraction of train-gate example: train-gateJoin.xml
  - the considered properites: train-gate1.q to train-gate4.q

4. Run the tool by:
>> time verifyta -u train-gate1.xml train-gate1.q