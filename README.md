<div>
  <img src="jamstack.jpeg" alt="JamStack Conf" />
  <hr />
  <h1 align="center">💿 Remix Workshop</h1>
  <p>
    Remix enables you to build fantastic user experiences for the web and feel
    happy with the code that got you there. In this workshop, we'll explore
    the core patterns in Remix that enable this, as well as some of its more
    advanced features.
  </p>
</div>

<hr />

## Prerequisites

- Some
  [experience with JavaScript](https://kentcdodds.com/blog/javascript-to-know-for-react)
- Some [experience with React](https://kcd.im/beginner-react)
- Some [experience with Node.js](https://nodejs.dev/learn)

## System Requirements

- [git][git] v2.13 or greater
- [NodeJS][node] `14 || 16 || 18`
- [npm][npm] v8 or greater

All of these must be available in your `PATH`. To verify things are set up
properly, you can run this:

```shell
git --version
node --version
npm --version
```

If you have trouble with any of these, learn more about the `PATH` environment
variable and how to fix it here for [Windows][win-path] or
[mac/linux][mac-path].

## Setup

Follow these steps to get this set up:

```sh
git clone https://github.com/remix-run/jamstack-conf-workshop.git
cd advanced-remix
npm run setup
```

If you experience errors here, please open [an issue][issue] with as many
details as you can offer.

### Exercises

You'll find all the exercises in the `exercises` directory. The finished version
of each exercise is in the `final` directory. Each directory is a completely
contained Remix app.

The purpose of the exercise is **not** for you to work through all the material.
It's intended to get your brain thinking about the right questions to ask me as
_I_ walk through the material.

### Running each app

Each directory in the `final` and `exercises` directories is a Remix app. The
easiest way to run these without having to `cd` into each directory is to use
the `dev.js` script in the root of this repository:

```sh
# to run the first exercise app:
node dev exercise/01

# This runs the first exercise too:
node dev 1

# or to run the final version of the 2nd exercise
node dev final/02
# this runs the 1st extra credit of the final version of the 2nd exercise
node dev final2.1

# this will just ask you which one you want to run
node dev
```

Each will run on a unique port so you can run multiple apps at once.

Unfortunately, due to the nature of this workshop, <kbd>⌘</kbd> + <kbd>P</kbd>
isn't very useful (because there are a LOT of duplicate files). If you'd prefer,
you can open each exercise in its own editor. Or just make sure to prefix your
searches with "exercise/03" (for example) so you're searching in the right app.

### Diffs

You can use the `diff.js` script to be shown the differences between what's in
any of the apps. For example:

```sh
# to be shown the differences between the first exercise and the final version:
node diff exercise/01 final/01

# We've got some sensible defaults in place so you can get the same diff as above with:
node diff 1

# And for comparing yourself to extra credits, you can run:
node diff exercise/02 final/02.2

# this will just ask you which ones you want to diff
node diff
```

This can be handy for you to run when you think you're done but things aren't
quite working as you expect.

Sometimes there are changes that happen outside of the tutorial because they're
unrelated to Remix but they can be handy to know about, so the diff command can
help with that:

```sh
# To be shown the changes that happened to prepare for the exercise:
node diff final/04 exercise/05
```

**NOTE:** Unfortunately, there's no way to exclude some files from the diff
we're doing, so we limit the diff to only the `app` directory (where almost all
of your code changes happen). You'll need to ignore any changes to
`styles/tailwind.css` however. That's a generated file. Sorry about that.

<!-- prettier-ignore-start -->
[npm]: https://www.npmjs.com/
[node]: https://nodejs.org
[git]: https://git-scm.com/
[build-badge]: https://img.shields.io/github/workflow/status/remix-run/jamstack-conf-workshop/%E2%9C%85%20Validate/main?logo=github&style=flat-square
[build]: https://github.com/remix-run/jamstack-conf-workshop/actions?query=workflow%3Avalidate
[license-badge]: https://img.shields.io/badge/license-GPL%203.0%20License-blue.svg?style=flat-square
[license]: https://github.com/remix-run/jamstack-conf-workshop/blob/main/LICENSE.md
[win-path]: https://www.howtogeek.com/118594/how-to-edit-your-system-path-for-easy-command-line-access/
[mac-path]: http://stackoverflow.com/a/24322978/971592
[issue]: https://github.com/remix-run/jamstack-conf-workshop/issues/new
<!-- prettier-ignore-end -->
