# fileSec/fileGrp	

**ID:** mets-xml_fileSec_fileGrp

**Rule:**
 * FileSec element MUST include at least one fileGrp element(CSIP57).


**Reference:** CSIP57, CSIP Ch. [5.3.5. Use of the METS file section (element fileSec)](https://github.com/DILCISBoard/E-ARK-CSIP/blob/6e5a08c9619840b4c768c8016ce55e47cf977d02/implementation/index.md#535use-of-the-mets-file-section-element-filesec)

**Referenced CSIP version:** [6e5a08c](https://github.com/DILCISBoard/E-ARK-CSIP/tree/6e5a08c9619840b4c768c8016ce55e47cf977d02), 2018-08-19

**Dependencies:** mets-xml_fileSec

---

**Violation ID:** mets-xml_fileGrp_element_not_exsist

**Violation description:** fileGrp element does not exist

**Error level:** `ERROR`

**Error message:** FileGrp element does not exist. MUST be:MUST be: The file section of both the root and representation METS files includes at least one file group (element fileGrp).

**Minimal test IP structure:** METS.xml file with fileSec element and without fileGrp element

---

