**another-enum** 1.0.0
=================
### _Another enum module, nothing more_

---
[![NPM](https://nodei.co/npm/another-enum.png)](https://www.npmjs.com/package/another-enum)

[![](https://img.shields.io/badge/version-1.0.0-blue.svg)]() [![](https://img.shields.io/badge/build-passing-brightgreen.svg)]() [![](https://img.shields.io/badge/tests-91%2F91-brightgreen.svg)]() [![](https://img.shields.io/badge/dependencies-none-brightgreen.svg)]()

---

## Usage
- [Import](#import)
- [Basic instanciation](#basic-instanciation)
- [Serializing](#serializing)

## Methods listing
- [Enum Constructors](doc/enum-constructors.md)
- [Enum Methods](doc/enum.md)
- [EnumValue Methods](doc/enum-value.md)

### **Import**
```
import { Enum } from 'another-enum'
const Enum = require('another-enum').Enum

const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')
```

### **Basic instanciation**
```
Enum.EnumName(NAME1, NAME2, ...)

Enum.EnumName({
   NAME1: value1,
   NAME2: value2,
   ...
})
```
See also: [Enum Constructors](doc/enum-constructors.md)

See also: [Instanciation with base](doc/base-instanciation.md)

#### _Examples_
```
const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')

const SimpleHexaColors = Enum.SimpleHexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})

// Should be avoided
// Because it will fail when trying to convert it in a number value
const CssColors = Enum.CssColors({
    RED: '#FF0000',
    GREEN: '#00FF00',
    BLUE: '#0000FF'
})
```
