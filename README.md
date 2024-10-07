 # Sample Data
 
 Sample data provided for VIVO installations.
 
 We have one [simple sample data set](./demovivo/README.md).  It includes people, organizations, papers, grants, memberships, 
 and other elements needed to demonstrate VIVO, and learn more about VIVO's approach to data representation. 

 There is also internationalized sample data set in [i18n directory](./i18n/README.md) 
 
 In addition, we have data from [OpenVIVO](http://openvivo.org) and from [VIVO at the University of Florida](http://vivo.ufl.edu).  These are "real world" data sets.
 
 ## Installation of sample data
 
 The data can be ingested by copying complete content except the README.md file of any subdirectory ([demovivo](./demovivo), [i18n](./i18n), 
 [openvivo](./openvivo), [uf](./uf)) into the VIVO_HOME/rdf/ directory and restarting Tomcat server. 
 
 In the case of i18n sample data, before restarting server, please check whether languages are includes in the runtime.properties:
```
RDFService.languageFilter = true
languages.selectableLocales = en_US, de_DE, sr_Latn_RS, ru_RU, fr_CA, en_CA, es, pt_BR, fr_CA_x_uqam
```
 
The sample data might be also ingested through VIVO user interface by following the instructions at 
https://wiki.lyrasis.org/display/VIVODOC115x/Sample+Data
  
