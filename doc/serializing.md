[![NPM](https://nodei.co/npm/another-enum.png?mini=true)](https://www.npmjs.com/package/another-enum)
### **Serializing**

### ** /!\ Be careful /!\ **
Serializing and deserializing a whole Enum with a custom class won't work.
Especially the deserializing part, since it's not supported.

#### **Simple value**
```
JSON.stringify(Colors.RED) // => '"Colors.RED"'
```
#### **A whole enum**
```
const Colors = Enum.Colors("RED", "GREEN", "BLUE")
JSON.stringify(Colors)
// => '{"Colors":{"values":["RED","GREEN","BLUE"]}}'

const DecColors = Enum.DecColors(10, {"RED":0xFF0000, "GREEN":0x00FF00, "BLUE":0x0000FF})
JSON.stringify(DecColors)
// => '{"DecColors":{"base":10,"values":{"RED":"16711680","GREEN":"65280","BLUE":"255"}}}'

const HexaColors = Enum.HexaColors(16, {"RED":0xFF0000, "GREEN":0x00FF00, "BLUE":0x0000FF})
JSON.stringify(HexaColors)
// => '{"HexaColors":{"base":16,"values":{"RED":"FF0000","GREEN":"00FF00","BLUE":"0000FF"}}}'

const BinColors = Enum.BinColors(2, {"RED":"100", "GREEN":"010", "BLUE":"001"})
JSON.stringify(BinColors)
// => '{"BinColors":{"base":2,"values":{"RED":"100","GREEN":"010","BLUE":"001"}}}'

const CssColors = Enum.CssColors({RED: '#FF0000', GREEN: '#00FF00', BLUE: '#0000FF'})
JSON.stringify(CssColors)
// => '{"CssColors":{"values":{"RED":"#FF0000","GREEN":"#00FF00","BLUE":"#0000FF"}}}'
```

### **Deserialize**
#### **Simple value**
```
const serialized = '"Colors.RED"' // Or 'Colors.RED'
// Obviously Colors has to be defined first
const RED = Colors.parse(serialized) // => EnumValue RED
```

#### **A whole Enum**
```
// This or any string in the serialize section
const serialized = '{"HexaColors":{"base":16,"values":{"RED":"FF0000","GREEN":"00FF00","BLUE":"0000FF"}}}'
const HexaColors = Enum.parse(serialized) // => Enum HexaColors { "RED": {}, "GREEN": {}, "BLUE": {} }
```
