# hydroid-conda
[HYDROID](https://github.com/ncbi/HYDROID) recipe for Anaconda



## Building and uploading to Anaconda cloud
```
conda install -y conda-build
conda update -n root -y conda-build
conda install -y anaconda-client
anaconda login

mv hydroid h
conda-build -c hydroid h
anaconda upload path_to_package #or toggle automatic upload with: conda config --set anaconda_upload True
conda convert --platform all path_to_package -o output/
#find output/ -name 'hydroid*' -exec anaconda upload {} \;
#Manually upload for OSX and Linux
#For windows32 repeat the above steps with deactivated freesasa module in meta.yml (freesasa module for win32 is not currently available)
```

## Installing HYDROID from Anaconda cloud

```
conda install -c hydroid hydroid
```
