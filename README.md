# hydroid-conda
[HYDROID](https://github.com/ncbi/HYDROID) recipe for Anaconda



## Building and uploading to Anaconda cloud
```
conda install conda-build
conda update -n root conda-build
conda install anaconda-client
anaconda login

conda-build -c https://anaconda.org/hydroid/ hydroid
anaconda upload path_to_package
conda convert --platform all path_to_package -o output/
find output/ -name 'hydroid*' -exec anaconda upload {} \;
```

## Installing HYDROID from Anaconda cloud

```
conda install -c hydroid hydroid
```
