Alternative Commit Message Format (version 0.9)
=============================================

##What is it?
This is a proposal of labels (expressions enclosed in square brackets) to be used in commit messages. The goal is to identify easily the different types of changes in a repo.

##Commit Message rules

Common layout for a commit message
```
[tag>subtag] subject description

body: used to explain the what and why of a commit, not the how. Wrap the body at 72 characters in each line.

footer: used to reference issue tracker IDs.
```

####Subject desription (first line)
>1. Prefix the line with an applicable label
>2. Limit all the lines (subject included) to 72 characters
>3. Use the imperative tone in the subject line
>4. Separate subject from body with a blank line
>5. Capitalize the subject line
>6. Do not end the subject line with a period

A complete description, rules and tips can be seen in [1].

####Main tags and meaning for source code
**NOTE:** The first commit does not have a label, and the message always is "**Initial commit**" as convention.

>* [core] when functions, methods or classes have been added, modified or removed; method signatures or return types have changed
>* [style] when improving the format/structure of the code, without modifying the previous functionality
>* [main] when dealing with a file that is used as view, notebook or main file
>* [new] when adding a new feature (see *Rules* section)
>* [pkg] when libraries, frameworks, packages  or modules are added
>* [docs] when writing documentation, formatting or comments on code; no code change
>* [test] when adding tests, refactoring tests; no production code change
>* [misc] anything not covered by the above categories, e.g. rename or move files, add configuration files, add dataset

####Sub-labels
Those sub-labels are used in order to provide the action that the commit does

>Example:
>  [core>add] Subject description

>* *add* when something new has been added
>* *modify* when changes in files have been made
>* *boost* when improving performance
>* *fix* when fixing a bug (see *Rules* section)
>* *move* when files are moved between directories
>* *remove* when files or directories are deleted
>* *rename* when files or directories are renamed
>* *update* when a package's version is changed or updated(see *Rules* section)

When fixing something on:
>* *and* (*Android*)
>* *ios*
>* *linux*
>* *macos*
>* *win*

Those sub-labels must be used just in combination with other label to specify a particular change related to an O.S. or a comma-separated operating systems.
>Example:
>  [api>add|macos] Subject description

####Rules
1. The label [new] is only used when you are doing a merge between a change-branch and source branch.

2. The sub-label [update] must be used just when a package is updates ([pkg>update]).

3. Sometimes when you are doing modifications on your source code, it is likely to find a bug, in this case, after fixed it:
>+ [api>modify+fix] the code was modified: a bug was found and WAS fixed


##REFERENCES

1. [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/#why-not-how) Chris Beams
2. [TYPO3 CMS](http://wiki.typo3.org/CommitMessage_Format_(Git))
3. [Atom](https://atom.io/docs/v0.186.0/contributing)
4. [Karma](http://karma-runner.github.io/0.8/dev/git-commit-msg.html)

-------------
This document was last modified on : July 9th, 2020.
