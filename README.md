# specs - A string formatting utility modeled off VM/CMS Pipeline's specs stage

## What's currently working

* Basic parsing of specs parameters
  * inputspec *STRIP *CONVERSION outputspec *PLACEMENT
* input specifications:
  * delimited string literals.  e.g. /abc def/ -or- ,xyzzy plugh, 
  * numerical ranges
    * mm-nn  mm-*
    * mm.len mm.*
    * nn
  * word ranges (WORD can be abbreviated)
    * WORDm-n WORDm-*   
    * WORDn

* output specifications:
  * '.' - skip output
  * numerical position
    * mm-nn mm-*
    * mm.len mm.*
    * mm
  * NEXT
    * NEXT.len NEXT.*
  * NEXTWORD
    * NEXTWORD.len
 
### Example

```
      specs '1-8 1 /some string/ nw 9-* nw'
      input:  123456789abcd
      output: 12345678 some string  9abcd
```

## TODOs

The long term goal is to implement as many features as practical
from the VM/CMS's specs stage.

There are a lot of missing features and partially implemented features.

There are stubs for: 

* *STRIP
* *CONVERSION
* *PLACEMENT
* Fields
