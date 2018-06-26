[![NPM](https://nodei.co/npm/another-enum.png?mini=true)](https://www.npmjs.com/package/another-enum)
# **Enum Constructors**
## **Parameters**

Enum._**[EnumName](#enumname:)**_([[EnumParameters](#enumparameters:)], **[EnumValues](#enumvalues:)**)


### **EnumName:**
    Name of your enum

### **EnumParameters:**
#### Base: Number (2-36)
##### default: 10

    The EnumValue base number.
    This parameter will be use to display EnumValue values, in a more readable way.

#### Class: EnumValue subclass
##### default: EnumValue

    This allow to override EnumValue behavior or add new properties and methods on your EnumValues.

#### All: Object
```
{
    base: Number (2-36)
    class: EnumValue subclass
}
```
See above:
- **[Base](#base:-number-(2-36))**
- **[Class](#class:-enumvalue-subclass)**



### **EnumValues:**
#### Values names: Strings parameters list
```
    'NAME1', 'NAME2', ...
```
**NAMEx**: valid identifier _(otherwise you won't be able to access it with '.' notation)_

#### NameValue Object litteral
```
    {
        NAME: value,
        ...
    }
```
- **NAME**: valid identifier _(otherwise you won't be able to access it with '.' notation)_
- **value**: Number|String Number (or Anything else, but not recommended),

#### EnumValue config Objet
    {
        NAME: {
            [value: Number|String (or Anything, but not recommended)],
            class: EnumValue subclass
        },
        ...
    }
- **NAME**: valid identifier _(otherwise you won't be able to access it with '.' notation)_
- **value**: Number|String Number (or Anything else, but not recommended),
- **class**: a subclass of the class passed as EnumParameter, if none passed, an EnumValue subclass
