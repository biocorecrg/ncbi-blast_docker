BootStrap: debootstrap
OSVersion: stretch
MirrorURL:  http://ftp.fr.debian.org/debian/
Include: curl perl-modules-5.24 libencode-perl

%runscript
    echo "Welcome to BiocoreCRG NCBI Blast Image"

%post

	BLAST_VERSION=2.8.1

	cd /usr/local; curl --fail --silent --show-error --location --remote-name ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/${BLAST_VERSION}/ncbi-blast-${BLAST_VERSION}+-x64-linux.tar.gz
	cd /usr/local; tar zxf ncbi-blast-${BLAST_VERSION}+-x64-linux.tar.gz; rm ncbi-blast-${BLAST_VERSION}+-x64-linux.tar.gz
	cd /usr/local/bin; ln -s /usr/local/ncbi-blast-${BLAST_VERSION}+/bin/* .

%labels
	Maintainer Biocorecrg
	Version 0.1.0

