These ontologies are an extraction and adaptation for internationalization of 
https://github.com/vivo-project/sample-data/blob/main/sample-data.n3.

Although they are of general use, the knowledge graphs and ontologies contained 
in this directory are specifically designed to be used with the regression tests
of https://github.com/vivo-community/vivo-regression-tests.

The files are divided into two series: *-orig.ttl and *-i18n*.ttl and they 
correspond respectively to a use in a first instance of VIVO 1.11 not 
including internationalization and the VIVO 1.12 version 
including internationalization (i18n)

Data sheet of the files:
- Semantics
    The semantics of the two file categories are the same. For example the 
    identification to the resource 'sample-data:n2022' refers to the concept of
    "Keynote Speaker" in both ontology categories.

- Base URI, sample-data prefix, individual base uri
    Each ontology category has its own URI sets
    
    - ORIG Category
        - base URI: http://localhost:8080/vivo_orig/sample-data-orig#
        - prefix sample-data http://localhost:8080/vivo_orig/individual/
        - Definition of the individual to be declared in the runtime.properties
          file of the VIVO instance: 
          Vitro.defaultNamespace = http://localhost:8080/vivo_orig/individual/
        - Internationalization 
          Only the en_US is available in this category

    - I18N Category
        - base URI: http://localhost:8080/vivo_i18n/sample-data-i18n#
        - prefix sample-data http://localhost:8080/vivo_i18n/individual/
        - Definition of the individual to be declared in the runtime.properties
          file of the VIVO instance: 
          Vitro.defaultNamespace = http://localhost:8080/vivo_i18n/individual/
        - for each language a graph containing the linguistic context of each 
          language in extension of the filename is available . For example, 
          for fr_CA, the graph sample-data-i18n-fr_CA.ttl contains the 
          Canadian-French translation of sample-data

Sample Data Language Enhancement
        To introduce a new linguistic context to the sample-data, perform the 
        following steps:
        
            1- Choose the graph of an original language (e.g. en_US) and rename
               it to the target language context (e.g. fr-BE). This gives for 
               example sample-data-i18n-fr_BE.ttl
            2- in the graph, replace the linguistic tag of the source language 
               (ex.: "@en-US") by the linguistic tag of the target 
               language (ex.: "@fr-BE")
            3- Translate the rdfs:label content of each resource to the new 
               liguistic context (e.g.: 
                    sample-data:n1467 rdfs:label "Professor"@en-US . 
                    by 
                    sample-data:n1467 rdfs:label " Professeur"@en-BE ;
                )
-- End of text --