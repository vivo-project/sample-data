## Internationalization (i8n) sample data

The `i18n` directory contains the internationalized version of the [test data](../testdata/sample-data.n3) graph and is distributed by linguistic context according to the following files:
* `sample-data-i18n.ttl` is a TURTLE copy of [test data](../testdata/sample-data.n3).
* `sample-data-de_DE.ttl` contains the German - Germany (`de_DE`) labels for each resource contained in [test data](../testdata/sample-data.n3).
* `sample-data-en_CA.ttl` contains the English Canadian (`en_CA`) labels for each resource contained in [test data](../testdata/sample-data.n3).
* `sample-data-en_US.ttl` contains the U.S. English (`en_US`) labels of each resource contained in [test data](../testdata/sample-data.n3).
* `sample-data-fr_CA.ttl` contains the French Canadian (`fr_CA`) labels for each resource contained in [test data](../testdata/sample-data.n3).
* `sample-data-fr_FR.ttl` contains the French - France (`fr_FR`) labels for each resource contained in [test data](../testdata/sample-data.n3).
* `sample-data-sr_Latn_RS.ttl` contains the Serbian latin (`sr_RS`) labels for each resource contained in [test data](../testdata/sample-data.n3).

Once when these data are ingested into the graph, the runtime.properties should be configured as follows, and tomcat server should be restarted:
 ```
RDFService.languageFilter = true
languages.selectableLocales = en_US, de_DE, sr_Latn_RS, ru_RU, fr_CA, en_CA, es, pt_BR, fr_CA_x_uqam
```


 