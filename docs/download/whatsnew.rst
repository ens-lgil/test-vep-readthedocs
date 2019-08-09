What's new
~~~~~~~~~~


New in version 97 (July 2019)
=============================

* Allele-specific clinical significance reported (it was previously variant-specific).
* New options:
    * `--clin_sig_allele </vep_options.html#opt_clin_sig_allele>`_: report allele specific clinical significance.
    * `--mane </vep_options.html#opt_mane>`_: report if a transcript is the MANE Select.
    * `--max_sv_size </vep_options.html#opt_max_sv_size>`_: extend the maximum Structural Variant size VEP can process.
    * `--no_check_variants_order </vep_options.html#opt_no_check_variants_order>`_: permit the use of unsorted input files (WARNING - this is slow and requires more memory).
  * `--overlaps </vep_options.html#opt_overlaps>`_: report the proportion and length of a transcript overlapped by a structural variant in VCF format.
* Include the --mane option into the --everything group option.
* Update --pick and --pick_order to support MANE Select transcripts.
* Check if the input variants are ordered: non ordered variants slow down VEP and require more memory.
* Skip annotation of complex and long structural variants and display a warning message.
* Variant recoder: add an option --vcf_string to return results in VCF format.
* VEP plugins:
    * FunMotifs - new: provide information about overlapping tissue-specific transcription factor motifs.
    * Mastermind - new: reports variants that have clinical evidence cited in the medical literature.
    * StructuralVariantOverlap - new: provide information from overlapping structural variants.
    * G2P - update: now the plugin can be run offline.
    * Phenotypes - update: change the format of the data file (from BED to GVF).
* VEP web tool: the transcript identifiers are now returned with versions unless otherwise specified.
* VEP installer: tabix-indexed variant cache files are now installed by default.


