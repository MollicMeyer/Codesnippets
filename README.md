# Codesnippets
Code without a home. 

list1 = [j for j in range(3,42,1) if j %2 != 0]
list2 = [k for k in range(47,138,6) if k %2 != 0]
list3 = [l for l in range (43,204,10) if l %2 != 0]

import grass.script as gscript

def main():

    gscript.run_command('g.region', raster=coahoma_dem3m)



method_n = ["aspect"]

naming = ["asp_"]

#single 



for i in list1:

    oname= "asp_" + str(i*3).zfill(3)+"m"

    gscript.run_command("r.param.scale", overwrite="T", input = 'coahoma_dem3m@PERMANENT', output = oname, size = i, method = method_n)

    outname = oname+".tif"

    AddLayer(oname)

    gscript.run_command("r.out.gdal", overwrite="T", input= oname, format = "GTiff", output = "T:\\AgTechInventures\\Mississippi\\data\\DTA\\asp\\"+outname)

for j in list2:

    oname= "asp_" + str(j*3).zfill(3)+"m"

    gscript.run_command("r.param.scale", overwrite="T", input = 'coahoma_dem3m@PERMANENT', output = oname, size = j, method = method_n)

    outname = oname+".tif"

    AddLayer(oname)

    gscript.run_command("r.out.gdal", overwrite="T", input= oname, format = "GTiff", output = "T:\\AgTechInventures\\Mississippi\\data\\DTA\\asp\\"+outname)

for k in list3:

    oname= "asp_" + str(k*10).zfill(3)+"m"

    gscript.run_command("r.param.scale", overwrite="T", input = 'coahoma_dem10m@PERMANENT', output = oname, size = k, method = method_n)

    outname = oname+".tif"

    AddLayer(oname)

    gscript.run_command("r.out.gdal", overwrite="T", input= oname, format = "GTiff", output = "T:\\AgTechInventures\\Mississippi\\data\\DTA\\asp\\"+outname)
