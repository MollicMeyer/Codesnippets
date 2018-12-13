# Codesnippets
## Code without a home. 
### Python v 2.7 with arcpy site package and os module

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
