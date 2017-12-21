# hydroid-conda
[HYDROID](https://github.com/ncbi/HYDROID) recipe for Anaconda



## Building and uploading to Anaconda cloud
```
conda install conda-build
conda-build -c conda-forge -c hydroid hydroid
anaconda upload path_to_package
convert --platform all path_to_package -o output/
find output/ -name 'hydroid*' -exec anaconda upload {} \;
```

## Installing HYDROID from Anaconda cloud

```
conda install -c hydroid hydroid
```
