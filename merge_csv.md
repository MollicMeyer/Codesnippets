### Codesnippets
##Code without a home.

#import modules
import sys, os

def mergeCSV(srcDir, destCSV, filename):
    with open(destCSV, 'w') as destFile:
        header = ''
        for root, dirs, files in os.walk(srcDir):
            for f in files:
                if f == str(filename):
                    with open(os.path.join(root, f), 'r') as csvfile:
                        if header == '':
                            header=csvfile.readline()
                            destFile.write(header)
                        else:
                            csvfile.readline()
                            for line in csvfile:
                                destFile.write(line)
