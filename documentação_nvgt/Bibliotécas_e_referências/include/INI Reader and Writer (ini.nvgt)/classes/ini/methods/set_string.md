# set_string
Set a string in the INI data given a section name, a key and a value.

`bool ini::set_string(string section, string key, string value);`

## Arguments:
* string section: the section to put this key/value pair in (leave blank to add at the top of the file without a section).
* string key: the name of the key.
* string value: the value to set.

## Returns:
bool: true if the string was successfully written, false otherwise.

## Remarks:
All of the other setters use this format. If the key exists already, the value, of course, will be updated.
