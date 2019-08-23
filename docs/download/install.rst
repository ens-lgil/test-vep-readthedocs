.. VEP installation documentation

.. highlight:: shell

Installation
~~~~~~~~~~~~

Requirements
============

VEP requires:

* **gcc**, **g++** and **make**
* **Perl** version **5.10** or above recommended (tested on 5.10, 5.14, 5.18, 5.22, 5.26)
* **Perl** packages

    * `Archive::Zip <https://metacpan.org/pod/Archive::Zip>`_
    * `DBD::mysql <https://metacpan.org/pod/DBD::mysql>`_
    * `DBI <https://metacpan.org/pod/DBI>`_

    See `this guide <http://www.cpan.org/modules/INSTALL.html>`_ for more information on how to install perl modules.
    :ref:`Additional libraries <additional>` can be installed for extra features and enhancements but they are not required to run VEP in most of the use cases.

VEP's INSTALL.pl script will install required components of Ensembl API for you, but VEP may also be used with any pre-existing API installations you have,
**provided their versions match the version of VEP you are using**.

VEP has been developed for UNIX-like environments and works well on Linux (e.g. Ubuntu, Debian, Mint) and Mac OSX.
It can also be used on :ref:`Windows <windows>` systems with a more involved installation process.


Installation
============

VEP's INSTALL.pl makes it easy to set up your environment for using the VEP. It will download and configure a minimal set of the Ensembl API for use by the VEP,
and can also download `cache files </vep_cache.html#cache>`_, `FASTA files </vep_cache.html#fasta>`_ and `plugins </vep_plugins.html>`_.

Run the following, and follow any prompts as they appear:

::

  perl INSTALL.pl


:ref:`Additional non-essential components <additional>` and enhancements must be installed manually.


**Software components installed**

* `BioPerl <https://github.com/bioperl/bioperl-live>`_
* `ensembl <https://github.com/Ensembl/ensembl>`_
* `ensembl-io <https://github.com/Ensembl/ensembl-io>`_
* `ensembl-variation <https://github.com/Ensembl/ensembl-variation>`_
* `ensembl-funcgen <https://github.com/Ensembl/ensembl-funcgen>`_
* `Bio::DB::HTS <https://github.com/Ensembl/Bio-DB-HTS>`_ (and `htslib <https://github.com/samtools/htslib>`_)

If you already have the latest version of the API installed you do not need to run the installer, although it can be used to simply update your API version (with post-release patches applied),
and retrieve cache and FASTA files. The installer downloads the API within the VEP directory and will not affect any other Ensembl API installations.

The script will also attempt to install a Perl::XS module, `Bio::DB::HTS <https://github.com/Ensembl/Bio-DB-HTS>`_, for rapid access to bgzipped FASTA files.
If this fails, you may add the `--NO_HTSLIB` flag when running the installer; VEP will fall back to using Bio::DB::Fasta for this functionality (`more details </vep_cache.html#fasta>`_).

**Running the installer**

The installer is run on the command line as follows:

::

  perl INSTALL.pl [options]

Follow on-screen prompts and note warnings of any files which will be deleted/overwritten

You should not need to add any options, but configuration of the installer is possible with the following flags:

.. list-table::
   :widths: 15 10 75
   :header-rows: 1

   * - Flag
     - Alternate
     - Description
   * - -\\-ASSEMBLY
     - -y
     - Assembly version to use when using ``--AUTO``. Most species have only one assembly available on each software release; currently this is only required for human.
   * - -\\-AUTO
     - -a
     - Run installer without prompts. Use the following options to specify parts to install:

        * **a** (API + Bio::DB::HTS/htslib)
        * **l** (Bio::DB::HTS/htslib only)
        * **c** (cache)
        * **f** (FASTA)
        * **p** (plugins) —- Require the use of the ``--PLUGINS`` flag to list the plugin(s) to install.

        e.g. for API and cache:
        ::

          perl INSTALL.pl --AUTO ac
   * - -\\-CACHE_VERSION [version]
     -
     - By default the installer will download the latest version of VEP caches and FASTA files (currently 97). You can force the script to install a different version, but there is no guarantee that a version of the API will be compatible with a different version of the cache.
   * - -\\-CACHEDIR [dir]
     - -c
     - By default the script will install the cache files in the ".vep" subdirectory in your home area. This option configures where cache files are installed. The --dir flag must be passed when running the VEP if a non-default directory is given:
       ::

         ./vep --dir [dir]
   * - -\\-DESTDIR [dir]
     - -d
     - By default the script will install the API modules in a subdirectory of the current directory named "Bio". Using this option you can configure where the Bio directory is created.
       If something other than the default is used, this directory must either be added to your **PERL5LIB** environment variable when running the VEP, or included using perl's -I flag:
       ::

         perl -I [dir] vep
   * - -\\-NO_HTSLIB
     - -l
     - Don't attempt to install Bio::DB::HTS/htslib.
   * - -\\-NO_TEST
     -
     - Don't run API tests - useful if you know a harmless failure will prevent continuation of the installer.
   * - -\\-NO_UPDATE
     - -n
     - By default the script will check for new versions or updates of the VEP. Using this option will skip this check.
   * - -\\-PLUGINS
     - g
     - Comma-separated list of plugins to install when using ``--AUTO``. To install all available plugins, use ``--PLUGINS all``.
       ::

         # List the available plugins:
         perl INSTALL.pl -a p --PLUGINS list
         # Download/install all the available plugins:
         perl INSTALL.pl -a p --PLUGINS all
         # Download/install a defined list of plugins, e.g.:
         perl INSTALL.pl -a p --PLUGINS dbNSFP,CADD,G2P
   * - -\\-PREFER_BIN
     - -p
     - Use this if the installer fails with out of memory errors.
   * - -\\-SPECIES
     - -s
     - Comma-separated list of species to install when using ``--AUTO``.
       To install the RefSeq cache, add **_refseq** to the species name, e.g. "homo_sapiens_refseq", or **_merged** to install the merged Ensembl/RefSeq cache.
       Remember to use `--refseq </vep_options.html#opt_refseq>`_ or `--merged </vep_options.html#opt_merged>`_ when running the VEP with the relevant cache!
   * - -\\-QUIET
     - -q
     - Don't write any status output when using ``--AUTO``.


.. _additional:

Additional components
=====================


Using VEP in Mac OS
===================

.. _windows:

Using VEP in Windows
====================
