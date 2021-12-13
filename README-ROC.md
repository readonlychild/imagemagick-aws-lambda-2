# ImageMagick Lambda Layer for Amazon Linux 2 AMIs

## Steps for Makefile_Layer20

On Docker Desktop, get image

`amazonlinux` IMAGE ID `f9d4a99f2542` approx size `163.85MB`

Run it, and go into it:

`> docker exec -it --user root **pensive_banach** /bin/bash`

Replace **pensive_banach** with container name

yum install update  
yum groupinstall "Development Tools"  
yum install cmake  
git clone https://github.com/readonlychild/imagemagick-aws-lambda-2.git  
cd ima<tab>  
rm Makefile  

make all -f Makefile_Layer20  

### Shortcomings

* This build does not support clippingPath (missing xml)  
* This build does not support avif



<pre>
bash-4.2# /opt/bin/magick --version
Version: ImageMagick 7.1.0-17 Q16-HDRI x86_64 2021-11-21 https://imagemagick.org
Copyright: (C) 1999-2021 ImageMagick Studio LLC
License: https://imagemagick.org/script/license.php
Features: Cipher DPC HDRI
Delegates (built-in): bzlib freetype heic jng jp2 jpeg lcms png tiff webp zlib
Compiler: gcc (7.3)
</pre>


## Steps for Makefile_Layer39

Same as Layer20, but before `make`, install python3:

`yum install python3`  
`make all -f Makefile_Layer39`

====

Now need to figure out `avif` support


