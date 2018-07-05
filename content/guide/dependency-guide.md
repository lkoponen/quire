---
title: Quire Dependency Guide
type: page
---

Each Quire project relies on two projects the `quire-cli` a command line interface (cli) to run commands to preview and build a static website, a PDF or an EPUB and the `quire-starter-theme` a front end development toolkit that allows users to shape the output of the website, PDF and EPUB. This page explains what makes these two projects work and what major dependencies currently make quire what it is.

<a alt="HUGO" title="HUGO" href="https://gohugo.io/"><img src="../images/hugo-logo.png" alt="HUGO" title="HUGO" width="100"/></a>

> Hugo is a static HTML and CSS website generator written in Go. It is optimized for speed, ease of use, and configurability. Hugo takes a directory with content and templates and renders them into a full HTML website. Hugo relies on Markdown files with front matter for metadata, and you can run Hugo from any directory. This works well for shared hosts and other systems where you don’t have a privileged account.

Quire makes use of Hugo via the npm package <a href="https://www.npmjs.com/package/hugo-bin"/>`hugo-bin`</a>

Quire uses Hugo’s cli, templating system and http server. to create a way to preview your site while editing the front end code, build a static html site and aids Prince XML to create a PDF of your publication you are building.

<a  alt="Prince XML" title="Prince XML" href="https://www.princexml.com/"><img src="../images/prince-xml-logo.png" alt="Prince XML" title="Prince XML" width="100"/></a>

> Prince can also be used by authors and publishers to typeset and print documents written in HTML, XHTML, or one of the many XML-based document formats. Prince is capable of formatting academic papers, journals, magazines, and books.

Quire uses the output of Hugo static-site generator to build a PDF as referenced above.

<a href="https://webpack.js.org/" alt="webpack" title="webpack" ><img src="../images/webpack-logo.png" alt="webpack" title="webpack" width="150"/></a>

> At its core, webpack is a static module bundler for modern JavaScript applications. When webpack processes your application, it internally builds a dependency graph which maps every module your project needs and generates one or more bundles.

Quire makes use of Webpack via the npm package <a href="https://www.npmjs.com/package/webpack"/>`webpack`</a>

Currently Quire starter theme uses the latest version of Webpack 4 to bundle front end assets and support the development workflow.

To modify the Webpack configuration for your project edit this file

`<your-project-directory>/themes/quire-starter-theme/webpack.config.js`

### [pe-epub](https://github.com/peoples-e/pe-epub) and [pe-epub-fs](https://github.com/peoples-e/pe-epub-fs)

>"pee pub" makes epubs better. Our goal is to make it as easy as possible to output a valid epub. It's used in production over at The People's E-Book. pe-epub-fs extends pe-epub so you can import local assets from your filesystem rather than from the web.

Quire uses these projects to generate the EPUB file. This file can be access on any device or software that reads the .epub file format. These projects generate a mostly style stripped version of the publication. These projects have been receiving limited maintenance. Quire is currently seeking a replacement to output the EPUB file.

## Quire Dependency Tables

### CLI Dependencies

| Dependency | NPM Description | Function in Quire |
| --- | --- | --- |
| axios | Promise based HTTP client for the browser and node.js |  |
| chalk | Terminal string styling done right |  |
| cheerio | Fast, flexible & lean implementation of core jQuery designed specifically for the server. |  |
| command-exists | node module to check if a command-line command exists |  |
| commander | The complete solution for node.js command-line interfaces, inspired by Ruby's commander. |  |
| execa | A better `child_process` |  |
| glob | Match files using the patterns the shell uses, like stars and stuff. |  |
| hugo-bin | Binary wrapper for Hugo |  |
| js-yaml | YAML 1.2 parser / writer for JavaScript | |
| lodash | The Lodash library exported as Node.js modules. |  |
| pe-epub | Makes epubs better. |  |
| pe-epub-fs | Extends pe-epub so you can import local assets from your filesystem rather than from the web |  |
| rimraf | The UNIX command rm -rf for node. |  |
| striptags | An implementation of PHP's strip_tags in Node.js. |  |
| webpack | webpack is a module bundler |  |
| yaml-front-matter | Parses yaml or json at the front of a string. Places the parsed content, plus the rest of the string content, into an object literal. |  |

### CLI Dev Dependencies

| Dependency | NPM Description | Function in Quire |
| --- | --- | --- |
| eslint | ESLint is a tool for identifying and reporting on patterns found in ECMAScript/JavaScript code. |  |
| eslint-config-standard |  |  |
| eslint-plugin-promise | Enforce best practices for JavaScript promises. |  |
| eslint-plugin-standard | ESlint Rules for the Standard Linter |  |
| jsdoc | An API documentation generator for JavaScript. |  |
| jsdoc-template-argon |  |  |
| mocha | Simple, flexible, fun JavaScript test framework for Node.js & The Browser |  |
| tmp | A simple temporary file and directory creator for node.js. |  |
