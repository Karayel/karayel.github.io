---
published: true
title: Manage Packages with npm
layout: post
tags: [npm, manage, package]
categories: [npm]
---
<b><u>Install</u></b>

{% highlight js %}
npm install npm
{% endhighlight %}

<b><u>Up to Date</u></b>

{% highlight js %}
npm install npm -g
{% endhighlight %}

<b><u>Login</u></b>

To see who you're logged in as, run `npm whoami`

To create your account, run `npm adduser`

<b><u>Start Project</u></b>

Run `npm init --scope=<username>`, and replace <username> with the user
you created in the last lesson. This will create a package.json file.

{% highlight js %}
{
  "name": "q",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
{% endhighlight %}

<b><u>Install A Module</u></b>

To install a module, use the `npm install <modulename>` command.

Try running `npm install @linclark/pkg --save` to install the module, and also
update your package.json file at the same time.

<b><u>Listing Dependencies</u></b>

You can do this using the `npm ls` command.

<b><u>npm test</u></b>

If you look at the package.json file, it has this rather odd bit in it:

{% highlight js %}
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
{% endhighlight %}

npm can be used as a task runner, and almost every module and project
will have a test script that runs to make sure everything is good.  In
order to help remind you to do this, npm puts a "always failing" test
in there by default.

First, create a file called `test.js`.  It doesn't have to do anything,
really.  (This is npm class, not testing class.)  But it has to exit
without throwing an error, or else the test fails.

Then, edit your `package.json` file to make your scripts section look like
this instead:

{% highlight js %}
  "scripts": {
    "test": "node test.js"
  },
{% endhighlight %}

<b><u>Package Niceties</u></b>

So, we've created a package.json file, but it's missing a few things
that people usually expect.  If you type `npm install`, you'll see
something like this:

{% highlight js %}
npm WARN package.json karayel@1.0.0 No description
npm WARN package.json karayel@1.0.0 No repository field.
npm WARN package.json karayel@1.0.0 No README data
{% endhighlight %}

Before we can share this work of art with the world, we need to make
it a bit more polished so that people know how to use it.

First, create a README.md file, with a bit of words in it.

Then, add a "repository" field in your package.json file, with a url
where people can access the code.

You can edit your package.json file by hand, or run `npm init` again.

<b><u>Publish</u></b>

Packages get into the registry by using the `npm publish` comman

<b><u>Version</u></b>

{% highlight html %}
 1.2.3
  ^ ^ ^
  | | `-- Patch version. Update for every change.
  | `---- Minor version. Update for API additions.
  `------ Major version. Update for breaking API changes.
{% endhighlight %}

npm has a special command called `npm version` which will update your
package.json file for you, and also commit the change to git if your
project is a git repository.  You can learn more at `npm help version`.

<b><u>Dist tag</u></b>

{% highlight js %}
npm dist-tag add @karayel/karayel@1.0.1 ["version":"1.0.1"]
{% endhighlight %}

<b><u>Dist tag removal</u></b>

{% highlight js %}
npm dist-tag rm @karayel/karayel ["version":"1.0.1"]
{% endhighlight %}

<b>change latest</b> : 

{% highlight js %}
npm dist-tag add @karayel/karayel@1.0.0 latest
{% endhighlight %}

<b><u>Outdated</u></b>

Now that we have some dependencies, and you've learned that your own
packages can be updated repeatedly, the obvious question is: What do
we do when someone *else* updates *their* package?

The first step is to detect this.  Because of the way that we define
our dependencies with a version range, and each release is a unique
combination of a name and a version, we can detect compatible releases
programmatically with the `npm outdated` command.

<b><u>Update</u></b>

{% highlight js %}
npm update or up
{% endhighlight %}

<b><u>Rm</u></b>

If you have a way to put stuff there, then naturally, you'll one
day need a way to delete them.

Enter the `npm rm` command (aka `npm uninstall` if you prefer to
type things out long-hand).	

Just like you can use `--save` on installing packages, you can also
use `--save` when removing packages, to also remove them from your
package.json file.

{% highlight js %}
npm uninstall @linclark/pkg --save
{% endhighlight %}
