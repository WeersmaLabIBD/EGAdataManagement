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
