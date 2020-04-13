# MulleSDE

Are you developing in C, C++ or Objective C?

Do you hate being tied to your IDE vendor ?

Do you want to develop for MacOS, FreeBSD, Linux, Windows all with the same IDE ?

Are you using docker to keep project dependencies separate but you are looking for something better ?

Would you like your projects to build not only next year but also in the next decades ?

Then install [mulle-sde](//github.com/mulle-sde/mulle-sde) and give it a try!

## About 

MulleSDE is an IDE and dependency (package) manager for the commandline. There are no graphical components.
Amongst a few other things it

* provides a per-project environment
* fetches remote files and place them anywhere in your project tree
* fetches and builds dependencies (archives and git repositories) recursively and installs them locally to the project or at a chose place
* creates source files from templates
* transforms file-system structure into project files
* interfaces with various build systems
* parallelizes cmake project builds
* loads build instructions for third party dependencies from github 
* is scriptable and extensible


## Install

See [mulle-sde-developer](//github.com/mulle-sde/mulle-sde-developer) how
to install mulle-sde.


## Quick Start

If you want to compile some dependencies without setting up a mulle-sde project, 
you can do an *install* with an archive. Here is an example where the latest *mulle-allocator*
and its dependencies is installed into `/tmp/foo`:

```
mulle-sde install --prefix /tmp/foo https://github.com/mulle-c/mulle-allocator/archive/latest.tar.gz
```

If you don't want to use the mulle-sde project management features, but would like to 
keep the dependencies local to your project, you can use a `none` project type:

```
mulle-sde init none
mulle-sde dependency add --c --github mulle-c mulle-allocator
mulle-sde craft
```

This will create four folders:

```
.
├── dependency   # the desired output
├── kitchen      # temporary build folder
├── .mulle       # internal mulle-sde maintenance
└── stash        # download dependencies
```

## In action

<script id="asciicast-223917"
        src="https://asciinema.org/a/223917.js"
        async>
</script>


## Baby steps

These tools can be useful on their own. When familiarizing with them, you will get an idea what *mulle-sde* 
can do for you:

Tool                                                  | Description
------------------------------------------------------|-------------------------
[mulle-env](//github.com/mulle-sde/mulle-env)         | custom environments for projects
[mulle-fetch](//github.com/mulle-sde/mulle-fetch)     | grab and unpack repositories and archives
[mulle-make](//github.com/mulle-sde/mulle-make)       | detect build method and build a project
[mulle-match](//github.com/mulle-sde/mulle-match)     | categorize files and make files
[mulle-monitor](//github.com/mulle-sde/mulle-monitor) | monitor a filesystem folder and trigger commands on change

