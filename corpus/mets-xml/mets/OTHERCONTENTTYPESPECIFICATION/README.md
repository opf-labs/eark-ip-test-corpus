# mets/@OTHERCONTENTTYPESPECIFICATION

**ID:** mets-xml_mets_OTHERCONTENTTYPESPECIFICATION

**Rule:** If @CONTENTTYPESPECIFICATION = "OTHER" then @OTHERCONTENTTYPESPECIFICATION MUST exist and have a non-empty value (CSIP5).

**Reference:** CSIP5, CSIP Ch. [5.3.1. Use of the METS root element (element mets)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#531use-of-the-mets-root-element-element-mets)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** None

---

**Violation ID:** mets-xml_mets_OTHERCONTENTTYPESPECIFICATION_attribute_required_and_not_exist

**Violation description:**  @CONTENTTYPESPECIFICATION = "OTHER", but @OTHERCONTENTTYPESPECIFICATION attribute does not exist

**Error level:** `ERROR`

**Error message:** mets/@OTHERCONTENTTYPESPECIFICATION attribute does not exist. MUST be: if @CONTENTTYPESPECIFICATION = "OTHER" then @OTHERCONTENTTYPESPECIFICATION MUST exist and have a value that records the name of the content information type specification.

**Minimal test IP structure:** METS.xml file with mets/@CONTENTTYPESPECIFICATION = "OTHER", but no mets/@OTHERCONTENTTYPESPECIFICATION attribute

---

**Violation ID:** mets-xml_mets_OTHERCONTENTTYPESPECIFICATION_attribute_required_and_value_empty

**Violation description:** @OTHERCONTENTTYPESPECIFICATION attribute is required, but its value is emptry string

**Error level:** `ERROR`

**Error message:** mets/@OTHERCONTENTTYPESPECIFICATION attribute value is emptry string. MUST be: if @CONTENTTYPESPECIFICATION = "OTHER" then @OTHERCONTENTTYPESPECIFICATION MUST exist and have a value that records the name of the content information type specification.

**Minimal test IP structure:** METS.xml file with mets/@CONTENTTYPESPECIFICATION = "OTHER" and mets/@OTHERCONTENTTYPESPECIFICATION = "". Note that @CONTENTTYPESPECIFICATION and @OTHERCONTENTTYPESPECIFICATION are extensions of METS by CSIP, so proper namespace declarations must be present, e.g.:
```
<mets xmlns="http://www.loc.gov/METS/" 
    xmlns:csip="DILCIS"
    csip:CONTENTTYPESPECIFICATION="OTHER"
    csip:OTHERCONTENTTYPESPECIFICATION="" 
</mets>
```
---

**Violation ID:** mets-xml_mets_OTHERCONTENTTYPESPECIFICATION_attribute_not_required_and_exists

**Violation description:** @CONTENTTYPESPECIFICATION != "OTHER", so @OTHERCONTENTTYPESPECIFICATION attribute is not required, but exists

**Error level:** `INFO`

**Error message:** mets/@OTHERCONTENTTYPESPECIFICATION attribute exists, but is not required as the value of @CONTENTTYPESPECIFICATION is not "OTHER".

**Minimal test IP structure:** METS.xml file with @CONTENTTYPESPECIFICATION != "OTHER" and mets/@OTHERCONTENTTYPESPECIFICATION exists. Note that @CONTENTTYPESPECIFICATION and @OTHERCONTENTTYPESPECIFICATION are extensions of METS by CSIP, so proper namespace declarations must be present, e.g.:
```
<mets xmlns="http://www.loc.gov/METS/" 
    xmlns:csip="DILCIS"
    csip:CONTENTTYPESPECIFICATION="SIARD2"
    csip:OTHERCONTENTTYPESPECIFICATION="1"
</mets>
```