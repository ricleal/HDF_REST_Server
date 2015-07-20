# HDF_REST_Server

HDF REST server is a Python-based web service that can be used to send and receive HDF5 data using an HTTP-based REST interface.

![HDF REST API ](https://www.hdfgroup.org/images/RESTfulHDF5.png)


Server running at:

http://data.hdfgroup.org:7253

Basic information about the data collection "tall" (originally from the file tall.h5):

http://tall.data.hdfgroup.org:7253

```
Showing contents for:  ../hdf5-json/data/hdf5/tall.h5
@attr1: 97
@attr2: [0 1]
g1 
  g1.1 
    dset1.1.1 int32 10x10 
      @attr1: 49
      @attr2: 50
    dset1.1.2 int32 20 
      [ 0  1  2 ..., 17 18 19]
```

To read an attribute:

http://tall.data.hdfgroup.org:7253/groups/345239f2-963f-11e4-b8cf-06fc179afd5e/attributes/attr1

Sub-region of the dataset:

http://tall.data.hdfgroup.org:7253/datasets/3452be54-963f-11e4-b8cf-06fc179afd5e/value?select=[0:4,0:4]

Note: objects are identified via a UUID (universally unique identifier) rather than (potentially ambiguous) path names.

Supports http methods:
- POST
- PUT
- DELETE

To create, update, and delete operations (comparable to what you would find in the HDF5 library).



