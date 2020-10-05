[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Bit%20-%20a%20modern%20git%20cli%20&url=https://github.com/chriswalz/bit&hashtags=bit,git,cli,developers)
<p align="center">
<img
    src="https://user-images.githubusercontent.com/6971318/94226426-96309480-fec5-11ea-929f-34551c5356dd.png"
    width="800px" border="0" alt="croc">
<br>
<a href="https://github.com/chriswalz/bit/tags"><img src="https://img.shields.io/badge/version-v0.4.1-brightgreen.svg?style=flat-square" alt="Version"></a>
<a href="https://goreportcard.com/report/github.com/chriswalz/bit"><img src="https://goreportcard.com/badge/github.com/chriswalz/bit" alt="Version"></a>
</p>

`bit` is an experimental modernized git CLI built on top of git that provides happy defaults and other niceties:

- command and **flag suggestions** to help you navigate the plethora of options git provides you
- autocompletion for files and branch names when using 
`bit add` or `bit checkout`
- automatic fetch and **branch fast-forwarding** reducing the likelihood of merge conflicts 
- suggestions **work with git aliases**
- new commands like `bit sync` that vastly simplify your workflow 
- commands from **git-extras** such as *git-release* & *git-info*
- **fully compatible with git** allowing you to fallback to git if need be.  

## Installation


```shell script
curl -sf https://gobinaries.com/chriswalz/bit | sh;
curl -sf https://gobinaries.com/chriswalz/bit/bitcomplete | sh && echo y | COMP_INSTALL=1 bitcomplete
```

Verify installation with:

`bit`

Dependencies: Git

Platform Support:
- iTerm2 (macOS)
- Terminal.app (macOS)
- Command Prompt (Windows)
- gnome-terminal (Ubuntu)

## Bit specific command Usage 

Create a new commit

`bit save [commit message]`

Save your changes to the current branch [amends current commit when ahead of origin]

`bit save` 

Synchronize your changes to origin branch (Beta)

`bit sync`

You have access to ALL git commands as well. 90% of the time the above commands will have you covered. 

`bit commit -m "I can still use git commands"`, `bit pull -r origin master`

## Example Workflow
`bit switch example-branch`
Branch does not exist. Do you want to create it? Y/n

yes

Switched to a new branch 'example-branch'

[Makes some changes]

`bit save "add important feature"`

[fix an error for important feature]

`bit save`

[push changes to origin]

`bit sync`

[two days later confirm your branch is in sync with origin]

`bit sync`




## Features

- Automatic fetching & fast forwarding to keep your branches up to date and prevent merge conflicts
- Every branch is a completely independent line. Changes in your working directory are saved and in the branch that you switch saved changes are retrieved.
- Simplify your entire rebase workflow with a single command `bit sync [branch-name]` 
- Automatic suggestions at your fingertips 
- `bit` is **fully compatible** with `git`. All features of git are available if need be.  


## Principles 

1. Think in the age of the cloud
1. Embed the spirit of modern day workflows
1. Favor simplicity over complexity 
1. Bit should have happy defaults
1. Bit must be fully compatible with Git

## Inspiration

Thanks to [Gitless](https://gitless.com/), [git-extras](https://github.com/tj/git-extras), researchers in the field and of course the developers of git itself! 
