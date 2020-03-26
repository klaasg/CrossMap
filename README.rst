A fork of liguowang/CrossMap
============================

**Main goal: providing a python (instead of CLI) interface to convert coordinates**

Installation:
-----------------------------
::

 pip3 install git+https://github.com/klaasg/CrossMap.git
 
if you want `pip freeze` to contain this github link instead of just 'CrossMap', use
::

 pip3 install -e git+https://github.com/klaasg/CrossMap.git#egg=CrossMap


Example usage:
-----------------------------
.. code:: python

    >>> import crossmap as cm
    >>>
    >>> (mapping, t, s) = cm.read_chain_file("/path/to/chain/file")
    >>> cm.convert_tuples(mapping, [("X", 10000, 20000), ("Y", 15000, 25000)])
    ([('X', 20000, 30000), ('Y', 25000, 35000)], [])
    # Result is a tuple of 1) a list of coordinates and 2) a list of errors
    >>> cm.convert_coordinates(mapping, ["X", "Y"], [10000, 15000], [20000, 25000])
    (['X', 'Y'], [20000, 25000], [30000, 35000], [])
    # Result is a tuple of chromosomes, start positions, end positions and a list of errors


See original documentation on where to download chain files

*Original README:*



Installation
==================

Use pip to install CrossMap
-----------------------------

::

 pip3 install git+https://github.com/liguowang/CrossMap.git

 or

 pip3 install CrossMap	#Install CrossMap supporting Python3


Documentation
=============

https://crossmap.readthedocs.io/en/latest/

