---
title: Errors and how to fix them
date: 2019-05-09T12:30:14.456Z
updated: 2019-05-09T12:30:14.560Z
toc: true
category:
  - 'CD:RE SDK'
  - Misc
---
While making mods for Crashday you may encounter a lot of different crashes and bugs. Problem is, the error messages were meant for developers so they don't usually give enough info about how you would fix the given bug. But usually it is possible to pinpoint the problematic file and fix the error. For this purpose here is the list of well-known errors and their possible causes.

If you found any error which is not on that list, please report it to the modding channel in Crashday Discord.

# Assertion failed

Generally these errors appear when the game got a value it did not expect to. If the game expects a mass as integer on line 3 in some file but finds a `great meme` this error will appear. Even then, we still can differ between different assertion fails.

## IsValueSetInString

Exact message:

```
Assertion failed!
IsValueSetInString((*tuning)[j].DetailString, "name")

(file ..\code\game\carobj\carspecs.cpp, line 111)
```

Problematic file: `.tun files`.

Possible causes: 

1. Wrongly specified amount of tuning items at the top.
2. Line 3 should be empty.

## size<BM_BYTESPERBLOCK

Exact message:

```
Assertion failed!
size<BM_BYTESPERBLOCK

(file ..\code\game\propcore\tools\memblock.cpp, line 52)
```

Problematic file: `unknown`

Possible causes: 

1. This error appears when the game tries to load a file bigger than it can handle. Usually none of the text files should exceed this limit so the most possible reason is too big .p3d file.
2. If it's a .p3d model chances are you have to many polygons. Reduce to 58k.

## wheelwidth > 0

Exact message:

```
Assertion failed!
wheelwidth > 0

(file ..\code\game\carspecial\skidmark.cpp, line 39)
```

Problematic file: `.p3d model of the wheel`

Possible causes: 

1. No "main" mesh found in the model.

## mass > 0

Exact message:

```
Assertion failed!
mass > 0

(file ..\code\game\dynobj\dynobj.cpp, line 529)
```

Problematic file: `unknown`

Possible causes: 

1. Faulty mesh?
2. Some dynamic or a car has a zero mass.

> you're assuming errors make sense
>
> \
>
>
> that's a rookie mistake
>
> \
>
>
> @Mica

# Others

## invalid NumPlate-value

Exact message:

```
The car file contains an invalid NumPlate-value!
Possible is 'wide', 'narrow' or 'us'
file = filename

(this message was produced in:
..\code\game\carobj\carspecs.cpp, line 274)
```

Problematic file: `carinfo.cca`. In the error message `file =` parameter should show what car caused the crash.

Possible causes:

1. You defined a non existent license plate e.g. `narow` (one r is missing).
2. The engine expected another value at this line position. This probably means you missed some value, added one extra. Possibly incorrect number of damage textures is present.

## Expected physics section but found

Exact message:

```
Expected physics section but found
file = *filename*
(this message was produced in:
..\code\game\carobj\carspecs.cpp, line 390)
```

Problematic file: `carinfo.cca`. In the error message `file =` parameter should show what car caused the crash.

Possible causes:

1. Number of gear rations is not equal to the amount of gears actually present in the config file (should be number of gears + 1 for rear).
2. The engine expected another value at this line position. This probably means you missed some value, added one extra.

## Unsupported type for shop article!

Exact message:

```
Unsupported type for shop article!

TempName = *partname*
(this message was produced in:
..\code\game\user\shop.cpp, line 645)
```

Problematic file: `shop.lst`.

Possible causes:

1. Part group specified incorrectly. Check .cdo file definition for possible variants.
2. The engine expected another value at this line position. This probably means you missed some value or added one extra.
