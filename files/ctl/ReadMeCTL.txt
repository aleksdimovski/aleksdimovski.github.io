
1. Install NuSMV and add its directory to your search path, such that the following command is runnable: 
>> NuSMV -r -df -dynamic *.smv

2. Download synthetic.zip, elevator5.zip; and unzip them in the same directory

3. Run the tool (for elevator5.smv also uncomment the CTL property you want to verify) by:
>> time NuSMV -r -df -dynamic feat25.smv

