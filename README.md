# git-config

My Git configuration, consisting of the following three files discussed herein.

## `config`

The Git configuration file includes aliases & other niceties support my typical workflow. 

## `ignore`

The global Git ignore file transcends all project types, and may provide a degree of insulation from the absence of a `.gitignore` file in a particular repository. It does not, however, preclude the use of a project-specific `.gitignore` file. As a starting point for those, consider reference `.gitignore` files maintained by either [GitHub](https://github.com/github/gitignore) or [gitignore.io](https://gitignore.io).

## `attributes`

The attributes file maps attributes to paths. At the time of this writing, it may only prove useful if you choose to incorporate support for diff-ing either `.plist` or `.strings` files.

## Usage

In all likelihood you will already have files in place for this purpose; in that case, simply integrate excerpts into your existing configuration. Otherwise, you can incorporate them in one of the following methods:

### Method 1
 1. Copy each file to `~/.config/git`. 
 
### Method 2
 1. Move `config` to `~/.gitconfig`. 
 1. Move `ignore` to `~/.global_ignore` and enter the following at the command line: `git config --global core.excludesfile ~/.global_ignore`. 
 1. Move `attributes` to `~/.gitattributes` and enter the following at the command line: `git config --global core.attributesfile ~/.gitattributes`.

## References

- [Documentation for `git-config`](https://git-scm.com/docs/git-config)
- [Documentation for `gitignore`](https://git-scm.com/docs/gitignore)
- [Documentation for `gitattributes`](https://git-scm.com/docs/gitattributes)
- The `subup` alias and use of the OS X credential helper were derived from [@schwa](https://github.com/schwa/git-config). Thank you.
