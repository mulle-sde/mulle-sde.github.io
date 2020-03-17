# MulleSDE

MulleSDE is an IDE and package (dependenc) manager for the commandline. There are no graphical components.
Amongst a few other things it

* provides a per-project environment
* fetches remote files and place them anywhere in your project tree
* fetches and builds dependencies (archives and git repositories) recursively and installs them locally to the project
* creates source files from templates
* transforms file-system structure into project files
* interfaces with various build systems
* parallelizes cmake project builds
* loads build instructions for third party dependencies from github 
* its scriptable and extensible

<script id="asciicast-223917"
        src="https://asciinema.org/a/223917.js"
        async>
</script>


## Should you be interested in MulleSDE ?

Are you developing in C, C++ or Objective C?

Do you hate being tied to your IDE vendor ?

Do you want to develop for MacOS, FreeBSD, Linux, Windows all with the same IDE ?

Are you using docker to keep project dependencies separate but you are looking for something better ?

Would you like your projects to build not only next year but also in the next decades ?

Then install [mulle-sde](//github.com/mulle-sde/mulle-sde) and give it a try!


## The snags

The whole thing is not badly documented. There is even a [Wiki](https://github.com/mulle-sde/mulle-sde/wiki) with
quite a bit of content. But there are snags.

There isn't a proper usage for every command yet. Some of the usages are not complete. If you can read bash source, it's very helpful.
There are some limitations with respect to platform differentiation via `${MULLE_UNAME}`. E.g. "arch linux" vs "debian linux".
It's completely different to anything you have used yet.


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

