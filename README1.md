# `faops` operates fasta files

`faops` is a lightweight tool for operating sequences in the fasta format.

This tool can be regarded as a combination of `faCount`, `faSize`,
`faFrag`, `faRc`, `faSomeRecords`, `faFilter` and `faSplit` from
[UCSC Jim Kent's utilities](http://hgdownload.cse.ucsc.edu/admin/exe/).

Comparing to Kent's `fa*` utilities, `faops` is:

* much smaller (kilo vs mega bytes)
* easy to compile (only one external dependency)
* well tested
* contains only one executable file
* can operate gzipped (bgzipped) files
* and can be run under all major OSes (including Windows).

`faops` is also inspired/influenced/stealing from
[`seqtk`](https://github.com/lh3/seqtk) and[`ufasta`](http://www.genome.umd.edu/masurca.html).