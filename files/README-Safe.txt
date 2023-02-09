
This documents shows how to use the tool tools from the paper 
¨Weakest Safe Context Synthesis by Symbolic Game Semantics and Logical Abduction¨

####################################################################################
## symbolicGC-safe --- Symbolic Game Checker for synthesizing weakest safe contexts ## 
####################################################################################

symbolicGC-safe is a research prototype designed for 
inferring weakest safe model specifications of unknown identifiers in the settings of game semantics.


## Author

	Aleksandar Dimovski
	
	
# Installation

The tool requires the following applications and libraries:

* Java: openjdk 11.0.17

* Yices2 

  sudo add-apt-repository ppa:sri-csl/formal-methods
  sudo apt-get update
  sudo apt-get install yices2
  
* Mistral SMT solver 
  Follow the installation instractions at https://www.cs.utexas.edu/~tdillig/mistral/index.html
  We have tested it on Ubunutu 18.04 LTS (we cannot install it on higher versions)
    

* Download symbolicGC-safe.tar.gz file and extract it by 

	$ tar -xvf symbolicGC-safe.tar.gz

* In the generated folder symbolicGC-safe, copy 'mistral' subfolder
   
The content of this folder should be: mistral symbolicGC-safe.jar term1.ia term2.ia term3.is 

Enter the folder symbolicGC-safe, and execute

	$ java -jar symbolicGC-safe.jar term1.ia 3

The generated output is in the file term1-Output.txt


# Benchmarks from the paper 

	$ java -jar symbolicGC-safe.jar term1.ia 3
	$ java -jar symbolicGC-safe.jar term1.ia 5
	$ java -jar symbolicGC-safe.jar term1.ia 7	
	$ java -jar symbolicGC-safe.jar term2.ia 3
	$ java -jar symbolicGC-safe.jar term2.ia 5
	$ java -jar symbolicGC-safe.jar term2.ia 7
