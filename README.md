# Personal Site

## Misc

### Run LiveReload
1. `cd` into the project directory (`devon.zuegel.us/`)
2. Execute `$ docpad run`, and visit `http://localhost:9778/` to view the live-reloading site.

## Q&A

**Q:** *I've installed a plugin, but it doesn't appear to be doing anything!*

Try cancelling the running site and executing `$ docpad run` once again. The `package.json` file doesn't live-reload on save. 