This software implements a simulation of the eVACS vote counting system used in the Australian Capital Territory.


Developed by Ekaterina Lebedeva in the Australian National University.

-----------------------------------------------------------------
INPUT FILE FORMAT:
-----------------------------------------------------------------

id1 weight preference1 > preference2 > ... > preferenceN  
id2 weight preference1 > preference2 > ... > preferenceM  
id3 weight preference1 > preference2 >... > preferenceK  

Weight has to be a rational number.  
In the beginning of scrutiny weight is normally equal to 1/1.

Example:

1 1/1 A  
2 1/1 A > B  
3 1/1 B > A > C  
4 1/1 C  

Ballot papers of ACT elections 2008 and 2012 in the required format can be found in the folder PreferenceData. 


-----------------------------------------------------------------
HOW TO RUN THE EXECUTABLE
-----------------------------------------------------------------

java -jar countvotes-assembly-1.1.jar -d <directory where the input file is located> -f name_of_file.txt -a EVACS -n <number of vacant seats>

Example:


java -jar countvotes-assembly-1.1.jar -d /home/PreferenceData/ACT/2012/ -f Preferences_ACT_Brindabella_2012.txt -a EVACS -n 5


-----------------------------------------------------------------
OUTPUT
-----------------------------------------------------------------

Two files will be produced in <directory where the input file is located>:  
1) Report_EVACS_InputFile_name_of_file.txt  with the table of votes distribution  
2) WinnersByAlgorithm_EVACS_InputFile_name_of_file.txt  with the winners  


