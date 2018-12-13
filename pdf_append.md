# Codesnippets
## Code without a home. 
### Python v 2.7 with arcpy site package and os and glob modules
#### creates a merged pdf from a list of pdfs
#### requires 1) script saved to working directory where merged pdf will be saved; 2) the path of folder containing pdfs to be merged

```
## import modules
import arcpy, os, glob

path = os.getcwd()
pdffolder = "somepdffolder"
pdfPath = path + '\\' + "merged.pdf"

os.chdir(pdffolder)
pdflist = glob.glob(*.pdf)

## merge pdfs in list
for pdfs in pdflist:
	pdfPath.appendpages(pdfs)
	
pdfPath.saveAndClose()
del pdfPath
