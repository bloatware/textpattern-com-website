# Textpattern.com website

[![Greenkeeper badge](https://badges.greenkeeper.io/textpattern/textpattern-com-website.svg)](https://greenkeeper.io/)
[![Build Status](https://img.shields.io/travis/textpattern/textpattern-com-website.svg)](https://travis-ci.org/textpattern/textpattern-com-website)

Official 2017+ website of the [Textpattern](https://textpattern.io/) project. **Currently under development. Requires Textpattern 4.7dev.**

## Supported web browsers

* Internet Explorer 11.
* Chrome, Edge, Firefox, Safari and Opera the last two recent stable releases.

Older versions of the above and other browsers may work, but these are the ones we verify.

## Requirements

Building this repository requires:

* [Node.js](https://nodejs.org/) >=4.0
* [Grunt](https://gruntjs.com/) >=1.0
* [Composer](https://getcomposer.org/)

## Setup

### Installing required tools

The project uses [Grunt](https://gruntjs.com/) to run tasks and [Sass](http://sass-lang.com/) for CSS pre-processing. First make sure you have base dependencies installed: [Node.js](https://nodejs.org/) and [Grunt](https://gruntjs.com/). You can install Node using the [installer](https://nodejs.org/), Composer using the [installer](https://getcomposer.org/), and Grunt with npm:

```ShellSession
$ npm install -g grunt-cli
```

Consult the Grunt documentation for more instructions if necessary. You might need to use `sudo npm install -g grunt-cli` instead when installing on certain Unix-based systems.

### Installing dependencies

After you have the base dependencies taken care of, you can install the project's dependencies. Navigate to the project's directory, and run the dependency manager:

```ShellSession
$ cd textpattern-com-website
$ npm install
$ composer install
```

**npm** installs Node modules for Grunt and **composer** installs PHP libraries. You might need to use `sudo` instead when installing on certain Unix-based systems.

## Building

This repository hosts sources and needs to be built before it can be used. After you have installed all dependencies, you will be able to run tasks using Grunt, including building:

```ShellSession
$ grunt @task@
```

Where the `@task@` is either `build` or `watch`.

* The `build` task builds the project.
* The `watch` task will launch a task that watches for file changes; the project is then automatically built if a source file is modified.

## Shortcodes

Textpattern 4.7 introduced support for user-definable `<txp:output_form />` attributes, allowing for our own version of 'shortcodes' within articles. This site uses the following tags:

### Video

To create a HTML5 video snippet:

    <txp::media_video width="" height="" ratio="" mp4-url="" webm-url="" poster-url="" duration-seconds="" />

`ratio`, `poster-url` and `duration-seconds` are optional, but should be provided if possible. If not used, remove those attributes from your tag.

For example:

    <txp:media_video width="640" height="480" ratio="0.5625" mp4-url="/video/video1.mp4" webm-url="/video/video1.webm" poster-url="/video/video1-poster.png" duration-seconds="20" />

TODO: more tags.

## Plugins used

TODO: use Composer to install plugins? If so need to create PRs on each of the listed plugins below where Composer support is not currently provided.

Plugins required for this website to function:

* `rah_flat` or `oui_flat` TBC
* `etc_pagination` (v0.4.7b)
* `zem_contact_reborn` (v4.5.0.0)
* TODO
