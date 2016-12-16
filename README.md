# Sentiment-CNN-extraction





## Requirement

### Caffe (for mac OsX)

###### General dependencies

```unix
brew install -vd snappy leveldb gflags glog szip lmdb
# need the homebrew science source for OpenCV and hdf5
brew tap homebrew/science
brew install homebrew/science/hdf5 #to be sure..
brew install hdf5 opencv
```
If using Anaconda Python, a modification to the OpenCV formula might be needed Do brew edit opencv and change the lines that look like the two lines below to exactly the two lines below.

```unix
-DPYTHON_LIBRARY=#{py_prefix}/lib/libpython2.7.dylib
-DPYTHON_INCLUDE_DIR=#{py_prefix}/include/python2.7
```

If using Anaconda Python, HDF5 is bundled and the hdf5 formula can be skipped.


##### Remaining dependencies, with / without Python

```unix
# with Python pycaffe needs dependencies built from source
brew install --build-from-source --with-python -vd protobuf
brew install --build-from-source -vd boost boost-python
# without Python the usual installation suffices
brew install protobuf boost
```
