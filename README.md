# DMVFL-RSA
Improved Protein Relative Solvent Accessibility Prediction Using Deep Multi-View Feature Learning Framework

# Pre-requisite:

- Linux system

- python3.7, pytorch, numpy

- HHblits, uniclust30_2018_08  (http://wwwuser.gwdg.de/~compbiol/data/hhsuite/databases/hhsuite_dbs/)

- blast+, nr  (https://ftp.ncbi.nih.gov/blast/db/)

- PSIPRED VFORMAT (PSIPRED V3.2)

# Installation:

*Install and configure the softwares of Python3, Java, Pytorch, HHblits, uniclust30_2018_08, blast+, nr, ProtChain database, and PSIPRED in your Linux system. Please make sure that python3 includes the modules of 'os', 'math', 'numpy', 'configparser', 'numba', 'random', 'subprocess', 'sys', and 'shutil'. If any one modules does not exist, please using 'pip install XXXX' command install the python revelant module. Here, "XXXX" is one module name.

*Download this repository at https://github.com/XueQiangFan/DMVFL-RSA. Then, uncompress it and run the following command lines on Linux System.

  $ tar zxvf DMVFL-RSA.tar.gz
  $ chmod -R 777 ./DMVFL-RSA
  $ cd ./DMVFL-RSA
  Here, you will see two configuration files

*Configure the following tools or databases in Config.properties
  The file of "Config.properties" should be set as follows:

- HHblits, uniclust30_2018_08  (http://wwwuser.gwdg.de/~compbiol/data/hhsuite/databases/hhsuite_dbs/)

- blast+, nr  (https://ftp.ncbi.nih.gov/blast/db/)

- PSIPRED VFORMAT (PSIPRED V3.2)

- ProtChain databases (It can be downloaded from xstrongf.163.com) 

*Configure the following tools or databases in SPRSA.config
  The file of "Config.properties" should be set as follows:
- HHblits, uniclust30_2018_08  (http://wwwuser.gwdg.de/~compbiol/data/hhsuite/databases/hhsuite_dbs/)

# Run DMVFL-RSA? 

## run: python main.py -p protein name -S protein sequence -o result path

Brief introduction for protein solvent accessibility prediction by DMVFL-RSA

Step 0. generate an MSA (in a3m format) for your protein sequence from HHblits.

Step 1. generate one PSFM profile for your the MSA

Step 2. generate one PSSM profile and a PSS profile for your protein sequence from blast+ and PSIPRED.

Step 3. generate one RPRSA profile for your protein sequence from RPRSA-Threader

Step 4.  protein name +.rsa is the result file

# The protein solvent accessibility result

*The protein solvent accessibility result of each rsidue should be found in the outputted file, i.e., " protein name +.rsa". In each result file, where "NO" is the position of each residue in your protein, where "AA" is the name of each residue in your protein, where "RSA" is the predicted relative accessible surface area of each residue in your protein, and where "ASA" is the predicted accessible surface area of each residue in your protein.

# Update History:

First release 2021-08-03

# References

[1] Xue-Qiang Fan, Jun Hu*, Ning-Xin Jia, Dong-Jun Yu*, and Gui-Jun Zhang*. Improved Protein Relative Solvent Accessibility Prediction using Deep Multi-View Feature Learning Framework. Analytical Biochemistry. sumitted.

