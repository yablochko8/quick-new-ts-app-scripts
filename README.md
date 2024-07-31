## How to use this tool

1. Create a folder for your scripts. This guide assumes your using a `bin` folder in your home directory, e.g.:
   `mkdir -p ~/bin`
1. Add that folder to your system path. In my case, the easiest way to do this was to edit .zprofile (a type of shell config file) in my home directory. I opened that in a text editor with this command...
   `open -e ~/.zprofile`
   (if that file doesn't exist for you you'll need to find a different way to add to system path)
1. Add this as a new first line to the config file you're editing:
   `export PATH="$HOME/bin:$PATH"`
1. Restart Terminal, and confirm path is updated:
   `echo $PATH`
1. Open this ~/bin folder in VS Code / Cursor, and clone this repo in Terminal:
   `git clone https://github.com/fractal-bootcamp/lui.shell-scripts`
1. In theory, any file at the top level of this project can be called from Shell. In practice, the only ones I call are `new-app` and `scrape-web`.

You should now be able to run the command `typespark` and have it work. By default, it will store all new projects to `~/typespark-apps`.

## Troubleshooting

If the command doesn't work, you may need to give the script executable permissions:

`chmod +x ~/bin/typespark`

PM2 shows the most recent error logs when you fire it up. This can sometimes be confusing. Use `pm2 flush` to clear out this noise.

## Future Features

### Upcoming Priorities

1. Store in pwd, not ~/typespark
1. Better script commmunication: don't run them automatically, show them in echo messages. Add them to the project README.
1. For full-stack projects add a shared folder at parent level (for types etc) by default
1. Add a better .env default and .env.example
1. Make README.md boilerplate better
1. Give the app a script that lets you fire up all created elements using pm2 at a later stage, and then use that in this script.

### Low Priority

1. Add support for non-Mac.
1. Fix the test suite part of this script so it works again with new folder structure.
