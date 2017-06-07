# V-Xtractor
Repository for V-Xtractor an open-source, high-throughput software tool to identify and extract hypervariable regions of small subunit (16S/18S) ribosomal RNA gene sequences

Authors: Hartmann M, Howes CG, Abarenkov K, Mohn WW, Nilsson RH.

Published in:
J Microbiol Methods. 2010 Nov;83(2):250-3. doi: 10.1016/j.mimet.2010.08.008. Epub 2010 Aug 27.
V-Xtractor: an open-source, high-throughput software tool to identify and extract hypervariable regions of small subunit (16S/18S) ribosomal RNA gene sequences.

Abstract:
V-Xtractor (http://www.cmde.science.ubc.ca/mohn/software.html) uses Hidden Markov Models to locate, verify, and extract defined hypervariable sequence segments (V1-V9) from bacterial, archaeal, and fungal small-subunit rRNA sequences. With a detection efficiency of 99.6% and low susceptibility to false-positives, this tool refines data reliability and facilitates subsequent analysis in community assays

Source code available at:
http://www.cmde.science.ubc.ca/mohn/software.html


Version: 2.0
Purpose: Extraction of variable subregions from SSU rRNA sequences
Copyright (c) Hartmann et al. 2010
University of British Columbia, Department of Microbiology
and Immunology, V6T 1Z3 Vancouver, Canada
Programmer: Charles Howes

The full installation instructions can be found in the file UsersGuide.pdf
Quick installation instructions can be found below.


## Requirements
### Perl and HMMER

Perl is available at http://www.perl.org/

Installing HMMER version 3
note: V-Xtractor 2.0 requires HMMER version 3. An older version of
V-Xtractor running on HMMER version 2 can be provided on request.

 - Download			http://hmmer.janelia.org/#download  
 - Uncompress/unpack		tar zxf hmmer-3.0.tar.gz
 - Move to new directory	cd hmmer-3.0
 - Configure			./configure
 - Build			make
 - Automated tests		make check
 - Automated install		make install

Precompiled binaries are available for some operating systems. Tdshey can be found in the "binaries/" directory after the unpacking the tarball. Installing the package takes nothing more than moving these binaries wherever you want them (e.g. /usr/local/bin).


## Running V-Xtractor

 - Download	from http://www.cmde.science.ubc.ca/mohn/software.html or here  V-Xtractor/vxtractor.pl

#### Input file and running V-Xtractor

Use sequences in FASTA formatted input file. Copy FASTA file to directory containing vxtractor.pl. Move into this directory with "cd path/". Typing "perl vxtractor.pl" lists all options of the program.

Example:perl vxtractor.pl -a -r .V1-V3. -h HMMs/bacteria/ -o out.fasta  in.fasta
 -- this will extract V1 through V3, for bacteria, from the file in.fasta and
    save the results to out.fasta, checking correct order of V1, V2, and V3.

### We have included all the Hidden Markov models for the different regoions in this compressed file V-Xtractor/HMMs.zip
