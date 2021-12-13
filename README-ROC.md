# ImageMagick Lambda Layer for Amazon Linux 2 AMIs

## Stpes for Makefile_Layer20

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


