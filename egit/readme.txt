This is the readme for the egit tool.

This tool was built to make managing subrepos easier during development.

-----------------------------how to use------------------------------------

The syntax is as follows:

egit <options> <command> <submodule>


options: 
-h                    prints help
-m                    specify commit message. Works like `git commit -m <message>`
-r                    sprcify project root. Defaults to /var/www/html


commands:
initialize           sets up submodules. you will proabably never need this one.
add                  runs 'git add .' in project root and specified submodule.
commit               runs 'git commit -m <message>' in project root and specified submodule.
push                 pushes staged changes to root and module repositories
pull                 pull from root and specified submodule repos
fetch                fetch from root and specified submodule repos
gap                  combines add, commit, and push.

submodules:
modules              the app/code directory where our custom modules live
theme                app/design/frontend/Eduporium/Eduporium


--------------------------examples----------------------------------------

egit add theme
egit add modules

egit commit theme -m "did some updates"

egit push theme

egit pull modules

egit fetch modules

egit gap modules -m "updated stuff"

