# Using Guide 
# 2016/08/22

1. directory description:
	
\dataset: include all the types of biobirck files, there are several gene strings in each file.
	
\testData:include some relation matrix files used in our experiment. 
		*.xlsx and *_knn.xlsx files are ready for le and isomap. matching between matrixs and string files is as follow:  
		t2*.xlsx: Protein_Generator and Protein_Domain
		t3*.xlsx: Protein_Generator and RBS
		t4*.xlsx: Primer and Protein_Domain
		t5*.xlsx: Primer and RBS
		t6*.xlsx: Protein_Domain and RBS
	
\python:  include one exe file ,main.exe, and other necessary files. 
		you can combine two gene string files, compute their edit distance and get their relation matrix.
	 
	        
\matlab:  include two exe files, runLE and runISOMAP. 
		they are used to deal with relation matrix by LE and ISOMAP

2. relation matrix:
	
	if you want to compute edit distance between every two biobricks in two different files and get relation matrix. First you need put two files from '\dataset' into '\python'. Then running main.exe in cmd by command 'main'. And then you need input three necessary parameters at first of program. the third parameter is used to tell program you want add 'knn' step or not in computing process. Remember you need knn in process, if this relation matrix is for isomap!

3. reduction dimsion by LE or ISOMAP:						 
	
	After get relation matrix you want, please put it in '\matlab'. Before running ang program you need review how many strings in two gene string files, remember two numbers as num1 and num2. Now you can run program in cmd with some parameters. Right commands are as follow: 'runLE(or runISOMAP) <filename> <num1> <num2>'. 
	
	we put test files, le_test.xlsx and lsomap_test.xlsx for two exe files in '\matlab', and they were built by two same string files(Protein_Generator and Primer). Both of these string files include 500 strings. So you need the command as the example: <runLE le_test 500 500> or <runLSOMAP isomap_test 500 500>
	
		
							
						 