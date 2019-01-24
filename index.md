# MulleSDE

The IDE for the commandline.

Should you use it.

* if you want to develop using mulle-objc, I'd say yes
* if you want to use it just to grab and build some dependencies (project type *none*), I'd say yes
* if you have time and energy to look into bash sources, to look for hidden options and to see why usages are out of date, I'd say yes

Otherwise the whole thing is not badly documented, but there are snags.

1. The project is still fairly unstable. I seem to keep rewriting stuff. Some areas are stable, but some areas aren't.
2. There are more options for each command, than I want to put into the usage. You have to look into the source to get the full power of the commands available.
3. There isn't a proper usage for every command yet. Some of the usages are already outdated.
4. There are some obvious limitations with respect to platform differentiation via `${MULLE_UNAME}`. E.g. arch linux vs debian linux
5. The version checking like "fetch me the latest foo with version < 2" isn't implemented, but probably will be.

On a day to day basis, MulleSDE though is a joy to use and my favorite IDE, because it saves me so much time.
