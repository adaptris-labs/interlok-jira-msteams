# interlok-jira-msteams
The suggested name was `ubiquitous-bassoon`

## Why ![Interlok Hammer](https://img.shields.io/badge/certified-interlok%20hammer-red.svg)

Well, we're using MS Teams; we have Jira. The Jira connector creates action cards that _aren't quite right_ for us.
Jira has webhooks that can post to arbitrary endpoints; MS Teams cards are just JSON, acceptable on a HTTPS endpoint... 

Honestly, when you have a integration product what did you expect us to do.

## Bonus Chatter

At the moment, it explicitly filters issue types of "Sub-Task" and discards any pending updates for those; it doesn't have to, but if your team likes to break down stories into a lot of tasks, then this might be suitable for you to remove any excess chatter in your action cards.

## Things to do

* Well, the links are hard-coded to our jira instance.
* If a `jira:issue_updated` webhook where something long changes (e.g. someone has updated the description) then the transform doesn't handle that very well. The __facts__ section of the card looks pretty rubbish because we're trying to fit stuff in there that doesn't really handle facts like that.
* Support for adaptive cards (our MS Teams instance doesn't yet appear to support it).

