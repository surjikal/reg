reg
===

Minimal sed-like tool for text replacements using JS regex syntax 

## Usage

```
reg <flags> <regex> <replacement>
```

This maps directly to Javascript's `String.replace` function:

```javascript
var regex = new RegExp(<regex>, <flags>);
str.replace(regex, <replacement>);
```

#### Examples

```bash
cat /etc/passwd | reg :.*

cat /etc/passwd | reg (.*?):.* "User: \$1"
```
