This is an image registration Matlab program corresponding to the paper Two
and Three Dimensional Image Registration Based on B-Spline Composition and
Level Sets (DOI: https://doi.org/10.4208/cicp.OA-2016-0042 or https://github.com/stellaccl/cdmffd-image-registration/blob/master/docs/ImageRegistration.pdf). If you find this
code useful for your research, a citation to the above reference would be 
appreciated.

It contains two main folders,
the 2D_multiresolution, and the 3D_multiresolution. This code works any pair
of images provided that they are of the same size.  Other than the given 
examples, other images can be used by saving them in the corresponding folder
and assigning them as I0 (moving image) and I1 (fixed image).

For more details on how to use this code, see the files Description_2D.txt
and Description_3D.txt 

Part of the code used the parfor loop which accelerates the program by performing
parallel computing (provided the Parallel Computing Toolbox is available). 
Also, the code can further speed up by using Mex-compiled functions. Mex files
compiled with MATLAB 2015b for Windows 64-bit, Linux and OS X are included
in the distribution. 

If the included Mex files do not work (for example due to differences in the
MATLAB version), they can be generated by running the scripts which use codegen
from the "Coder" toolbox:

`make_mex_files2D.m` (in the folder 2D_multiresolution) and 

`make_mex_files3D.m` (in the folder 3D image registration).

Short description about important variables used in the code can be find in
variableList2D.txt and variableList3D.txt.

Main files for included examples:

`2D_multiresolution/main2DLena.m` - Lena example

`2D_multiresolution/main2DLenaSynthetic.m` - Lena example with a synthetic transformation

`2D_multiresolution/main2DCShape.m` - Circle to C-Shape registration

`3D_multiresolution/main3D.m` - Sphere to Sun-shape registration

`3D_multiresolution/main3DDiceSimilarity` - Registration of MRI images obtained
from http://brainweb.bic.mni.mcgill.ca/brainweb/ (a reader for the rawb format
is included).

