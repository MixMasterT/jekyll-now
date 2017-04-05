---
layout: post
title: Green -- Not always a bad thing
---

## Still Need a Shamrock

The luck of the Irish has not been with me recently. However, that is no
reason to slow down or give up. I have been trying to truly understand Webpack
and I have gained some insights by reading blogs, checking out documentation,
and watching videos online.

So far, I have learned a bit, and I want to share that with any interested
readers who might be stopping by.

First, the package.json file is an important key. This file lives in the
root directory of your project, and lists important meta information about
the project in JSON format. When you run 'npm init' or 'yarn init' a series
of questions comes up in the command line to help fill in some of this basic
info. That can be annoying, so you can add the --yes (or -y) flag after
the init command to skip this process. If you have a .npmrc file in your
home directory, the defaults will be taken from there when you use the -y
(or --yes) flag. You can use 'npm set init.[field] "<YOUR DETAILS>"' at
the command line to generate the .npmrc file. The fields include 'author.name'
'author.email', 'author.url' and 'license' among other things. You can
alternatively create your own .npmrc file with a text editor. Each declaration
goes on a new line, with no spaces and an equal sign to relate the field
to the value, like this: "init.author.name=Torah Oglander". Setting these
defaults will save you time!

After generating a package.json file, the next step in building with Webpack
is to import dependencies. Any npm package that you want to use, such as
babel-loader or react can be installed in the project with the command:
'npm install <desired package> --save' or 'yarn add <desired package>'.
Installing will add the package to a local node_modules director. It will
generate this directory if it doesn't already exist. You must add webpack
as a dependency with this process in order to use it. Don't forget!
The --save flag tells npm to add the listed package (or packages) to the
'dependencies' list in your package.json file. This is important because it
allows anyone to regenerate the same node_modules contents with the
command "npm init" (or just "yarn") if they want to run your project
somewhere else. You can also add the -dev flag after --save to save the
dependency as a 'dev' dependency, which can be desirable, though I am not
yet sure why.

So far, this post has mostly been about setting up the package.json contents.
That is a necessary prerequisite to running a Webpack build. You can still
add more packages and modify package.json after your first Webpack build, but
something needs to be there first, before Webpack will be able to do anything.
When you want to actually run your code, you need to run the 'webpack.'

To run webpack, you can either pass in the source, and then the build destination
as command line arguments, or you can set up a webpack.config.js file
to specify details of how exactly you want your project bundled. using
webpack.config.js is the preferred method.

I will be adding a more detailed post soon with more specifics about how
to set up webpack.config.js, so check back for that!
