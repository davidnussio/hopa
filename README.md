![Хопа-тропа](./assets/hopa-tropa.jpg)

<h1 align="center">Zero config JavaScript/TypeScript runner<br />right in your terminal</h3>

## Features

* Zero configuration 🚀
* Transpiles and runs JavaScript and TypeScript ⚙️
* Single-folder file browser 📁

## What and Why

**Hopa** is a command line tool that does the following:

1. Reads the current directory and lets you choose a file.
2. Transpiles the file and produces a valid JavaScript bundle. It uses [Rollup](https://rollupjs.org/) so it does resolve your imports.
3. Runs the generated bundle via node and shows you the result.
4. It also runs a watcher so changing the files will trigger new compilation.

I did this little tool because I'm tired of creating dummy repos, copying webpack files, switching between terminal and browser just so I can run some "modern" JavaScript. I know about solution like [CodeSandbox](https://codesandbox.io/) and [CodePen](https://codepen.io/) but I want specifically to exercise my code in the terminal. And I want to do it quick, without configuring stuff like Babel and Webpack.

More about the story here [https://krasimirtsonev.com/blog/article/hopa-javascript-typescript-runner](https://krasimirtsonev.com/blog/article/hopa-javascript-typescript-runner).

## Installation

```
npm i hopa -g
```

## Usage

Go to the folder that contains your files and run `hopa`.

```
> hopa
```

This will display a menu and you have to pick a file. You'll get transpilation, bundling, running and watching.

```
> hopa -i script.js -o bundle.js -m
```

Gets `script.js`, transpiles it and bundle it to a new file called `bundle.js` which is also minified. No watching in this case. It's a single-shot operation. `-m` and `-o` are optional. If the output is not specified Hopa creates a file with name `bundle.<your file>`. Have in mind that this feature is experimental. I find that in some cases Hopa can't resolve properly modules and errors out.


## Demo

![Hopa demo](./assets/hopa.gif)