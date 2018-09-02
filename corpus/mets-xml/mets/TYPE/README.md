# mets/@TYPE

**ID:** mets-xml_mets_TYPE

**Rule:**
 * @TYPE MUST be present (CSIP3).
 * @TYPE MUST have a non-empty value (CSIP3).

**Reference:** CSIP3, CSIP Ch. [5.3.1. Use of the METS root element (element mets)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#531use-of-the-mets-root-element-element-mets)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** None

---

**Violation ID:** mets-xml_mets_TYPE_attribute_not_exist

**Violation description:** @TYPE attribute does not exist

**Error level:** `ERROR`

**Error message:** mets/@TYPE attribute does not exist. MUST be: attribute exists and has a value that identifies the type of the package (genre).

**Minimal test IP structure:** METS.xml file with no mets/@TYPE attribute

---

**Violation ID:** mets-xml_mets_TYPE_attribute_value_empty

**Violation description:** @TYPE attribute value is emptry string

**Error level:** `ERROR`

**Error message:** mets/@TYPE attribute value is emptry string. MUST be: attribute exists and has a value that identifies the type of the package (genre).

**Minimal test IP structure:** METS.xml file with mets/@TYPE = ""
