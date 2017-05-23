
1. Install SPIN and add its directory to your search path, such that the following commands are runnable: 
>> spin -a *.pml
>> gcc -o pan pan.c
>> ./pan -a -n -N p

2. Download ARP.zip, Lib.zip, BenchmarksARP.zip; and unzip them in the same directory

3. Run the tool by:
>> java -cp "antlr-4.5.3-complete.jar:." Root fwarm2-1.pml

4. The assertions and deadlock-freedom for fwarm*-*.pml and minepumpARP.pml are checked automatically without specfying additional arguments.
>> java -cp "antlr-4.5.3-complete.jar:." Root minepumpARP.pml

5. To verify some LTL properties for minepumpARP.pml and elevatorARP.pml, select as a second argument to Root the property number 
(p2 for \phi_2, p3 for \phi_3, p4 for \phi_4, p5 for \phi_5, where \phi_2, \phi_3, \phi_4, \phi_5 are properties described in our paper FASE'17 and TSE). For example,
>> java -cp "antlr-4.5.3-complete.jar:." Root minepumpARP.pml p2
>> java -cp "antlr-4.5.3-complete.jar:." Root elevatorARP.pml p1

