### Codesnippets
## Code without a home.

# import modules
import sys, os
# define source directory
#srcpath = 'some csv path'
# define csv list
#csv_list = [csvs]

# function inputs: source directory, file location of CSVs, list of csvs
def mergeCSV(srcDir, destCSV, csvlist):
    with open(destCSV, 'w') as destFile:
        for csv in csvlist:
			header = ''
        	for root, dirs, files in os.walk(srcDir):
            	for f in files:
                	if f == str(csv):
                    	with open(os.path.join(root, f), 'r') as csvfile:
                        	if header == '':
                            	header=csvfile.readline()
                            	destFile.write(header)
                       	 	else:
                            	csvfile.readline()
                            	for line in csvfile:
                                	destFile.write(line) 
									
# import function ##optional								
# from merge_csv import mergeCSV

## run function
mergeCSV(srcpath, srcpath + '//csvname.csv', csv_list)
