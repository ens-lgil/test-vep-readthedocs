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
