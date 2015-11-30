# sublime-cssnext

> Sublime plugin to use tomorrow's CSS syntax

cssnext is a CSS transpiler that allows you to use the latest CSS syntax today. It transforms CSS specs into more compatible CSS so you don’t need to wait for browser support.


## Install

Install `cssnext` with [Package Control](https://sublime.wbond.net) and restart Sublime.

**You need to have [Node.js](http://nodejs.org) >=0.12.0 installed.**  
Make sure it's in your $PATH by running `node -v` in your command-line.  
On OS X you need to make sure it's in `/usr/local/bin` or symlink it there.


## Getting started

In a CSS file, open the Command Palette *(Cmd+Shift+P)* and choose `cssnext`. You can alternatively create one or more selections before running the command to only prefix those parts.


### Options

*(Preferences > Package Settings > Cssnext > Settings - User)*

You can specify which browsers you need to support using an array of rules.

See the [supported browser names](https://github.com/ai/autoprefixer#browsers).


#### Default

```json
{
	"browsers": ["last 2 versions"]
}
```


#### Example

```json
{
	"browsers": ["last 1 version", "> 10%", "> 5% in US", "ie 8", "ie 7"]
}
```

This will add the needed prefixes for the last version of each browser, all browsers with market share of more than 10% globally and 5% in the US, and Internet Explorer 7 and 8.


### Keyboard shortcut

You can also set up a keyboard shortcut to run the command by opening up "Preferences > Key Bindings - User" and adding your shortcut with the `cssnext` command.

Example:

```json
[
	{ "keys": ["alt+super+p"], "command": "cssnext" }
]
```


### Project settings

You can override the default and user settings for individual projects. Just add an `"Autoprefixer"` object to the `"settings"` object in the project's `.sublime-project` file containing your [project specific settings](http://www.sublimetext.com/docs/3/projects.html).

Example:

```json
{
	"settings": {
		"Autoprefixer": {
			"browsers": ["last 1 version"]
		}
	}
}
```


## License

MIT © [zhowenbin](http://zhouwenbin.com) 
[sublime-autoprefixer](https://github.com/sindresorhus/sublime-autoprefixer) thanks [Sindre Sorhus](http://sindresorhus.com) 
[postcss-cssnext](https://github.com/cssnext/postcss-cssnext) thanks [cssnext](https://github.com/cssnext/postcss-cssnext)
