V-Xtractor An open-source, high-throughput software tool to identify and
extract hypervariable regions of small subunit ribosomal RNA gene sequences 

Source code available at:
http://www.cmde.science.ubc.ca/mohn/software.html

Version: 2.0
Purpose: Extraction of variable subregions from SSU rRNA sequences
Copyright (c) Hartmann et al. 2010
Contact: Martin Hartmann (martinha(at)interchange.ubc.ca)
University of British Columbia, Department of Microbiology
and Immunology, V6T 1Z3 Vancouver, Canada
Programmer: Charles Howes (vxtractor(at)ch.pkts.ca)

The full installation instructions can be found in the file UsersGuide.pdf
Quick installation instructions can be found below.


1) Perl and HMMER

Perl is available at http://www.perl.org/

Installing HMMER version 3
note: V-Xtractor 2.0 requires HMMER version 3. An older version of
V-Xtractor running on HMMER version 2 can be provided on request.

 - download			http://hmmer.janelia.org/#download  
 - uncompress/unpack		tar zxf hmmer-3.0.tar.gz
 - move to new directory	cd hmmer-3.0
 - configure			./configure
 - build			make
 - automated tests		make check
 - automated install		make install

Precompiled binaries are available for some operating systems. They can be found in the "binaries/" directory after the unpacking the tarball. Installing the package takes nothing more than moving these binaries wherever you want them (e.g. /usr/local/bin).


2) V-Xtractor

 - download	http://www.cmde.science.ubc.ca/mohn/software.html
 - unpack	"unzip vxtractor.pl"


3) Input file and running V-Xtractor

Use sequences in FASTA formatted input file. Copy FASTA file to directory containing vxtractor.pl. Move into this directory with "cd path/". Typing "perl vxtractor.pl" lists all options of the program.

Example:perl vxtractor.pl -a -r .V1-V3. -h HMMs/bacteria/ -o out.fasta  in.fasta
 -- this will extract V1 through V3, for bacteria, from the file in.fasta and
    save the results to out.fasta, checking correct order of V1, V2, and V3.

