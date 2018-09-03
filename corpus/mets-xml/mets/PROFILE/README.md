# mets/@PROFILE

**ID:** mets-xml_mets_PROFILE

**Rule:**
 * @PROFILE MUST be present (CSIP6).
 * @PROFILE MUST have a non-empty value (CSIP6).
 * @PROFILE MUST have a value that is a URL of the used profile (CSIP6).

**Reference:** CSIP6, CSIP Ch. [5.3.1. Use of the METS root element (element mets)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/master/implementation/index.md#531use-of-the-mets-root-element-element-mets)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** None

**Comments:** This test case assumes that the validator can check if the attribute value is a standard-conformant URL, so only one URL violation is needed. Without a proper URL validator there would be workaround validation rules (e.g. the value begins with "http://", minimum length of the value etc.), which would require specific violations.

---

**Violation ID:** mets-xml_mets_PROFILE_attribute_not_exist

**Violation description:** @PROFILE attribute does not exist

**Error level:** `ERROR`

**Error message:** mets/@PROFILE attribute does not exist. MUST be: attribute exists and has a value that is a URL of the used profile.

**Minimal test IP structure:** METS.xml file with no mets/@PROFILE attribute

---

**Violation ID:** mets-xml_mets_PROFILE_attribute_value_empty

**Violation description:** @PROFILE attribute value is emptry string

**Error level:** `ERROR`

**Error message:** mets/@PROFILE attribute value is emptry string. MUST be: attribute exists and has a value that is a URL of the used profile.

**Minimal test IP structure:** METS.xml file with mets/@PROFILE = ""

---

**Violation ID:** mets-xml_mets_PROFILE_attribute_value_not_url

**Violation description:** @PROFILE attribute value is not a URL

**Error level:** `ERROR`

**Error message:** mets/@PROFILE attribute value is not a URL. MUST be: attribute exists and has a value that is a URL of the used profile.

**Minimal test IP structure:** METS.xml file with mets/@PROFILE = "1"