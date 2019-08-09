Download
~~~~~~~~

Download ensembl-vep package (see below the different ways to download it) and then follow the :ref:`download/install`.

Using Git
=========

- :Clone the Git repository:

Use git to download the ensembl-vep package:

::

    git clone https://github.com/Ensembl/ensembl-vep.git
    cd ensembl-vep
    
- :Update to a newer version:

To update from a previous version:

::

    cd ensembl-vep
    git pull
    git checkout release/97
    perl INSTALL.pl
