# batch-image-resizer
A shell script that resizes to a given width preserving aspect ratio all the images of a folder recursively.

## Dependency
The script needs the package ```imagemagick``` installed on your system :
```sudo apt install imagemagick -y```

## Usage

```./batch-image-resizer.sh -d /path/to/root/directory -s 1920 -q 80```  
where  
-d = directory  
-s = max size of files that will be resized  
-q = quality of compression, this argument is optional and will defaut to 90  

This will parse recursively the folder ```/path/to/root/directory``` for .jpg/.jpeg and .png files bigger than 1920px width and resize them in place to 1920px width keeping their aspect ratio. Any parsed file with a width smaller than 1920px would be left untouched.
