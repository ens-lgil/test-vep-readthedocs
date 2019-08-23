.. Documentation for VEP download

.. highlight:: shell

Download
~~~~~~~~

Download ensembl-vep package (see below the different ways to download it) and then follow the `Installation instructions <https://test-vep-readthedocs.readthedocs.io/en/latest/download/install.html>`.


Using Git
=========

* **Clone the Git repository**

Use git to download the ensembl-vep package:

::

    git clone https://github.com/Ensembl/ensembl-vep.git
    cd ensembl-vep

* **Update to a newer version**

To update from a previous version:

::

    cd ensembl-vep
    git pull
    git checkout release/97
    perl INSTALL.pl


* **Use an older version**

To use an older version (this example shows how to set up release 87):

::

    cd ensembl-vep
    git checkout release/87
    perl INSTALL.pl


Download the Zipped package file
================================

Users without the git utility installed may download a zip file from GitHub, though we would always recommend using git if possible.

::

    curl -L -O https://github.com/Ensembl/ensembl-vep/archive/release/97.zip
    unzip 97.zip
    cd ensembl-vep-release-97/


Previous versions (ensembl-tools)
=================================

Previously VEP was available as part of the ensembl-tools package (see the Ensembl archive site for documentation). The following downloads are available for archival purposes.

* `Download version 87 <https://github.com/Ensembl/ensembl-tools/archive/release/87.zip>`_ (Ensembl 87)
* `Download version 86 <https://github.com/Ensembl/ensembl-tools/archive/release/86.zip>`_ (Ensembl 86)
* `Download version 85 <https://github.com/Ensembl/ensembl-tools/archive/release/85.zip>`_ (Ensembl 85)
* `Download version 84 <https://github.com/Ensembl/ensembl-tools/archive/release/84.zip>`_ (Ensembl 84)
* `Download version 83 <https://github.com/Ensembl/ensembl-tools/archive/release/83.zip>`_ (Ensembl 83)
* `Download version 82 <https://github.com/Ensembl/ensembl-tools/archive/release/82.zip>`_ (Ensembl 82)
* `Download version 81 <https://github.com/Ensembl/ensembl-tools/archive/release/81.zip>`_ (Ensembl 81)
* `Download version 80 <https://github.com/Ensembl/ensembl-tools/archive/release/80.zip>`_ (Ensembl 80)
* `Download version 79 <https://github.com/Ensembl/ensembl-tools/archive/release/79.zip>`_ (Ensembl 79)
* `Download version 78 <https://github.com/Ensembl/ensembl-tools/archive/release/78.zip>`_ (Ensembl 78)
* `Download version 77 <https://github.com/Ensembl/ensembl-tools/archive/release/77.zip>`_ (Ensembl 77)
* `Download version 76 <https://github.com/Ensembl/ensembl-tools/archive/release/76.zip>`_ (Ensembl 76)
* `Download version 75 <https://github.com/Ensembl/ensembl-tools/archive/release/75.zip>`_ (Ensembl 75)
* `Download version 74 <https://github.com/Ensembl/ensembl-tools/archive/release/74.zip>`_ (Ensembl 74)
* `Download version 73 <https://github.com/Ensembl/ensembl-tools/archive/release/73.zip>`_ (Ensembl 73)
* `Download version 72 <https://github.com/Ensembl/ensembl-tools/archive/release/72.zip>`_ (Ensembl 72)
* `Download version 71 <https://github.com/Ensembl/ensembl-tools/archive/release/71.zip>`_ (Ensembl 71)
* `Download version 2.8 <https://github.com/Ensembl/ensembl-tools/archive/release/70.zip>`_ (Ensembl 70)
* `Download version 2.7 <https://github.com/Ensembl/ensembl-tools/archive/release/69.zip>`_ (Ensembl 69)
* `Download version 2.6 <https://github.com/Ensembl/ensembl-tools/archive/release/68.zip>`_ (Ensembl 68)
* `Download version 2.5 <https://github.com/Ensembl/ensembl-tools/archive/release/67.zip>`_ (Ensembl 67)
* `Download version 2.4 <https://github.com/Ensembl/ensembl-tools/archive/release/66.zip>`_ (Ensembl 66)
* `Download version 2.3 <https://github.com/Ensembl/ensembl-tools/archive/release/65.zip>`_ (Ensembl 65)
* `Download version 2.2 <https://github.com/Ensembl/ensembl-tools/archive/release/64.zip>`_ (Ensembl 64 - ensembl-tools/scripts/variant_effect_predictor)
* `Download version 2.1 <https://github.com/Ensembl/ensembl-tools/archive/release/63.zip>`_ (Ensembl 63)
* `Download version 2.0 <https://github.com/Ensembl/ensembl-tools/archive/release/62.zip>`_ (Ensembl 62 - ensembl-variation/scripts/examples)
