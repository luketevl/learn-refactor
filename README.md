# learn-refactor
Learn refactor


# BEST PRACTICES
- **Small** functions
- **Private** functions
- **Separe** the **responsibilities**
  - _Creating_ **functions**
  - _Creating_ **Classes**
- **Readable names** to _classes_, _functions_, _variables_
- **Varibles** have one type value.

> Wrong

```javascript
const number = 1;
const number = number == 1 ;
```
> Correct

```javascript
const number = 1;
const check = number == 1;
```
- **Doesn't duplicate code**
  - _Creating_ **functions**
  - _Creating_ **Classes**
  - _Composition_
  - _Inheritance_
- **Doesn't boolean args**

> Wrong

```javascript
const calcTax = (value = 0, dollar = true) => (dollar) ? value * 3.23 : value * 2;
calcTax(10, false);
```
> Correct

```javascript
const calcTax = (value = 0, tax = 1) => value * tax;
const calcTaxDollar = value => calcTax(value, 3.23);
const calcTaxOther = value => calcTax(value, 2);
```
- **Doesn't use MAGIC NUMBERS**
  - Use **CONSTANTS**
  - Use **Enums**

> Wrong

```javascript
const size  = value => value * 9;
const size2 = value => value / 9;
```

> Correct

```javascript
const width = 9;
const size  = value => value * width;
const size2 = value => value / width;
```

# OBSERVATIONS
- All **code** should be _visible_ on your monitor
