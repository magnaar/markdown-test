[![NPM](https://nodei.co/npm/another-enum.png?mini=true)](https://www.npmjs.com/package/another-enum)
### **EnumValue**
#### **index**
```
Colors.RED.index // 0
HexaColors.RED.index // 0
CssColors.RED.index // 0
```

#### **isIn**(_mask_)
```
const value = 0xFFFF00
HexaColors.RED.isIn(value) // true
HexaColors.GREEN.isIn(value) // true
HexaColors.BLUE.isIn(value) // false
```

#### **longName**
```
Colors.RED.longName // 'Colors.RED'
HexaColors.RED.longName // 'HexaColors.RED'
CssColors.RED.longName // 'CssColors.RED'
```

#### **name**
```
Colors.RED.name // 'RED'
HexaColors.RED.name // 'RED'
CssColors.RED.name // 'RED'
```

#### **stringValue**
```
Colors.RED.stringValue // '0'
HexaColors.RED.stringValue // 'FF0000'
CssColors.RED.stringValue // '#FF0000'
BinColors.RED.stringValue // '100'
```

#### **value**
```
Colors.RED.value // 0
HexaColors.RED.value // 16711680
CssColors.RED.value // '#FF0000'
BinColors.RED.value // 4
```
