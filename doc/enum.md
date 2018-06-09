### **Enum** _(returned by Enum.YourName(...))_
#### **get**(_value_)
```
Colors.get(1) // EnumValue GREEN
HexaColors.get(0x00FF00) // EnumValue GREEN
CssColors.get("#00FF00") // EnumValue GREEN
```

#### **getAt**(_index_)
```
Colors.getAt(2) // EnumValue BLUE
HexaColors.getAt(2) // EnumValue BLUE
CssColors.getAt(2) // EnumValue BLUE
```

#### **hasIn**(_mask, ...[enumValues|names|values])
```
const value = 0xFFFF00
HexaColors.hasIn(value, Colors.RED, Colors.GREEN) // true
HexaColors.hasIn(value, Colors.RED, Colors.BLUE) // false

HexaColors.hasIn(value, "RED", "GREEN") // true
HexaColors.hasIn(value, 0xFF0000, 0x00FF00) // true

// You can even mix them
HexaColors.hasIn(value, 0x00FF00, "RED") // true
HexaColors.hasIn(value, Colors.GREEN, "RED") // true
```

#### **in**(_value_)
```
const value = 0xFFFF00
HexaColors.in(value) // [HexaColors.RED, HexaColors.GREEN]
```

#### **length**
```
HexaColors.length // 3
```

#### **name**
```
Colors.name // 'Colors'
HexaColors.name // 'HexaColors'
CssColors.name // 'CssColors'
```

#### **parse**(_string_)
```
Colors.parse("Colors.RED") // EnumValue RED
Colors.parse("HexaColors.RED") // null
Colors.parse("Not an enum value") // null
```
