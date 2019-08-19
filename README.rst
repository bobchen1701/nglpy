=====
nglpy
=====

.. introduction

A Python wrapped version of the [Neighborhood Graph Library
(NGL_) developed by Carlos Correa and Peter Lindstrom.

.. _NGL: http://www.ngraph.org/

.. LONG_DESCRIPTION

NGLPY but modified to generate relative neighborhood graphs in a python environment.

.. END_LONG_DESCRIPTION

.. end_introduction

.. install

Modified Installation
============

Must get the most up-to-date xcode and commandline tools 

::

    sudo rm -rf /Library/Developer/CommandLineTools
    
    xcode-select --install
    
    sudo installer -pkg /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg -target /
    
    pip install . 

.. end-install

.. usage

Usage
=====

Then you can use the library from python such as the example below::

    import nglpy
    import numpy as np

    point_set = np.random.rand(100,2)
    max_neighbors = 9
    beta = 1

    # TODO: Make this an enum, remove hard-coding
    graph_type = 'beta skeleton'

    aGraph = nglpy.Graph(point_set, graph_type, max_neighbors, beta)

    aGraph.neighbors()

.. end-usage
