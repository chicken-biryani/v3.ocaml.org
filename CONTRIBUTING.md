# How to contribute

Welcome to v3.ocaml.org's contributing guide.

Ocaml's a community-driven project and your help to v3.ocaml.org is extremely welcome.

## Code of Conduct

## How to get started

We are particularly motivated to support new contributors. Here are a few ways to get started. You could contribute to a bunch of issues suggested below:


- **Good First Issues** 
You can look at the good first issues in four repositories:
    - [ocaml/ood](https://github.com/ocaml/ood/labels/good%20first%20issue). 
    - [ocaml/v3.ocaml.org](https://github.com/ocaml/v3.ocaml.org/labels/good%20first%20issue).
    - [ocaml-docs-ci](https://github.com/ocurrent/ocaml-docs-ci/labels/good%20first%20issue).
    - [ocaml/v3.ocaml.org-server](https://github.com/ocaml/v3.ocaml.org-server/labels/good%20first%20issue).

- **Fix or suggest content to ocaml/ood**
 Add some scrapped blog posts. You can help with importing the blog posts from [here.](https://github.com/ocaml/platform-blog.)
- **Implement pages**
 You can search through existing issues [over here](https://github.com/ocaml/v3.ocaml.org/projects/11) to find out what pages are planned for upcoming implementation.
- **File an issue**
 File an issue suggesting improvements [over here.](https://github.com/ocaml/v3.ocaml.org/issues/new)


**Note: If you get stuck, chat with us on [Discord.](https://discord.com/channels/436568060288172042/585511202759770135)**

> 

## Reporting bugs

We use GitHub issues to track all bugs and feature requests; feel free to open an issue over [here](https://github.com/ocaml/v3.ocaml.org/issues/new) if you have found a bug or wish to see a feature implemented.


## Setup and Development

### Prerequisities

The site-building process assumes that you have `npx` available. Run `npx --version` to test your installation. If you don’t have `npx`, you will need to install node, the package that npx is part of. Currently, we require node LTS Version 14.x. Please consult the Node.js website for instructions on installing it.

Our recommendation is to use a node version manager, such as [fnm](https://github.com/Schniz/fnm) or [nvm](https://github.com/nvm-sh/nvm). Therefore, please install one of these tools instead. 

If you do have `npx` [fork and clone the repository](https://github.com/ocaml/v3.ocaml.org) and run the following command in the root directory of the repo:

```bash
echo 14 > .nvmrc
fnm install # run this
nvm install # or this
```

Now check that `npx --version` works, and that `node --version` returns v14.x. Note that we have added `.nvmrc` to `.gitignore`, so you can leave that file in your directory.


### Quickstart

Once you have the node toolchain installed, the easiest way to get the project installed, built, and get the development servers started is to run:

```bash
make
```

Yes, it's that simple. However, if you'd like a little more fine-grained control over installing, building, and running the development servers, please see the sections below.

### Dependencies

Run the following command to install various dependencies:

```
make install-deps
```

The command installs all dependencies, including compilers such as ReScript and OCaml, and package managers like esy. It also vendors in the `ood` library, to support its co-development. All depdencies are installed in a project local way, so there will be no affect on your system or other projects.

### Development

Use the following command to run the ReScript compiler in watch mode as well as the NextJS dev server:

```
make watch
```

Go to `http://localhost:3000`



**Note :** 
- Ensure that the site remains static. Have a look at the nextjs's functionalities to be avoided overe [here.](https://nextjs.org/docs/advanced-features/static-html-export#caveats)
- Build CSS separately via `npx postcss` . This is useful for debugging.

```
npx postcss@8.3.1 styles/main.css -o /tmp/test.css
```

### Test production setup

```
make build && make serve
```

## Git and GitHub workflow

The preferred workflow for contributing to a repository is to fork the main repository on GitHub, clone, and develop on a new branch.

If you aren't familiar with how to work with Github or would like to learn it, here is [a great tutorial](https://app.egghead.io/playlists/how-to-contribute-to-an-open-source-project-on-github).

Feel free to use any approach while creating a pull request. Here are a few suggestions from the dev team:

- If you are not sure whether your changes will be accepted or want to discuss the method before delving into it, please create an issue and ask it.
- Clone the repo locally (or continue editing directly in github if the change is small). Checkout
  out the branch that you created.
- Create a draft pull request with a small initial commit. Here's how you can [create a draft pull request.](https://github.blog/2019-02-14-introducing-draft-pull-requests/)
- Continue developing, feel free to ask questions in the PR, if you run into obstacles or uncertainty as you make changes
- Review your implementation according to the checks noted in the PR template
- Once you feel your branch is ready, change the PR status to "ready to review"
- Consult the tasks noted in the PR template
- When merging, consider cleaning up the commit body
- Close any issues that were addressed by this PR.


## Design and Information Architecture

The Design uses Figma and is currently managed by designer. Discussion of both design and content is managed with Figma commenting system.

You can have a look at the sitemap and information architecture on flowmap over [here.](https://app.flowmapp.com/share/6e5eeb4573f9e110ac779691fee85422/sitemap/)

## Architecture
## Coding style


## Acknowledging contributions
We follow the [all-contributors](https://allcontributors.org/) specification and recognize various types of contributions. Take a look at our past and current contributors!