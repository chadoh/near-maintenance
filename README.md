NEAR Examples maintenance scripts
=================================

A couple scripts to quickly fetch & update all repositories from the
https://github.com/near-examples organization

_NOTE: These scripts have only been tested on macOS_

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

* Install prerequisites: `brew install jq hub`
* Set up a new directory where you want to clone _only_ the `near-examples`
  repositories (example: `~/code/n/x/`)
* Clone this repository into that new directory
* Optionally: name the local project folder for _this_ repository `bin` and add
  `./bin` to your PATH

If you've done the last step, you can change into your local near-examples
folder (following the example above, this would be `~/code/n/x`) and 

* run `pull` to fetch the latest `master` for all `near-examples` repositories
* run `status` to quickly find out if all projects are up-to-date

If you don't complete the last step, you will have to type
`./near-maintenance/pull` and `./near-maintenance/status` instead.
