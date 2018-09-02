# mets/@OBJID

**ID:** mets-xml_mets_OBJID

**Rule:**
 * @OBJID MUST be present (CSIP2).
 * @OBJID MUST have a non-empty value (CSIP2).
 * @OBJID MUST have a value that starts with a prefix, followed by the actual value of the identifier (CSIP Ch. 5.2).

**Reference:** CSIP2, CSIP Ch. [5.2 The use of identifiers](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#the-use-of-identifiers) and [5.3.1. Use of the METS root element (element mets)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#531use-of-the-mets-root-element-element-mets)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** None

---

**Violation ID:** mets-xml_mets_OBJID_attribute_not_exist

**Violation description:** @OBJID attribute does not exist

**Error level:** `ERROR`

**Error message:** mets/@OBJID attribute does not exist. MUST be: attribute exists and has a value that starts with a letter or underscore that form a part of prefix, followed by the actual value of the identifier.

**Minimal test IP structure:** METS.xml file with no mets/@OBJID attribute

---

**Violation ID:** mets-xml_mets_OBJID_attribute_value_empty

**Violation description:** @OBJID attribute value is emptry string

**Error level:** `ERROR`

**Error message:** mets/@OBJID attribute value is emptry string. MUST be: a value that starts with a letter or underscore that form a part of prefix, followed by the actual value of the identifier.

**Minimal test IP structure:** METS.xml file with mets/@OBJID = ""

---

**Violation ID:** mets-xml_mets_OBJID_attribute_value_numeric

**Violation description:** @OBJID attribute value is numeric

**Error level:** `ERROR`

**Error message:** mets/@OBJID attribute value is numeric. MUST be: a value that starts with a letter or underscore that form a part of prefix, followed by the actual value of the identifier.

**Minimal test IP structure:** METS.xml file with mets/@OBJID = "1"

---

**Violation ID:** mets-xml_mets_OBJID_attribute_value_too_short

**Violation description:** @OBJID attribute value is too short

**Error level:** `ERROR`

**Error message:** mets/@OBJID attribute value is too short. MUST be: a value that starts with a letter or underscore that form a part of prefix, followed by the actual value of the identifier. The theoretical minimum is 2 characters: a prefix and an identifier, e.g. "a1"

**Minimal test IP structure:** METS.xml file with mets/@OBJID = "a"

