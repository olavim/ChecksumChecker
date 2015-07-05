# Checksum Checker

## How to run

in the commandline:

  java -jar ChecksumChecker.jar [-MD5|SHA1] [-o] [-r] <file> [file]


## Usage

### Output

By default, calculated checksums are printed to the console and written into a
checksum.txt file. To change the output file, use the -o argument:

  java -jar ChecksumChecker.jar -o outputfile <file(s)>

### Algorithms

The checksum can be calculated with either MD5 or SHA1 algorithm. The program uses
MD5 by default. To specify the algorithm:

  java -jar ChecksumChecker.jar -MD5 <file(s)>
or
  java -jar ChecksumChecker.jar -SHA1 <file(s)>

### Directory traversing

By default, if a directory or directories are given to the program, only the checksums of
the files in the specified directories' roots are calculated. To recursively traverse the
directory structure and calculate the checksums of all the files there, use the -r argument:

  java -jar ChecksumChecker.jar -r <file>


## Examples

Calculate the checksums of all files in the current directory to a c.txt file:

  java -jar ChecksumChecker.jar -o c.txt .

Calculate the checksums of a.txt and b.exe:

  java -jar ChecksumChecker.jar a.txt b.exe