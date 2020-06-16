NEAR Examples maintenance scripts
=================================

A couple scripts to quickly fetch & update all repositories from the
https://github.com/near-examples organization

![demo running status and pull](https://repository-images.githubusercontent.com/272589316/ebb9e480-af59-11ea-8aee-ad0a44455a8b)

_NOTE: These scripts have only been tested on macOS_


Use it
======

* Install prerequisites: `brew install jq`
* Must have [ssh key added to GitHub](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
* Set up a new directory where you want to clone _only_ the `near-examples`
  repositories (example: `~/code/n/x/`)
* Clone this repository into that new directory
* Optionally: add `./bin` to your PATH

If you've done the last step, you can change into your local near-examples
folder (following the example above, this would be `~/code/n/x`) and

* run `pull` to fetch the latest `master` for all `near-examples` repositories
* run `status` to quickly find out if all projects are up-to-date

If you don't complete the last step, you will have to type `./bin/pull` and
`./bin/status` instead.
