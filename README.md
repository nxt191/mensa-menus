# mensa-menus

This script fetches and displays menus for ETH mensas and the Mercato UZH mensa.

![example image](example.png)

## Installation

This script works on OSX and (probably) all Linux distros. 

It requires python3 to be installed.

Simply download the file and drop it in a folder in your `$PATH`

For example you can run

```
curl 'https://raw.githubusercontent.com/nxt191/mensa-menus/master/menus' > menus

chmod +x menus

mv menus /usr/local/bin

``` 



## Usage

Type `menus` to get a list of all default locations.

Type `menus location` (substitute 'location' by a valid location) to get a list of all current menus and their price.

Default locations are `zentrum`, `hoengg` and names of most mensas.

Type `menus location --all` to get all menus, even the blocked ones.

It will show the Dinner Menus after 14:00 (your system time) and next day's lunch after 21:00.

## Fuzzy matching

Thanks to RobinJadoul, you can also use abbreviations and it tries to find a matching group:

Use for example `menus z` for zentrum, `menus ps` for polysnack

## Known bugs

There are still some bugs for certain edge cases around weekend times. Will (might) be fixed in the next few days...


## Customization

Open the file `menus` in your favourite text editor.

Change the value of `lang` to `'en'` or `'de'`to set the language of the menus. (Line 9) (Thanks to RobinJadoul)

Change the value of `prices` to `'student'`, `'staff'` or `'extern'` to get the prices desired. (Line 13)

Add or remove menu names from `blocked_menus` to hide menus you're not interested in. By default, most vegi menus are blocked, because yuck vegies... (Line 17)

Modify the default locations by changing the `locations`. See Line 14 etc. for ids. (Line 38)





