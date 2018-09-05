# mets/@CONTENTTYPESPECIFICATION

**ID:** mets-xml_mets_CONTENTTYPESPECIFICATION

**Rule:**
 * @CONTENTTYPESPECIFICATION MUST be present (CSIP4).
 * @CONTENTTYPESPECIFICATION MUST have a value from a fixed vocabulary of `[ SMURFERMS | SMURFSFSB | SIARD1 | SIARD2 | SIARDDK | GeoVectorGML | GeoRasterGeotiff | MIXED | OTHER ]` (CSIP4).

**Reference:** CSIP4, CSIP Ch. [5.3.1. Use of the METS root element (element mets)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#531use-of-the-mets-root-element-element-mets)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** None

---

**Violation ID:** mets-xml_mets_CONTENTTYPESPECIFICATION_attribute_not_exist

**Violation description:** @CONTENTTYPESPECIFICATION attribute does not exist

**Error level:** `ERROR`

**Error message:** mets/@CONTENTTYPESPECIFICATION attribute does not exist. MUST be: attribute exists and has a value from the fixed vocabulary of [ SMURFERMS | SMURFSFSB | SIARD1 | SIARD2 | SIARDDK | GeoVectorGML | GeoRasterGeotiff | MIXED | OTHER ].

**Minimal test IP structure:** METS.xml file with no mets/@CONTENTTYPESPECIFICATION attribute

---

**Violation ID:** mets-xml_mets_CONTENTTYPESPECIFICATION_attribute_value_empty

**Violation description:** @CONTENTTYPESPECIFICATION attribute value is emptry string

**Error level:** `ERROR`

**Error message:** mets/@CONTENTTYPESPECIFICATION attribute value is emptry string. MUST be: a value from the fixed vocabulary of [ SMURFERMS | SMURFSFSB | SIARD1 | SIARD2 | SIARDDK | GeoVectorGML | GeoRasterGeotiff | MIXED | OTHER ].

**Minimal test IP structure:** METS.xml file with mets/@CONTENTTYPESPECIFICATION = "". Note that @CONTENTTYPESPECIFICATION is an extension of METS by CSIP, so proper namespace declarations must be present, e.g.:
```
<mets xmlns="http://www.loc.gov/METS/" 
    xmlns:csip="DILCIS"
    csip:CONTENTTYPESPECIFICATION="" 
</mets>
```
---

**Violation ID:** mets-xml_mets_CONTENTTYPESPECIFICATION_attribute_value_not_in_vocabulary

**Violation description:** @CONTENTTYPESPECIFICATION attribute value does not match any of the allowed values in the vocabulary

**Error level:** `ERROR`

**Error message:** mets/@CONTENTTYPESPECIFICATION attribute value does not match any of the allowed values in the vocabulary. MUST be: a value from the fixed vocabulary of [ SMURFERMS | SMURFSFSB | SIARD1 | SIARD2 | SIARDDK | GeoVectorGML | GeoRasterGeotiff | MIXED | OTHER ].

**Minimal test IP structure:** METS.xml file with mets/@CONTENTTYPESPECIFICATION = "1". Note that @CONTENTTYPESPECIFICATION is an extension of METS by CSIP, so proper namespace declarations must be present, e.g.:
```
<mets xmlns="http://www.loc.gov/METS/" 
    xmlns:csip="DILCIS"
    csip:CONTENTTYPESPECIFICATION="1" 
</mets>
```