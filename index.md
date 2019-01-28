# MulleSDE

The IDE for the command-line.

* fetches remote files and place them anywhere in your project tree
* interfaces with various build systems
* parallelizes C project builds
* provides a per-project build environment
* does recursive dependency management
* transforms file-system structure into project files


<script id="asciicast-223917"
        src="https://asciinema.org/a/223917.js"
        async>
</script>


## Should you be interested in MulleSDE ?

Are you developing in C, C++ or Objective ? Then MAYBE.

Are you tied to a single platform and do you always develop in the same
language and development environment (aka IDE) ? Then NO.

Otherwise install [mulle-sde](//github.com/mulle-sde/mulle-sde) and try the
following commands:

```bash
mulle-sde init -d foo -m mulle-sde/c-developer none
mulle-sde foo
dependency add --github mulle-core mulle-sprintf
craft
ls -R dependency
```

If you think "So what ?", then the answer is NO.


## Should you use it ?

* if you want to develop using mulle-objc: YES
* if you want to use it just to grab and build some dependencies (project type *none*): MAYBE
* if you have time and energy to look into bash sources, to look for hidden options and to see why usages are out of date: GO FOR IT
* if you just use the stable tools (see below): YES
* if you generally need a lot of help to get your things together:NO

Otherwise the whole thing is not badly documented, but there are snags.

1. The project is still fairly unstable. I seem to keep rewriting stuff. Some areas are stable, but some areas aren't.
2. There isn't a proper usage for every command yet. Some of the usages are already outdated.
3. There are some limitations with respect to platform differentiation via `${MULLE_UNAME}`. E.g. arch linux vs debian linux.
4. The version checking like "fetch me the latest foo with version < 2" isn't implemented, but probably will be.

On a day to day basis, MulleSDE though is a joy to use and my favorite IDE, because it saves me so much time.


## Presumed to be stable

These tools look like they are complete and useful on their own

Tool                                                  | Description
------------------------------------------------------|-------------------------
[mulle-env](//github.com/mulle-sde/mulle-env)         | custom environments for projects
[mulle-fetch](//github.com/mulle-sde/mulle-fetch)     | grab and unpack repositories and archives
[mulle-make](//github.com/mulle-sde/mulle-make)       | detect build method and build a project
[mulle-match](//github.com/mulle-sde/mulle-match)     | categorize files and make files
[mulle-monitor](//github.com/mulle-sde/mulle-monitor) | monitor a filesystem folder and trigger commands on change

