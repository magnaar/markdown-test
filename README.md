**another-enum** 1.0.0
=================
### _Another enum module, nothing more_

---
[![NPM](https://nodei.co/npm/another-enum.png)](https://nodei.co/npm/another-enum/)

[![](https://img.shields.io/badge/version-1.0.0-blue.svg)]() [![](https://img.shields.io/badge/build-passing-brightgreen.svg)]() [![](https://img.shields.io/badge/tests-76%2F76-brightgreen.svg)]() [![](https://img.shields.io/badge/dependencies-none-brightgreen.svg)]()

---

## Usage
- [Import](#import)
- [Basic instanciation](#basic-instanciation)

## Methods listing
- [Methods Enum](doc/enum.md)
- [Methods EnumValue](doc/enum-value.md)

### Import
```
import { Enum } from 'another-enum'
const Enum = require('another-enum').Enum

const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')
```

### Basic instanciation
```
Enum.EnumName([base|class], NAME1, NAME2, ...)
Enum.EnumName({base:..., class:...}, NAME1, NAME2, ...)

Enum.EnumName([base|class], {
   NAME1: value1,
   NAME2: value2,
   ...
})

Enum.EnumName([base|class], {
   NAME1: {
       [value: value1],
       class: Name1Class
   },
   NAME2: {
       [value: value2],
       class: Name2Class
   },
   ...
})
```
