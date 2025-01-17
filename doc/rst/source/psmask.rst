.. index:: ! psmask
.. include:: module_core_purpose.rst_

******
psmask
******

|psmask_purpose|

Synopsis
--------

.. include:: common_SYN_OPTs.rst_

**gmt psmask** [ *table* ]
|SYN_OPT-I|
|-J|\ *parameters*
|SYN_OPT-R|
[ |SYN_OPT-B| ]
[ |-C| ]
[ |-D|\ *dumpfile* ]
[ |-F|\ [**l**\|\ **r**] ]
[ |-G|\ *fill* ]
[ |-K| ]
[ |-L|\ *nodegrid*\ [**+i**\|\ **o**] ]
[ |-N| ] [ |-O| ]
[ |-P| ] [ |-Q|\ *cut* ]
[ |-S|\ *search\_radius* ]
[ |-T| ]
[ |SYN_OPT-U| ]
[ |SYN_OPT-V| ]
[ |SYN_OPT-X| ]
[ |SYN_OPT-Y| ]
[ |SYN_OPT-bi| ]
[ |SYN_OPT-di| ]
[ |SYN_OPT-e| ]
[ |SYN_OPT-h| ]
[ |SYN_OPT-i| ]
[ |SYN_OPT-p| ]
[ |SYN_OPT-qi| ]
[ |SYN_OPT-r| ]
[ |SYN_OPT-t| ]
[ |SYN_OPT-w| ]
[ |SYN_OPT-:| ]
[ |SYN_OPT--| ]

**psmask** **-C** [ **-K** ] [ **-O** ]

.. include:: mask.rst
    :start-after: .. module_common_begins
    :end-before: .. module_common_ends

.. include:: common_classic.rst_

Examples
--------

.. include:: explain_example.rst_

To make an overlay that will mask out the regions of a
contour map where there is no control data using clip polygons, use:

   ::

    gmt psmask africa_grav.xyg -R20/40/20/40 -I5m -JM10i -O -K > mask.ps

We do it again, but this time we wish to save the clipping polygons to
file all_pols.txt:

   ::

    gmt psmask africa_grav.xyg -R20/40/20/40 -I5m -Dall_pols.txt

A repeat of the first example but this time we use white tiling:

   ::

    gmt psmask africa_grav.xyg -R20/40/20/40 -I5m -JM10i -T -O -K -Gwhite > mask.ps

See Also
--------

:doc:`gmt`, :doc:`gmtcolors`,
:doc:`grdmask`, :doc:`surface`,
:doc:`psbasemap`, :doc:`psclip`
