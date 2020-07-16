NEAR Examples maintenance scripts
=================================

A couple scripts to quickly fetch & update all repositories from the
https://github.com/near-examples organization

![demo running status and pull](https://repository-images.githubusercontent.com/272589316/ebb9e480-af59-11ea-8aee-ad0a44455a8b)

_NOTE: These scripts have only been tested on macOS_


Use it
======

First, set up a token for pulling repositories:

* Go to https://github.com/settings/tokens
* Click "Generate new token"
* Give it a good "Note", like "'zamples scripting"
* Don't check any boxes; it's just pulling public repos
* Scroll down and hit "Generate token"
* In your `~/.bashrc` or equivalent, export an environment variable called
  `ZAMPLES_GITHUB_TOKEN` with the value of your new token

      ZAMPLES_GITHUB_TOKEN=the_value_github_gave_you

Now install some dependencies & clone this repo into a sensible location:

* Install prerequisites: `brew install jq`
* Must have [ssh key added to GitHub](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
* Set up a new directory where you want to clone _only_ the `near-examples`
  repositories (example: `~/code/n/x/`)
* Clone this repository into that new directory
* Optionally: add `./bin` to your PATH

If you've done the last step, you can change into your local near-examples
folder (following the example above, this would be `~/code/n/x`) and

* run `pull` to fetch the latest `master` for all `near-examples` repositories
* run `status` to quickly find out if all projects have `master` checked out
  with a clean working tree. You can pass options that you would normally pass
  to `git status`, such as `-s` for short output.
* run `run some command` to run "some command" in each repository
* use `dirty` to do things like quickly commit a bunch of changes. Example:

      for x in $(dirty); do (cd $x && git add --all && git commit -m "cool" && git push); done

If you don't complete the last step, you will have to type `./bin/pull` and
`./bin/status` instead.
