# Git Cheatsheet for Writers
Technical writers often use [Git](https://git-scm.com/)) or other version control software with different tools than developers. Writers have different workflows and backgrounds, too. This cheatsheet offers concise, better-tailered tips.

[MkDocs Setup](#mkdocs-setup) - [MadCap Flare Setup](#madcap-flare-setup) - [Repository Setup](#repository-setup) - [Branching Styles](#branching-styles)

## MkDocs Setup
**Don't** commit MkDocs libraries (unless you have written custom plugins). Instead, each writer should run the installation commands.

## MadCap Flare Setup
**Don't** bind your project to Flare's built-in Git/Subversion plugin. It's incomplete, buggy, and neglected. Instead, install a normal version of the software, and use the cheatsheet commands.

Flare likes to re-arrange source files sometimes. This bloats the repository's size with irrelevant changes. It drowns out your "real" changes during peer reviews or pull request/merges, too, because it may look like you changed _every_ line in the file. To prevent that problem, install a [smudge]().

## Repository Setup
If you will use Flare with its Git plugin (not recommended), then **don't** add a `README.md`. Otherwise, Flare will think that the repository has already been bound.

Add `.gitignore` etc. to the repository to avoid writers accidentally committing personal settings or MkDocs/Docusaurus/Hugo/etc. libraries.

## Branching Styles
Because developers' tools and workflows are different and designed with version control in mind, when and why they create a repository "branch" (version of the files that has different history/changes) can be different, too.

For example, developers might want to create a release branch (`release/2_0_0`) early so that automatic compatibility tests will run and give them warning about what APIs would break. Documentation doesn't use the same APIs, and therefore doesn't need to branch at the same time. Branching early could even be bad for the writers: documentation often has many changes later in the development cycle, and this would mean that lots of changes would need to be applied to 2 branches, not just 1 branch.
