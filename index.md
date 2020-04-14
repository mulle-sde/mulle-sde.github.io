```
mulle-sde install --prefix /tmp/foo https://github.com/mulle-c/mulle-buffer/archive/latest.tar.gz
```

If you don't want to use the mulle-sde project management features, but would like to 
keep the dependencies local to your project, you can use a `none` project type:

```
mulle-sde init none
mulle-sde dependency add --c --github mulle-c mulle-buffer
mulle-sde craft
mulle-sde linkorder
```

This will create four folders with the compiled results:

```
.
├── dependency   # the desired output
├── kitchen      # temporary build folder
├── .mulle       # internal mulle-sde maintenance
└── stash        # download dependencies
```

and it will give you the link options for your platform in the correct order:

```
-L./dependency/lib
-lmulle-buffer
-lmulle-allocator
```

## In action

<script id="asciicast-223917"
        src="https://asciinema.org/a/223917.js"
        async>
</script>


## Baby steps

These tools can be useful on their own. When you get familiar with them, you will get an idea what *mulle-sde* 
can do for you:

Tool                                                  | Description
------------------------------------------------------|-------------------------
[mulle-env](//github.com/mulle-sde/mulle-env)         | custom environments for projects
[mulle-fetch](//github.com/mulle-sde/mulle-fetch)     | grab and unpack repositories and archives
[mulle-make](//github.com/mulle-sde/mulle-make)       | detect build method and build a project
[mulle-match](//github.com/mulle-sde/mulle-match)     | categorize files and make files
[mulle-monitor](//github.com/mulle-sde/mulle-monitor) | monitor a filesystem folder and trigger commands on change

