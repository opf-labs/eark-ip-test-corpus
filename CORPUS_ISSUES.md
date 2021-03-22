Issues with Test Cases and Corpus Packages
==========================================

Classes of Issue
================
Categorising the issues helps by encouraging:
- use of criteria when assessing and issue; and
- consistency of approach when dealing with it.

Contradiction
-------------
These represent unresolvable issues where it is impossible to satisfy two or more
requirements in the specification due to contradictions in the text.

CSIP64 vs CSIPSTR13 <https://github.com/DILCISBoard/E-ARK-CSIP/issues/555>

Case Sensitivity
----------------
Causes more issues than it solves:
- for file systems it can cause issues unpacking an IP on a different file system.
Both HFS+ and Windows are unpredictable when dealing with matters of case. I'd suggest
that case clashes at the file system level simply generate a warning regarding
a potentially incompatible feature.

XML tag and attribute names are case-sensitive but between METS, the extension
schema and E-ARK choice of values/folder names it's all a little arcane. Some XML
and file system issues combine, e.g. <https://github.com/E-ARK-Software/py-rest-ip-validator/issues/27>

Inflexibility
-------------
Mandatory folder names are a barrier to entry for orgs that have established
practices, automated workflows and AIPs that use other folder names. The intention
is to make it easy to know where to find types of metadata and content. Despite
mandating the folder names an implementer is still forced to record the intention
for the folder through a USE attribute (see Redundancy). There is a performance
argument for avoiding XML parsing but there are ways to mitigate that concern.

Redundancy
----------
Repetition of names and labels that don't offer additional information about the
package structure and contents

CSIP 80 & 82 are identical <https://github.com/DILCISBoard/eark-ip-test-corpus/pull/291>
reported here: <https://github.com/DILCISBoard/E-ARK-CSIP/issues/648>

This Issue on the CSIP site list several instances <https://github.com/DILCISBoard/E-ARK-CSIP/issues/570>:
 - CSIP88 and CSIP90 both apply to the same node: `mets/structMap[@LABEL='CSIP']/div/div[@LABEL='Metadata']`
   <https://github.com/DILCISBoard/eark-ip-test-corpus/pull/301>
 - CSIP93 and CSIP95 both apply to the same nodeL `mets/structMap[@LABEL='CSIP']/div/div[@LABEL='Documentation']`
   In this case CSIP93 is `SHOULD` while CSIP95 is a more strident `MUST`
   <https://github.com/DILCISBoard/eark-ip-test-corpus/pull/308>
 - CSIP97 and CSIP99 both apply to the same node: `mets/structMap[@LABEL='CSIP']/div/div[@LABEL='Schemas']`
 - CSIP101 and CSIP103 both apply to the same nodeL `mets/structMap[@LABEL='CSIP']/div/div[@LABEL='Representations']`
   In this case CSIP101 is `SHOULD` while CSIP103 is a more strident `MUST`

Redundancy in use of the package name in `mets/@OBJID` CSIP1 and 'structMap/div@Label'
CSIP86 attribute:
 - <https://github.com/DILCISBoard/E-ARK-CSIP/issues/649>
 - <https://github.com/DILCISBoard/eark-ip-test-corpus/pull/297>

### Policy
- remove repeat requirements

Suggestions
-----------
- [CSIP91 and CSIP92 - what about SUPERSEEDED xml:IDs?](https://github.com/DILCISBoard/E-ARK-CSIP/issues/650)

Supporting Documentation
------------------------
Inconsistencies between formal specification text and examples, or between examples.
Policy: If resolution leaves the requirement unaltered, i.e. only the example is
fixed then these can be treated as matters of accuracy, i.e. a patch release.
