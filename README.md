# Modified README.md

This is a modified version of redmine-slack where the project identifier
is used as the channel name (instead of using a Custom Value wich have to be
setted on every issue).

To install this modified version please do:

    git clone https://github.com/lpenap/redmine-slack.git redmine_slack
    bundle install

# Slack chat plugin for Redmine

This plugin posts updates to issues in your Redmine installation to a Slack
channel. Improvements are welcome! Just send a pull request.

## Screenshot

![screenshot](https://raw.github.com/sciyoshi/redmine-slack/gh-pages/screenshot.png)

## Installation

From your Redmine plugins directory, clone this repository as `redmine_slack`:

    git clone https://github.com/sciyoshi/redmine-slack.git redmine_slack

You will also need the `httpclient` dependency, which can be installed by running

    bundle install

from the plugin directory.

Restart Redmine, and you should see the plugin show up in the Plugins page.
Under the configuration options, set the Slack API URL to the URL for an
Incoming WebHook integration in your Slack account.

## Customized Routing

You can also route messages to different channels on a per-project basis. To
do this, create a project custom field (Administration > Custom fields > Project)
named `Slack Channel`. If no custom channel is defined for a project, the parent
project will be checked (or the default will be used). To prevent all notifications
from being sent for a project, set the custom channel to `-`.

For more information, see http://www.redmine.org/projects/redmine/wiki/Plugins.
