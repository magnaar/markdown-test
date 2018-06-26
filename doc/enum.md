[![NPM](https://nodei.co/npm/another-enum.png?mini=true)](https://www.npmjs.com/package/another-enum)
### **Enum** _(returned by Enum.YourName(...))_
#### **get**(_value_)
> Return the EnumValue for the given value
```
// With this instanciation, value and index are the same
const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')
Colors.get(1) // => Colors.GREEN

// With this instanciation, value and index are different
const HexaColors = Enum.HexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})
HexaColors.get(0x00FF00) // => HexaColors.GREEN
```

#### **getAt**(_index_)
> Return value for the given index (declaration order)
```
// With this instanciation, value and index are the same
const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')
Colors.getAt(1) // => Colors.GREEN

// With this instanciation, value and index are different
const HexaColors = Enum.HexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})
HexaColors.getAt(1) // => Colors.GREEN
```

#### **hasIn**(_mask, ...EnumValues|names|values_)
> Indicates if the mask contains AL the given values
```
const HexaColors = Enum.HexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})
const mask = 0xFFFF00
HexaColors.hasIn(mask, Colors.RED, Colors.GREEN) // => true
HexaColors.hasIn(mask, Colors.RED, Colors.BLUE) // => false, mask doesn't contain BLUE

HexaColors.hasIn(mask, 'RED', 'GREEN') // => true
HexaColors.hasIn(mask, 0xFF0000, 0x00FF00) // => true

// You can even mix them
HexaColors.hasIn(mask, 0x00FF00, 'RED') // => true
HexaColors.hasIn(mask, Colors.GREEN, 'RED') // => true
```

#### **in**(_value_)
> Returns an array of all the EnumValues contained in the given mask
```
const HexaColors = Enum.HexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})
const mask = 0xFFFF00
HexaColors.in(mask) // => [HexaColors.RED, HexaColors.GREEN]
```

#### **length**
> Returns the number of EnumValues in the enum
```
const Colors = Enum.Colors('RED', 'GREEN', 'BLUE')
Colors.length // => 3
```

#### **name**
> Return the Enum's name
```
let anotherEnum = Enum.Colors('RED', 'GREEN', 'BLUE')
anotherEnum.name // => 'Colors'

anotherEnum = Enum.HexaColors({
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})
anotherEnum.name // => 'HexaColors'
```

#### **parse**(_string_)
> Return an EnumValue for the given name
```
Colors.parse('Colors.RED') // EnumValue RED
Colors.parse('HexaColors.RED') // null
Colors.parse('Not an enum value') // null
```

#### **toString(_number|EnumValue_)
```
HexaColors.toString() // Colors(RED|GREEN|BLUE)
HexaColors.toString(0x00FF00) // Colors.GREEN(16:00FF00)
HexaColors.toString(0xFF00FF) // Colors.[RED|BLUE](16:FF00FF)
```
