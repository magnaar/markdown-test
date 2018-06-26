[![NPM](https://nodei.co/npm/another-enum.png?mini=true)](https://www.npmjs.com/package/another-enum)
# Instanciate an Enum with a different numeric base
### _base: number 2-36_

## Why you should use the base parameter ?

if you do not specify the base, it will be displayed as base 10
> SimpleHexaColors.GREEN.toString() // => 'SimpleHexaColors.GREEN(65280)'

But if you specify it
> HexaColors.GREEN.toString() // => 'HexaColors.GREEN(16:00FF00)'

A bit more readable, right ?

See below to see how to use it.


## Hexadecimal
```
const HexaColors = Enum.HexaColors(16, {
    RED: 0xFF0000,
    GREEN: 0x00FF00,
    BLUE: 0x0000FF
})

const HexaColors2 = Enum.HexaColors2(16, {
    RED: 'FF0000',
    GREEN: '00FF00',
    BLUE: '0000FF'
})

// Hexa numbers will always be displayed in uppercase
HexaColors.GREEN.toString() // => 'HexaColors.GREEN(16:00FF00)'
HexaColors2.BLUE.toString() // => 'HexaColors2.BLUE(16:0000FF)'
```

## Octal
```
const OctalColors = Enum.HexaColors(8, {
    RED: 0o700,
    GREEN: 0o070,
    BLUE: 0o007
})

const OctalColors2 = Enum.HexaColors2(8, {
    RED: '700',
    GREEN: '070',
    BLUE: '007'
})

OctalColors.GREEN.toString() // => 'OctalColors.GREEN(8:070)'
OctalColors2.BLUE.toString() // => 'OctalColors2.BLUE(8:007)'
```

## Binary
```
const BinColors = Enum.BinColors(2, {
    RED: '100',
    GREEN: '010',
    BLUE: '001'
})

const BinColors2 = Enum.BinColors(2, {
    RED: 1,
    GREEN: 2,
    BLUE: 4
})
BinColors.GREEN.toString() // => 'BinColors.GREEN(2:010)'
BinColors2.BLUE.toString() // => 'BinColors2.BLUE(2:100)'
```

## Others
```
const Base20Colors = Enum.Colors(20, {
    RED: 'J00',
    GREEN: '0J0',
    BLUE: '00J'
})
Base20Colors.BLUE.toString() // => 'BinColors.BLUE(20:00J)'
```
