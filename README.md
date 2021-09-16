# EGAdataManagement

*Uploading to EGA*
---

- create a folder containing all samples waiting to upload

- download EGA Cryptor tools

- cryption
```
java -jar ../EgaCryptor.jar -file file.name1 file.name2 (or * indicates all files)

Three files will be generated for each: md5 file, gpg file and gpg.md5 file
```

- upload
```
 ml Aspera-Connect
 
 ascp -P33001 -O33001 -QT  L files(all output above)  ega-box-764@fasp.ega.ebi.ac.uk:/
 
 Password: XXXXXXXXXXXX
 
```

*Linking uploaded samples to exist 1000IBD study*
---

```
Webpage: https://ega-archive.org/submitter-portal/#/

Click new submissions

Add title and descriptions of uploaded samples/datasets

Register samples: upload csv file which contains detailed information. 
Note: alia is the most important link in EGA. Each alia indicates one sample (paired-end, bam, fasta etc.). This should be consistent with later runs/experiments.
Example can be found in Examples folder.

Define one or more experiments. Choose exist study (e.g. 1000IBD). Select the correct libray information. No sample infor need here.

Link files and samples. Choose experiment from last step. Upload csv file which contains raw sequencing information. Alias must be the same with sample registering.
This step might take some time and easily get errors. Example can be found in Examples folder.

If there is error that one sample must be defined in the experiment, then go back to "Link files and samples". Something wrong there.

At last, go for submission!

```
