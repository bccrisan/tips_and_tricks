# chmod cheatsheet

## Lengend
- d = Directory
- r = Read
- w = Write
- x = Execute

|Number|DRWX|Binary|
|-|---|---|
|7|rwx|111|
|6|rw-|110|
|5|r-x|101|
|4|r--|100|
|3|-wx|011|
|2|-w-|010|
|1|--x|001|
|0|---|000|

## Command:

```Python
chmod 777 file
```

### Brakedown

|command|Owner|Group|Others|File|
|-|-|-|-|-|
|chmod|7|7|7| test_file|
